# Comment activer le débogage

IIl est possible d'obtenir que les applications affichent ou enregistrent plus d'informations qui pourraient aider à déboguer divers problèmes.

## Application de bureau

Si l'application démarre avec un écran blanc, ouvrez **Aide > Basculer les outils de développement** dans le menu. Ensuite, vérifiez dans la console s'il y a une erreur ou un avertissement et veuillez nous en informer.

Sinon, suivez ces instructions :

- Cliquez sur le menu **Aide > Ouvrir le dossier des paramètes** et ajoutez un fichier nommé "flags.txt" dans votre répertoire avec le contenu suivant : `--open-dev-tools --debug --log-level debug`
- Redémarrez l'application
- Les outils de développement devraient maintenant être ouverts. Cliquez sur l'onglet "Console"
- Maintenant, répétez l'action qui posait problème. La console peut afficher des avertissements ou des erreurs - veuillez les ajouter au problème GitHub. Ouvrez également log.txt dans le dossier de configuration et s'il y a une erreur ou un avertissement, veuillez également les ajouter au problème.

Assurez-vous de désactiver le débogage une fois que vous avez terminé. Le laisser activé peut entraîner une croissance très rapide de votre log.txt. Pour désactiver le débogage, il suffit de supprimer le fichier "flags.txt" créé.

### Mode sans echec

Le mode sans échec est un mode spécial qui désactive tous les plugins et rend les notes en texte brut. Vous pouvez l'utiliser si, par exemple, l'application plante ou se bloque au démarrage, ou est très lente à s'exécuter. En démarrant en mode sans échec, vous pouvez vérifier s'il s'agit d'un problème avec l'application elle-même ou avec l'un des plugins. Dans de rares cas, certaines notes peuvent également geler l'application, et le mode sans échec vous permet de modifier la note ou de la supprimer si elle pose des problèmes.

Il existe deux façons de démarrer en mode sans échec :

1. Depuis l'application, cliquez sur **Aide > Activer le mode sans échec**. L'application redémarrera en mode sans échec.

2. Si cela ne fonctionne pas, si par exemple l'application se fige avant que vous ne puissiez accéder à ce menu, vous pouvez définir un indicateur de débogage dans le fichier "flags.txt", [comme décrit ici](#desktop-application). Définissez simplement le contenu sur `--safe-mode --open-dev-tools --debug --log-level debug`.

## Application CLI

- Démarrez l'application avec `joplin --debug --log-level debug`
- Vérifiez log.txt comme indiqué ci-dessus pour l'application de bureau et joignez le journal au problème GitHub (ou uniquement les avertissements/erreurs, le cas échéant). Le répertoire de profil serait dans `~/.config/joplin`.

## Application mobile

- Dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md), appuyez sur le **bouton Log** et affichez une capture d'écran de toute erreur/avertissement.

# Création d'un rapport de bogue de bas niveau sur Android

https://developer.android.com/studio/debug/bug-report

Pour obtenir un rapport de bogue directement depuis votre appareil, procédez comme suit :

- Assurez-vous que [les options devellopeur](https://developer.android.com/studio/debug/dev-options) soit activées.
- Dans les options pour les développeurs, appuyez sur Prendre un rapport de bogue.
- Sélectionnez le type de rapport de bogue souhaité et appuyez sur Signaler.

Après un moment, vous recevez une notification indiquant que le rapport de bogue est prêt. Pour partager le rapport de bogue, appuyez sur la notification.

# Création d'un rapport de bogue de bas niveau sur iOS

Certains accidents ne peuvent pas être étudiés à l'aide des propres outils de Joplin. Dans ce cas, il peut être très utile de fournir un rapport de plantage iOS natif.

Pour cela, veuillez suivre ces instructions :

Vous pouvez l'envoyer à cette adresse 

https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/AdresseSupport.png

https://developer.apple.com/library/content/qa/qa1747/_index.html

Obtention des journaux de plantage directement à partir d'un appareil sans Xcode

Vos utilisateurs peuvent récupérer des rapports d'erreur sur leur appareil et vous les envoyer par e-mail en suivant ces instructions.

(Il n'est pas possible d'obtenir les journaux de la console de l'appareil directement à partir d'un appareil)

1. Ouvrir l'application Paramètres
2. Allez dans Confidentialité, puis Diagnostics et utilisation
3. Sélectionnez Diagnostics et données d'utilisation
4. Localisez le journal de l'application en panne. Les journaux seront nommés au format : `<AppName>_<DateTime>_<DeviceName>`
5. Sélectionnez le journal souhaité. Ensuite, à l'aide de l'interface utilisateur de sélection de texte, sélectionnez l'intégralité du texte du journal. Une fois le texte sélectionné, appuyez sur Copier
6. Collez le texte copié dans Mail et envoyez-le à une adresse e-mail comme vous le souhaitez