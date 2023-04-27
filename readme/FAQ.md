# FAQ

## Le programme d'installation reste bloqué sous Windows

Le programme d'installation peut rester bloqué si l'application n'a pas été désinstallée correctement. Pour résoudre le problème, vous devrez nettoyer l'entrée restante du registre. Pour ce faire, veuillez suivre ces étapes :

- Appuyez sur Win + R (Touche Windows + R)
- Tapez "regedit.exe"
- Accédez à `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Uninstall`
- Là-dedans, vous verrez un ou plusieurs dossiers. Ouvrez-les un par un pour trouver celui de Joplin. L'une des entrées devrait être "DisplayName" avec la valeur "Joplin xxx".
- Une fois trouvé, supprimez ce dossier.

Maintenant, essayez à nouveau d'installer et cela devrait fonctionner.

Plus d'informations ici : https://github.com/electron-userland/electron-builder/issues/4057

## Comment puis-je passer des arguments au script d'installation de Linux ?

Vous pouvez transmettre [arguments](https://github.com/laurent22/joplin/blob/dev/Joplin_install_and_update.sh#L37) au script d'installation à l'aide de cette commande.

wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash -s -- --argument1 --argument2


## L'application de bureau ne se lancera pas sous Linux

Si vous avez téléchargé AppImage directement et que vous ne l'avez donc pas installé via le script recommandé, il se peut qu'il ne soit pas actuellement autorisé à s'exécuter et que ces autorisations doivent être définies manuellement (voir [AppImage User Guide](https://docs.appimage.org/ introduction/quickstart.html#how-to-run-an-AppImage)).

Si les autorisations d'exécution sont correctes et qu'il ne se lance toujours pas, votre système ne dispose peut-être pas de la bibliothèque "libfuse2" dont AppImages a besoin pour s'exécuter. Cette exigence de bibliothèque est inhérente au format AppImage et non spécifiquement à Joplin. Pour plus d'informations, consultez [ce fil de discussion](https://discourse.joplinapp.org/t/appimage-incompatibility-in-ubuntu-22-04/25173) qui contient plus de détails sur le problème et un [correctif spécifique à Ubuntu] (https://discourse.joplinapp.org/t/appimage-incompatibility-in-ubuntu-22-04/25173/12).

## Comment puis-je modifier ma note dans un éditeur de texte externe ?

La commande de l'éditeur (peut inclure des arguments) définit l'éditeur qui sera utilisé pour ouvrir une note. Si aucun n'est fourni, il essaiera de détecter automatiquement l'éditeur par défaut. Si cela ne fait rien ou si vous voulez le changer pour Joplin, vous devez le configurer dans la commande Préférences -> Éditeur de texte.

Voici quelques exemples de configurations : (commentaires après #)

Linux/Mac :

```bash
subl -n -w # Ouvre Sublime (subl) dans une nouvelle fenêtre (-n) et attend sa fermeture (-w)
code -n --wait # Ouvre Visual Studio Code (code) dans une nouvelle fenêtre (-n) et attend la fermeture (--wait)
gedit --new-window # Ouvre gedit (éditeur de texte Gnome) dans une nouvelle fenêtre
xterm -e vim # Ouvre un nouveau terminal et ouvre vim. Peut être remplacé par un
                # terminal alternatif (gnome-terminal, terminateur, etc.)
                # ou éditeur de texte terminal (emacs, nano, etc.)
ouvrir un
     # Mac uniquement : ouvre une application graphique
```

Les fenêtres:

```bash
subl.exe -n -w # Ouvre Sublime (subl) dans une nouvelle fenêtre (-n) et attend sa fermeture (-w)
code.exe -n --wait # Ouvre Visual Studio Code dans une nouvelle fenêtre (-n) et attend la fermeture (--wait)
notepad.exe # Ouvre le Bloc-notes dans une nouvelle fenêtre
notepad++.exe --openSession # Ouvre Notepad++ dans une nouvelle fenêtre
```

Notez que le chemin d'accès au répertoire contenant l'exécutable de votre éditeur doit exister dans votre variable PATH ([Windows](https://www.computerhope.com/issues/ch000549.htm), [Linux/Mac](https://opensource. com/article/17/6/set-path-linux)) Sinon, le chemin complet vers l'exécutable doit être fourni.

## Lorsque j'ouvre une note dans vim, le curseur n'est pas visible

Cela semble être dû au paramètre `set term=ansi` dans .vimrc. Le supprimer devrait résoudre le problème. Voir https://github.com/laurent22/joplin/issues/147 pour plus d'informations.

## Toutes mes notes ont été supprimées après avoir changé l'URL WebDAV !

Lorsque vous modifiez l'URL WebDAV, assurez-vous que le nouvel emplacement a exactement le même contenu que l'ancien emplacement (c'est-à-dire copiez toutes les données Joplin vers le nouvel emplacement). Sinon, s'il n'y a rien sur le nouvel emplacement, Joplin pensera que vous avez supprimé toutes vos données et procédera également à leur suppression localement. Donc, pour changer l'URL WebDAV, veuillez suivre ces étapes :

1. Faites une sauvegarde de vos données Joplin en cas de problème. Exporter vers une archive JEX par exemple.
2. Synchronisez une dernière fois toutes vos données depuis un client Joplin (par exemple, depuis le client de bureau)
3. Fermez le client Joplin.
4. Sur votre service WebDAV, copiez tous les fichiers Joplin de l'ancien emplacement vers le nouveau. Assurez-vous également de copier le répertoire `.resource` car il contient vos images et autres pièces jointes.
5. Une fois que c'est fait, ouvrez à nouveau Joplin et modifiez l'URL WebDAV.
6. Synchronisez pour vérifier que tout fonctionne.
7. Effectuez les étapes 5 et 6 pour tous les autres clients Joplin que vous devez synchroniser.

## J'ai supprimé des notes par accident et je n'ai pas de sauvegarde

Si vous connaissez le `NOTE_ID` et que l'historique des notes est activé, vous pouvez exécuter la commande `restoreNoteRevision` à partir de la palette de commandes, par exemple `restoreNoteRevision 66457326a6ba4adeb4be8ce05e37af0d`. Joplin confirmera alors si la restauration a réussi et placera la note dans un cahier "Restored Note".
Si vous ne connaissez pas le `NOTE_ID`, vous pouvez le trouver dans la base de données Joplin sqlite en tant que `item_id` dans les tables `deleted_items` ou `revisions`. Cela nécessitera une vérification manuelle des champs `title_diff` et `body_diff` pour vérifier si le `ITEM/NOTE_ID` que vous ciblez est le bon.
Vous devez d'abord faire une copie de la base de données pour éviter d'apporter des modifications accidentelles à la base de données en direct.
Pour plus d'informations, allez [ici](https://discourse.joplinapp.org/t/restoring-deleted-notes/21304).

## Comment puis-je saisir facilement des balises Markdown dans Android ?

Vous pouvez utiliser un clavier spécial tel que [Multiling O Keyboard](https://play.google.com/store/apps/details?id=kl.ime.oh&hl=en), qui dispose de raccourcis pour créer des balises Markdown. [Plus d'informations dans cet article](https://discourse.joplinapp.org/t/android-create-new-list-item-with-enter/585/2?u=laurent).

## La synchronisation initiale est très lente, comment puis-je l'accélérer ?

Chaque fois que vous importez un grand nombre de notes, par exemple à partir d'Evernote, la première synchronisation peut prendre très longtemps. Il existe différentes techniques pour accélérer cela (si vous ne voulez pas simplement attendre la fin de la synchronisation), qui sont décrites dans [ce message](https://discourse.joplinapp.org/t/workaround-for- slow-initial-bulk-sync-after-evernote-import/746?u=laurent).

## Toutes les notes, dossiers ou balises ne sont pas affichés sur l'application mobile

Joplin n'a pas de synchronisation en arrière-plan sur les appareils mobiles. Lorsque Joplin est fermé, envoyé en arrière-plan ou que l'appareil est mis en veille (affichage éteint), la synchronisation est interrompue.

## Comment puis-je vérifier l'état de la synchronisation ?

Accédez à la page de synchronisation. Vous pouvez le trouver sur l'application de bureau sous `Aide > État de la synchronisation` et sur l'application mobile sous `Configuration > SYNC STATUS`.

`total items` = Combien d'éléments il y a au total à synchroniser.  
`synced items` = Combien d'éléments ont déjà été chargés ou téléchargés.

Si `total items` et `synced items` sont égaux, toutes les données ont été synchronisées. De plus, tous les appareils doivent avoir le même "total d'éléments".

## Est-il possible d'utiliser de vrais noms de fichiers et de dossiers dans la cible de synchronisation ?

Malheureusement ce n'est pas possible. Joplin se synchronise avec les systèmes de fichiers en utilisant un format ouvert, mais cela ne signifie pas que les fichiers de synchronisation sont censés être modifiables par l'utilisateur. Le format est conçu pour être performant et fiable, non convivial (il ne peut pas être les deux), et cela ne peut pas être modifié. Le répertoire de synchronisation Joplin n'est en fait qu'une base de données.

## Pourrait-il y avoir un mot de passe pour restreindre l'accès à Joplin ?

Le cryptage de bout en bout que Joplin implémente est de protéger les données pendant la transmission et sur le service cloud afin que vous seul puissiez y accéder.

Sur l'appareil local, il est supposé que les données sont sécurisées grâce aux fonctionnalités de sécurité intégrées au système d'exploitation. Si une sécurité supplémentaire est nécessaire, il est toujours possible de mettre les notes sur un lecteur VeraCrypt crypté par exemple.

Pour ces raisons, parce que le système d'exploitation ou vous-même pouvez facilement protéger les données locales, aucun code PIN ou mot de passe n'est actuellement pris en charge pour accéder à Joplin.

Il y a cependant un problème ouvert à ce sujet, donc les pull requests sont les bienvenues : https://github.com/laurent22/joplin/issues/289

## Pourquoi mon hôte WebDAV ne fonctionne-t-il pas ?

### Erreur "Interdit" dans Strato

Par exemple:

    MKCOL .sync/ : Erreur inconnue 2 (403) :
    
    
    
    
    
    
Interdit

    
    
Vous n'êtes pas autorisé à accéder à /.sync/
    sur ce serveur.


    

Dans ce cas, [assurez-vous d'entrer la bonne URL WebDAV](https://github.com/laurent22/joplin/issues/309).

### Les hôtes WebDAV suivants ne sont pas pris en charge

- Jianguoyun (voir [problème Github](https://github.com/laurent22/joplin/issues/4294))
- pCloud (voir [Fil de discussion](https://discourse.joplinapp.org/t/feature-request-pcloud-synchronisation/3530/51))

### La synchronisation Nextcloud ne fonctionne pas

- Vérifiez votre nom d'utilisateur et votre mot de passe. **Tapez-le manuellement** (sans le copier-coller) et réessayez.
- Vérifiez l'URL WebDAV - pour obtenir l'URL correcte, accédez à Nextcloud et, dans la barre latérale gauche, cliquez sur "Paramètres" et copiez l'URL WebDAV à partir de là. **N'oubliez pas d'ajouter le dossier que vous avez créé à cette URL**. Par exemple, si la base de l'URL WebDAV est "https://example.com/nextcloud/remote.php/webdav/" et que vous souhaitez que les notes soient synchronisées dans le répertoire "Joplin", vous devez donner l'URL " https://example.com/nextcloud/remote.php/webdav/Joplin" **et vous devez créer vous-même le répertoire "Joplin"**.
- Avez-vous activé **2FA** (authentification multi-facteurs) sur Nextcloud ? Dans ce cas, vous devez [créer un mot de passe d'application pour Joplin dans l'interface d'administration de Nextcloud](https://github.com/laurent22/joplin/issues/1453#issuecomment-486640902).

## Comment puis-je utiliser des certificats SSL auto-signés sur Android ?

Si vous souhaitez servir en utilisant https mais que vous ne pouvez pas ou ne voulez pas utiliser de certificats SSL signés par des autorités de certification de confiance (comme "Let's Encrypt"), il est possible de générer une autorité de certification personnalisée et de signer vos certificats avec. Vous pouvez générer l'autorité de certification et les certificats à l'aide de [openssl](https://gist.github.com/fntlnz/cf14feb5a46b2eda428e000157447309), mais j'aime utiliser un outil appelé [mkcert](https://github.com/FiloSottile/mkcert ) pour sa simplicité. Enfin, vous devez ajouter votre certificat CA aux paramètres Android afin qu'Android puisse reconnaître les certificats que vous avez signés avec votre CA comme valides ([link](https://support.google.com/nexus/answer/2844832?hl=en -GB)).

## Comment redémarrer Joplin sous Windows (pour que certaines modifications prennent effet) ?

Si "Afficher l'icône de la barre d'état système" est activé, la fermeture de la fenêtre Joplin ne quitte pas l'application. Pour redémarrer correctement l'application, l'une des actions suivantes doit être effectuée pour quitter Joplin :

- cliquez sur "Fichier" dans le menu puis sur "Quitter"
- faites un clic droit sur l'icône de la barre d'état Joplin, puis cliquez sur "Quitter"

De plus, le Gestionnaire des tâches de Windows peut être utilisé pour vérifier si Joplin est toujours là.

## Pourquoi l'application s'appelle t'elle Joplin ?

Le nom vient du compositeur et pianiste [Scott Joplin](https://en.wikipedia.org/wiki/Scott_Joplin), que j'écoute souvent. Son nom est également facile à retenir et à taper, donc c'était un bon choix.