[![Donnner avec Paypal](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Donate-PayPal-green.svg)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=E8JMYD2LQ8MMA&lc=GB&item_name=Joplin+Development&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted) [![Sponsoriser sur GitHub](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/GitHub-Badge.svg)](https://github.com/sponsors/laurent22/) [![Devenez un patreon](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Patreon-Badge.svg)](https://www.patreon.com/joplin) [![Donner avec un IBAN](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/badges/Donate-IBAN.svg)](https://joplinapp.org/donate/#donations)

<img width="64" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/LinuxIcons/256x256.png" align="left" /> **Joplin** est une application gratuite et open source de prise de notes et de tâches, qui peut gérer un grand nombre de notes organisées en carnets. Les notes sont consultables, peuvent être copiées, étiquetées et modifiées directement depuis les applications ou depuis votre propre éditeur de texte. Les notes sont au format  [Markdown.](#markdown)

Les notes [peuvent être exportées](#importing) depuis Evernote dans Joplin, y compris le contenu formaté (qui est converti en Markdown), les ressources (images, pièces jointes, etc.) et les métadonnées complètes (géolocalisation, heure de mise à jour,heure de création, etc.). Les fichiers Markdown simples peuvent également être importés.

Les notes peuvent être  [synchronisées ](#synchronisation) en toute sécurité grâce [à un cryptage de bout en bout](#encryption) avec divers services cloud, notamment Nextcloud, Dropbox, OneDrive et [Joplin Cloud](https://joplinapp.org/plans/).

La recherche de texte est disponible sur toutes les plateformes pour trouver rapidement les informations dont vous avez besoin. L'application peut être personnalisée à l'aide de plugins et thèmes, et vous pouvez également créer facilement les vôtres.

L'application est disponible sur Windows, Linux, macOS, Android et iOS. Un [Web Clipper](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md), pour enregistrer les pages Web et les captures d'écran de votre navigateur, est également disponible pour [Firefox](https://addons.mozilla.org/firefox/addon/joplin-web-clipper/) et [Chrome](https://chrome.google.com/webstore/detail/joplin-web-clipper/alofnhikmmkdbbbgpnglcpdollgjjfek?hl=en-GB).

<div class="top-screenshot"><img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/home-top-img.png" style="max-width: 100%; max-height: 35em;"></div>

# Installation

Trois types d'applications sont disponibles : pour **desktop** (Windows, macOS et Linux), pour **mobile** (Android et iOS) et pour **terminal** (Windows, macOS, Linux et FreeBSD). Toutes les applications ont des interfaces utilisateur similaires et peuvent se synchroniser les unes avec les autres.

## Application de bureau

| Système d'exploitation | Download |
| --- | --- |
| Windows (32 and 64-bit) | [<img alt="Get it on Windows" width="134px" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeWindows.png" class="jop-noMdConv">](https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-Setup-2.9.17.exe) |
| macOS | [<img alt="Get it on macOS" width="134px" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeMacOS.png" class="jop-noMdConv">](https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-2.9.17.dmg) |
| Linux | [<img alt="Get it on Linux" width="134px" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeLinux.png" class="jop-noMdConv">](https://github.com/laurent22/joplin/releases/download/v2.9.17/Joplin-2.9.17.AppImage) |

**Sous Windows**, vous pouvez également utiliser la [version portable](https://github.com/laurent22/joplin/releases/download/v2.9.17/JoplinPortable.exe). L'[application portable](https://en.wikipedia.org/wiki/Portable_application) permet d'installer le logiciel sur un appareil portable tel qu'une clé USB. Copiez simplement le fichier JoplinPortable.exe dans n'importe quel répertoire de cette clé USB ; l'application créera alors un répertoire appelé "JoplinProfile" à côté du fichier exécutable

**Sous Linux**, la méthode recommandée consiste à utiliser le script d'installation suivant car il gérera également l'icône du bureau :

```
wget -O - https://raw.githubusercontent.com/laurent22/joplin/dev/Joplin_install_and_update.sh | bash
```

## Application mobile

| Système d'exploitation | Download | Alt. Download |
| --- | --- | --- |
| Android | [<img alt="Get it on Google Play" height="40px" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeAndroid.png" class="jop-noMdConv">](https://play.google.com/store/apps/details?id=net.cozic.joplin&utm_source=GitHub&utm_campaign=README&pcampaignid=MKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1) | ou téléchargez le fichier APK : [64-bit](https://github.com/laurent22/joplin-android/releases/download/android-v2.9.8/joplin-v2.9.8.apk) [32-bit](https://github.com/laurent22/joplin-android/releases/download/android-v2.9.8/joplin-v2.9.8-32bit.apk) |
| iOS | [<img alt="Get it on the App Store" height="40px" src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/BadgeIOS.png" class="jop-noMdConv">](https://itunes.apple.com/us/app/joplin/id1315599797) | -   |

## Application pour terminal 

| Système d'exploitation | Method |
| --- | --- |
| macOS, Linux, ou Windows (via [WSL](https://msdn.microsoft.com/en-us/commandline/wsl/faq?f=255&MSPPError=-2147217396)) | **Important:** Tout d'abord, [Téléchargez Node 12+](https://nodejs.org/en/download/package-manager/).<br>`NPM_CONFIG_PREFIX=~/.joplin-bin npm install -g joplin`<br>`sudo ln -s ~/.joplin-bin/bin/joplin /usr/bin/joplin`<br>Par défaut, le binaire de l'application sera installé sous `~/.joplin-bin`. Vous pouvez modifier ce répertoire si nécessaire. Alternativement, si vos autorisations npm sont configurées comme décrit [ici](https://docs.npmjs.com/getting-started/fixing-npm-permissions#option-2-change-npms-default-directory-to-another-directory) (Option 2) une simple execution `npm -g install joplin` devrait fonctionner. |

Pour le démarrer, tapez `joplin`.

Pour plus d'informations sur l'utilisation, reportez-vous à la [documentation complète de l'application pour terminal Joplin](https://joplinapp.org/terminal/).

## Web Clipper

Le Web Clipper est une extension de navigateur qui vous permet d'enregistrer des pages Web et des captures d'écran à partir de votre navigateur. Pour plus d'informations sur son installation et son utilisation, consultez la [page d'aide du Web Clipper](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md).

## Distributions alternatives non officielles

Il existe un certain nombre de distributions Joplin alternatives non officielles. Si vous ne voulez pas ou ne pouvez pas utiliser appimages ou l'une des autres versions officiellement prises en charge, vous pouvez les envisager.

Cependant, ceux-ci sont accompagnés d'une mise en garde, du fait qu'ils ne soient pas officiellement pris en charge, tout problèmes peuvent ne seront pas pris en charge par le Joplin. Les demandes d'assistance, les rapports de bogues et les conseils généraux devraient plutôt être adressés aux responsables de ces distributions.

Une liste communautaire de ces distributions peut être trouvée ici : [Distributions non officielles de Joplin](https://discourse.joplinapp.org/t/unofficial-alternative-joplin-distributions/23703)

# Sponsors

[<img title="Serei Network" width="256" src="https://joplinapp.org/images/sponsors/SeireiNetwork.png" class="jop-noMdConv">](https://seirei.ne.jp) [<img title="Hosting.de" width="256" src="https://joplinapp.org/images/sponsors/HostingDe.png" class="jop-noMdConv">](https://www.hosting.de/nextcloud/?mtm_campaign=managed-nextcloud&mtm_kwd=joplinapp&mtm_source=joplinapp-webseite&mtm_medium=banner)[<img title="Greece Golden Visa" width="256" src="https://joplinapp.org/images/sponsors/ResidenceGreece.jpg" class="jop-noMdConv">](https://residence-greece.com/)[<img title="SP Software GmbH" width="256" src="https://joplinapp.org/images/sponsors/Grundstueckspreise.png" class="jop-noMdConv">](https://grundstueckspreise.info/)

* * *

|     |     |     |     |
| --- | --- | --- | --- |
| <img width="50" src="https://avatars2.githubusercontent.com/u/215668?s=96&amp;v=4" class="jop-noMdConv"><br>[avanderberg](https://github.com/avanderberg) | <img width="50" src="https://avatars2.githubusercontent.com/u/67130?s=96&amp;v=4" class="jop-noMdConv"><br>[chr15m](https://github.com/chr15m) | <img width="50" src="https://avatars2.githubusercontent.com/u/2793530?s=96&amp;v=4" class="jop-noMdConv"><br>[CyberXZT](https://github.com/CyberXZT) | <img width="50" src="https://avatars2.githubusercontent.com/u/1307332?s=96&amp;v=4" class="jop-noMdConv"><br>[dbrandonjohnson](https://github.com/dbrandonjohnson) |
| <img width="50" src="https://avatars2.githubusercontent.com/u/49439044?s=96&amp;v=4" class="jop-noMdConv"><br>[fourstepper](https://github.com/fourstepper) | <img width="50" src="https://avatars2.githubusercontent.com/u/64712218?s=96&amp;v=4" class="jop-noMdConv"><br>[Hegghammer](https://github.com/Hegghammer) | <img width="50" src="https://avatars2.githubusercontent.com/u/3266447?s=96&amp;v=4" class="jop-noMdConv"><br>[iamwillbar](https://github.com/iamwillbar) | <img width="50" src="https://avatars2.githubusercontent.com/u/1310474?s=96&amp;v=4" class="jop-noMdConv"><br>[jknowles](https://github.com/jknowles) |
| <img width="50" src="https://avatars2.githubusercontent.com/u/11947658?s=96&amp;v=4" class="jop-noMdConv"><br>[KentBrockman](https://github.com/KentBrockman) | <img width="50" src="https://avatars2.githubusercontent.com/u/5588131?s=96&amp;v=4" class="jop-noMdConv"><br>[kianenigma](https://github.com/kianenigma) | <img width="50" src="https://avatars2.githubusercontent.com/u/24908652?s=96&amp;v=4" class="jop-noMdConv"><br>[konishi-t](https://github.com/konishi-t) | <img width="50" src="https://avatars2.githubusercontent.com/u/42319182?s=96&amp;v=4" class="jop-noMdConv"><br>[marcdw1289](https://github.com/marcdw1289) |
| <img width="50" src="https://avatars2.githubusercontent.com/u/126279083?s=96&amp;v=4" class="jop-noMdConv"><br>[matmoly](https://github.com/matmoly) | <img width="50" src="https://avatars2.githubusercontent.com/u/1788010?s=96&amp;v=4" class="jop-noMdConv"><br>[maxtruxa](https://github.com/maxtruxa) | <img width="50" src="https://avatars2.githubusercontent.com/u/29300939?s=96&amp;v=4" class="jop-noMdConv"><br>[mcejp](https://github.com/mcejp) | <img width="50" src="https://avatars2.githubusercontent.com/u/31054972?s=96&amp;v=4" class="jop-noMdConv"><br>[saarantras](https://github.com/saarantras) |
| <img width="50" src="https://avatars2.githubusercontent.com/u/327998?s=96&amp;v=4" class="jop-noMdConv"><br>[sif](https://github.com/sif) | <img width="50" src="https://avatars2.githubusercontent.com/u/765564?s=96&amp;v=4" class="jop-noMdConv"><br>[taskcruncher](https://github.com/taskcruncher) | <img width="50" src="https://avatars2.githubusercontent.com/u/333944?s=96&amp;v=4" class="jop-noMdConv"><br>[tateisu](https://github.com/tateisu) |     |

# Table of contents

- Applications
    
    - [Application bureau](https://github.com/laurent22/joplin/blob/dev/readme/desktop.md)
    - [Application mobile](https://github.com/laurent22/joplin/blob/dev/readme/mobile.md)
    - [Application terminal](https://github.com/laurent22/joplin/blob/dev/readme/terminal.md)
    - [Web Clipper](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md)
- Support
    
    - [Joplin Forum](https://discourse.joplinapp.org)
    - [Guide Markdown](https://github.com/laurent22/joplin/blob/dev/readme/markdown.md)
    - [Comment activer le chiffrement de bout en bout](https://github.com/laurent22/joplin/blob/dev/readme/e2ee.md)
    - [Qu'est-ce qu'un conflit ?](https://github.com/laurent22/joplin/blob/dev/readme/conflict.md)
    - [Comment activer le mode débogage](https://github.com/laurent22/joplin/blob/dev/readme/debugging.md)
    - [À propos des limites de l'éditeur de texte Rich Text](https://github.com/laurent22/joplin/blob/dev/readme/rich_text_editor.md)
    - [Liens externes](https://github.com/laurent22/joplin/blob/dev/readme/external_links.md)
    - [FAQ](https://github.com/laurent22/joplin/blob/dev/readme/faq.md)
- Joplin Cloud
    
    - [Partager un carnet](https://github.com/laurent22/joplin/blob/dev/readme/share_notebook.md)
    - [Publier une note](https://github.com/laurent22/joplin/blob/dev/readme/publish_note.md)
- Joplin API - Premier pas
    
    - [Présentation de l'API Joplin](https://github.com/laurent22/joplin/blob/dev/readme/api/overview.md)
    - [Développement de plugins](https://github.com/laurent22/joplin/blob/dev/readme/api/get_started/plugins.md)
    - [Tutoriel sur les plugins](https://github.com/laurent22/joplin/blob/dev/readme/api/tutorials/toc_plugin.md)
- Joplin API - References
    
    - [Plugin API](https://joplinapp.org/api/references/plugin_api/classes/joplin.html)
    - [Data API](https://github.com/laurent22/joplin/blob/dev/readme/api/references/rest_api.md)
    - [Plugin manifest](https://github.com/laurent22/joplin/blob/dev/readme/api/references/plugin_manifest.md)
    - [Règles de chargement des plugins](https://github.com/laurent22/joplin/blob/dev/readme/api/references/plugin_loading_rules.md)
    - [Thématisation des plugins](https://github.com/laurent22/joplin/blob/dev/readme/api/references/plugin_theming.md)
- Development
    
    - [Comment créer les applications](https://github.com/laurent22/joplin/blob/dev/BUILD.md)
    - [Rédaction d'une spécification technique](https://github.com/laurent22/joplin/blob/dev/readme/technical_spec.md)
    - [Style d'application de bureau](https://github.com/laurent22/joplin/blob/dev/readme/spec/desktop_styling.md)
    - [Spécification de l'historique des notes](https://github.com/laurent22/joplin/blob/dev/readme/spec/history.md)
    - [Spécification de synchronisation](https://github.com/laurent22/joplin/blob/dev/readme/spec/sync.md)
    - [Spécification de verrouillage de synchronisation](https://github.com/laurent22/joplin/blob/dev/readme/spec/sync_lock.md)
    - [Spécification de défilement synchrone](https://github.com/laurent22/joplin/blob/dev/readme/spec/sync_scroll.md)
    - [Spécification de l'architecture du plugin](https://github.com/laurent22/joplin/blob/dev/readme/spec/plugins.md)
    - [Spécification du tri de la recherche](https://github.com/laurent22/joplin/blob/dev/readme/spec/search_sorting.md)
    - [Encryption de bout en bout: Spécification technique](https://github.com/laurent22/joplin/blob/dev/readme/spec/e2ee.md)
    - [Encryption de bout en bout: Flux de travail](https://github.com/laurent22/joplin/blob/dev/readme/spec/e2ee/workflow.md)
    - [Serveur : format d'URL de fichier](https://github.com/laurent22/joplin/blob/dev/readme/spec/server_file_url_format.md)
    - [Serveur : Delta Sync](https://github.com/laurent22/joplin/blob/dev/readme/spec/server_delta_sync.md)
    - [Serveur : Partage](https://github.com/laurent22/joplin/blob/dev/readme/spec/server_sharing.md)
- Google Summer of Code 2022
    
    - [Google Summer of Code 2022](https://github.com/laurent22/joplin/blob/dev/readme/gsoc2022/index.md)
    - [Comment soumettre une demande d'extraction GSoC](https://github.com/laurent22/joplin/blob/dev/readme/gsoc2022/pull_request_guidelines.md)
    - [Idées de projets](https://github.com/laurent22/joplin/blob/dev/readme/gsoc2022/ideas.md)
- About
    
    - [Journal des modifications (application de bureau)](https://github.com/laurent22/joplin/blob/dev/readme/changelog.md)
    - [Journal des modifications (Android)](https://github.com/laurent22/joplin/blob/dev/readme/changelog_android.md)
    - [Journal des modifications (iOS)](https://github.com/laurent22/joplin/blob/dev/readme/changelog_ios.md)
    - [Journal des modifications (application CLI)](https://github.com/laurent22/joplin/blob/dev/readme/changelog_cli.md)
    - [Journal des modifications (serveur)](https://github.com/laurent22/joplin/blob/dev/readme/changelog_server.md)
    - [Statistiques](https://github.com/laurent22/joplin/blob/dev/readme/stats.md)
    - [Faire un don](https://github.com/laurent22/joplin/blob/dev/readme/donate.md)

# Caractéristiques

- Applications de bureau, mobiles et terminaux.
- [Web Clipper](https://github.com/laurent22/joplin/blob/dev/readme/clipper.md) pour Firefox et Chrome.
- Chiffrement de bout en bout (E2EE).
- Notez l'historique (révisions).
- Synchronisation avec divers services, dont Nextcloud, Dropbox, WebDAV et OneDrive.
- Hors ligne d'abord, de sorte que toutes les données sont toujours disponibles sur l'appareil, même sans connexion Internet.
- Importez des fichiers Enex (format d'exportation Evernote) et des fichiers Markdown.
- Exportez des fichiers JEX (format Joplin Export) et des fichiers bruts.
- Prenez en charge les notes, les tâches, les balises et les carnets.
- Triez les notes selon plusieurs critères - titre, heure de mise à jour, etc.
- Prise en charge des alarmes (notifications) dans les applications mobiles et de bureau.
- Notes Markdown, qui sont rendues avec des images et une mise en forme dans les applications de bureau et mobiles. Prise en charge de fonctionnalités supplémentaires telles que la notation mathématique et les cases à cocher.
- Choix des éditeurs Markdown et Rich Text (WYSIWYG).
- Prise en charge des pièces jointes - les images sont affichées, d'autres fichiers sont liés et peuvent être ouverts dans l'application appropriée.
- Affichage en ligne des fichiers PDF, vidéo et audio.
- Fonction Aller à n'importe quoi.
- Fonctionnalité de recherche.
- Prise en charge de la géolocalisation.
- Prend en charge plusieurs langues.
- Prise en charge de l'éditeur externe - ouvrez des notes dans votre éditeur externe préféré en un seul clic dans Joplin.
- Fonctionnalité extensible via des plugins et des API de données.
- Prise en charge CSS personnalisée pour la personnalisation du démarquage rendu et de l'interface utilisateur globale.
- La disposition personnalisable permet de basculer, de déplacer et de dimensionner divers éléments.
- Les raccourcis clavier sont modifiables et permettent de lier la plupart des commandes Joplin avec la fonctionnalité d'exportation/importation.
- Prise en charge de plusieurs profils.

# Importation

## Importation depuis Evernote

Joplin a été conçu comme une solution alternative à Evernote et peut donc importer des blocs-notes Evernote complets, ainsi que des notes, des balises, des ressources (fichiers joints) et des métadonnées de note (telles que l'auteur, la géolocalisation, etc.) via des fichiers ENEX. En termes de données, les deux seules choses qui pourraient légèrement différer sont :

- Les données de reconnaissance - Les images Evernote, en particulier les documents numérisés (ou photographiés), sont associées à [des données de reconnaissance](https://en.wikipedia.org/wiki/Optical_character_recognition). Le texte qu'Evernote a pu reconnaître dans le document par exemple ne sont pas conservées lorsque la note est importée dans Joplin. Cependant, si cela devait être pris en charge dans l'outil de recherche ou dans d'autres parties de Joplin, il devrait être possible de régénérer ces données de reconnaissance puisque l'image réelle serait toujours disponible.
    
- Les Couleur, tailles de police et familles - Le texte Evernote est stocké au format HTML et est converti en Markdown pendant le processus d'importation. Pour les notes qui sont principalement en texte brut ou avec une mise en forme de base (gras, italique, puces, liens, etc.), il s'agit d'une conversion sans perte, et la note, une fois rendue au format HTML, devrait être très similaire. Les tableaux sont également importés et convertis en tableaux Markdown. Pour les notes très complexes, certaines données de mise en forme peuvent être perdues - en particulier les couleurs, les tailles de police et les polices ne seront pas importées. Cependant, le texte lui-même est toujours importé dans son intégralité, quel que soit le formatage. S'il est essentiel que ces données supplémentaires soient conservées, Joplin permet également l'importation de fichiers ENEX au format HTML.
    

Pour importer des données Evernote, exportez d'abord vos carnets Evernote vers des fichiers ENEX comme décrit [ici](https://help.evernote.com/hc/en-us/articles/209005557-How-to-back-up-export-and-restore-import-notes-and-notebooks). Suivez ensuite ces étapes :

Dans l'**application de bureau**, ouvrez Fichier > Importer > ENEX et sélectionnez votre fichier. Les notes seront importées dans un nouveau carnet séparé. Si nécessaire, ils peuvent ensuite être déplacés vers un autre bloc-notes, ou le bloc-notes peut être renommé, etc.

Dans l'**application pour terminal**, en [mode ligne de commande](https://github.com/laurent22/joplin/blob/dev/readme/terminal.md#command-line-mode), tapez `import /path/to/file.enex`. Cela importera les notes dans un nouveau carnet nommé d'après le nom du fichier.

## Importation à partir de fichiers Markdown

Joplin peut importer des notes à partir d'un fichier Markdown ordinaire. Vous pouvez soit importer un répertoire complet de fichiers Markdown, soit des fichiers individuels.

Dans l'**application de bureau**:

- **Importation de fichier**: Allez dans Fichier > Importer > MD - Markdown (fichier) et sélectionnez le fichier Markdown. Ce fichier sera ensuite importé dans le Notebook actuellement sélectionné.
- **Importation de répertoire**: Allez dans Fichier > Importer > MD - Markdown (répertoire) et sélectionnez le niveau supérieur du répertoire en cours d'importation. La structure des répertoires (dossiers) sera conservée dans Notebook > Subnotebook > Note structure dans Joplin.

Dans l'**application pour terminal**, en [mode ligne de commande](https://github.com/laurent22/joplin/blob/dev/readme/terminal.md#command-line-mode), tapez `import --format md /path/to/file.md` or `import --format md /path/to/directory/`.

## Importation à partir d'autres applications

En général, la façon d'importer des notes de n'importe quelle application dans Joplin est de convertir les notes en fichiers ENEX (format Evernote) et d'importer ces fichiers ENEX dans Joplin en utilisant la méthode ci-dessus. La plupart des applications de prise de notes prennent en charge les fichiers ENEX, cela devrait donc être relativement simple. Pour obtenir de l'aide sur des applications spécifiques, voir ci-dessous :

- Notes standard : veuillez consulter [ce didacticiel](https://programadorwebvalencia.com/migrate-notes-from-standard-notes-to-joplin/)
- Notes Tomboy : Exportez les notes vers des fichiers ENEX [comme décrit ici](https://askubuntu.com/questions/243691/how-can-i-export-my-tomboy-notes-into-evernote/608551) par exemple, et importez ces fichiers ENEX dans Joplin.
- OneNote: Tout d'abord [importez les notes de OneNote dans Evernote](https://discussion.evernote.com/topic/107736-is-there-a-way-to-import-from-onenote-into-evernote-on-the-mac/). Exportez ensuite le fichier ENEX depuis Evernote et importez-le dans Joplin.
- NixNote : Synchronisez avec Evernote, puis exportez les fichiers ENEX et importez-les dans Joplin. Plus d'infos [dans ce thread](https://discourse.joplinapp.org/t/import-from-nixnote/183/3).

# Exportation

Joplin peut exporter au format JEX (fichier d'exportation Joplin), qui est un fichier tar pouvant contenir plusieurs notes, carnets, etc. Il s'agit d'un format sans perte dans la mesure où toutes les notes, mais également des métadonnées telles que la géolocalisation, l'heure de mise à jour , balises, etc. sont conservés. Ce format est pratique à des fins de sauvegarde et peut être réimporté dans Joplin. Un format "brut" est également disponible. C'est le même que le format JEX sauf que les données sont enregistrées dans un répertoire et chaque élément représenté par un seul fichier.
Joplin est également capable d'exporter vers un certain nombre d'autres formats, y compris HTML et PDF, ce qui peut être fait pour des notes simples, des carnets ou tout.

# Synchronisation

L'un des objectifs de Joplin est d'éviter d'être lié à une entreprise ou à un service en particulier, qu'il s'agisse d'Evernote, de Google ou de Microsoft. En tant que telle, la synchronisation est conçue sans aucune dépendance matérielle à un service particulier. La majeure partie du processus de synchronisation se fait à un niveau abstrait et l'accès à des services externes, tels que Nextcloud ou Dropbox, se fait via des pilotes légers. Il est facile de prendre en charge de nouveaux services en créant des pilotes simples qui fournissent une interface de type système de fichiers, c'est-à-dire la possibilité de lire, d'écrire, de supprimer et de lister des éléments. Il est également simple de passer d'un service à un autre ou même de synchroniser plusieurs services à la fois. Chaque note, carnet, balises, ainsi que la relation entre les éléments sont transmis sous forme de fichiers texte lors de la synchronisation, ce qui signifie que les données peuvent également être déplacées vers une application différente,

Actuellement, la synchronisation est possible avec Nextcloud, WebDAV, Dropbox, OneDrive ou le système de fichiers local. Pour activer la synchronisation, veuillez suivre les instructions ci-dessous. Après cela, l'application se synchronisera en arrière-plan chaque fois qu'elle est en cours d'exécution, ou vous pouvez cliquer sur "Synchroniser" pour démarrer une synchronisation manuellement. Joplin se synchronisera automatiquement en arrière-plan après toute modification de contenu effectuée sur l'application locale.

Si le **client terminal** a été installé, il est possible de synchroniser également en dehors de l'interface utilisateur en tapant `joplin sync` depuis le terminal. Cela peut être utilisé pour configurer un script cron pour synchroniser à intervalle régulier. Par exemple, cela le ferait toutes les 30 minutes :

`*/30 * * * * /path/to/joplin sync`

## Synchronisation Nextcloud

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/nextcloud-logo-background.png" width="100" align="left" class="jop-noMdConv"> [Nextcloud](https://nextcloud.com/) est une solution de cloud privé auto-hébergée. Il peut stocker des documents, des images et des vidéos mais aussi des calendriers, des mots de passe et d'innombrables autres choses et peut les synchroniser avec votre ordinateur portable ou votre téléphone. Comme vous pouvez héberger votre propre serveur Nextcloud, vous possédez à la fois les données sur votre appareil et l'infrastructure utilisée pour la synchronisation. En tant que tel, il convient parfaitement à Joplin. La plate-forme est également bien prise en charge et avec une communauté forte, elle est donc susceptible d'exister pendant un certain temps - comme c'est de toute façon open source, ce n'est pas un service qui peut être fermé, il peut exister sur un serveur aussi longtemps qu'un choisit.

Dans l'**application de bureau** ou l'**application mobile**, accédez à [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md) et sélectionnez Nextcloud comme cible de synchronisation. Saisissez ensuite l'URL WebDAV (pour l'obtenir, cliquez sur Paramètres dans le coin inférieur gauche de la page, dans Nextcloud), c'est normalement  `https://example.com/nextcloud/remote.php/webdav/Joplin` (**assurez -vous de créer le répertoire "Joplin" dans Nextcloud**), aet définissez le nom d'utilisateur et le mot de passe. Si cela ne fonctionne pas, veuillez [consulter cette explication](https://github.com/laurent22/joplin/issues/61#issuecomment-373282608) pour plus de détails.

Dans l'**application terminal**, vous devrez définir la  `sync.target` variable de configuration et toutes les variables de configuration , et , respectivement l'URL Nextcloud WebDAV, votre nom d'utilisateur et votre mot de passe. Cela peut être fait à partir du mode ligne de commande en utilisant : `sync.5.path`, `sync.5.username` 

```
:config sync.5.path https://example.com/nextcloud/remote.php/webdav/Joplin
:config sync.5.username YOUR_USERNAME
:config sync.5.password YOUR_PASSWORD
:config sync.target 5 
```

Si la synchronisation ne fonctionne pas, veuillez consulter les journaux dans le répertoire du profil de l'application - cela est souvent dû à une URL ou à un mot de passe mal configuré. Le journal doit indiquer quel est le problème exact.

## Synchronisation WebDAV 

Sélectionnez la cible de synchronisation "WebDAV" et suivez les mêmes instructions que pour Nextcloud ci-dessus (pour l' **application terminal** , vous devrez sélectionner la cible de synchronisation 6 plutôt que 5)

Services compatibles WebDAV connus pour fonctionner avec Joplin :

- [Apache WebDAV Module](https://httpd.apache.org/docs/current/mod/mod_dav.html)
- [DriveHQ](https://www.drivehq.com)
- [Fastmail](https://www.fastmail.com/)
- [HiDrive](https://www.strato.fr/stockage-en-ligne/) from Strato. [Setup help](https://github.com/laurent22/joplin/issues/309)
- [Nginx WebDAV Module](https://nginx.org/en/docs/http/ngx_http_dav_module.html)
- [Nextcloud](https://nextcloud.com/)
- [OwnCloud](https://owncloud.org/)
- [Seafile](https://www.seafile.com/)
- [Stack](https://www.transip.nl/stack/)
- [Synology WebDAV Server](https://www.synology.com/en-us/dsm/packages/WebDAVServer)
- [WebDAV Nav](https://www.schimera.com/products/webdav-nav-server/), a macOS server.
- [Zimbra](https://www.zimbra.com/)

##  Synchronisation Dropbox

Lors de la synchronisation avec Dropbox, Joplin crée un sous-répertoire dans Dropbox, dans /Apps/Joplinet lit/écrit les notes et les carnets qu'il contient. L'application n'a accès à rien en dehors de ce répertoire.

Dans l'**application de bureau** ou l**application mobile** , sélectionnez "Dropbox" comme cible de synchronisation dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md) (c'est sélectionné par défaut). Ensuite, pour lancer le processus de synchronisation, cliquez sur le bouton "Synchroniser" dans la barre latérale et suivez les instructions.

Dans l' **application terminal**, pour lancer le processus de synchronisation, tapez  `:sync`. Il vous sera demandé de suivre un lien pour autoriser l'application.

## Synchronisation OneDrive

Lors de la synchronisation avec OneDrive, Joplin crée un sous-répertoire dans OneDrive, dans /Apps/Joplin et lit/écrit les notes et les carnets qu'il contient. L'application n'a accès à rien en dehors de ce répertoire.

Dans l'**application de bureau** ou l**application mobile** sélectionnez "OneDrive" comme cible de synchronisation dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md).  Ensuite, pour lancer le processus de synchronisation, cliquez sur le bouton "Synchroniser" dans la barre latérale et suivez les instructions.

Dans l' **application terminal**, pour lancer le processus de synchronisation, tapez  `:sync`. Il vous sera demandé de suivre un lien pour autoriser l'application (saisissez simplement vos informations d'identification Microsoft - vous n'avez pas besoin de vous inscrire sur OneDrive).

## Synchronisation S3 

Depuis Joplin 2.xx, Joplin prend en charge plusieurs fournisseurs S3. Nous exposons quelques options qui devront être configurées en fonction de votre fournisseur de choix. Nous avons testé avec UpCloud, AWS et Linode. d'autres devraient fonctionner aussi.

Dans l'**application de bureau** ou l**application mobile**, sélectionnez "S3 (Bêta)" comme cible de synchronisation dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md).

- **S3 Bucket:** le nom de votre compartiment, par exemple `joplin-bucket`
- **S3 URL:** URL complète ; Pour AWS, cela devrait être `https://s3.<regionName>.amazonaws.com/`
- **S3 Access Key & S3 Secret Key:** la clé d'accès programmatique de l'utilisateur. Pour créer une nouvelle clé et un nouveau secret sur AWS, consultez [IAM Security Credentials](https://console.aws.amazon.com/iam/home#/security_credentials). Pour les autres fournisseurs, suivez leur documentation.
- **S3 Region:** certains fournisseurs vous demandent de fournir la région de votre compartiment. Cela se présente généralement sous la forme "eu-west1" ou quelque chose de similaire selon votre région. Pour les fournisseurs qui ne nécessitent pas de région, vous pouvez la laisser vide.
- **Force Path Style**: ce paramètre permet à Joplin de communiquer avec les fournisseurs S3 à l'aide d'un chemin S3 de style plus ancien. Selon votre fournisseur, vous devrez peut-être essayer d'activer et de désactiver cette option.

Lors de la création d'un nouveau compartiment pour Joplin, désactivez **Bucket Versioning**, activez **Block all public access** et activez **le chiffrement par défaut** avec `Amazon S3 key (SSE-S3)`. Certains fournisseurs n'exposent pas ces options, et cela pourrait créer un problème de synchronisation. Essayez et faites un rapport afin que nous puissions mettre à jour la documentation de manière appropriée.

Pour ajouter une **stratégie de compartiment** à partir de la console Web AWS S3, accédez à l' onglet **Permission**. Désactivez temporairement **Bloquer tous les accès publics** pour modifier la politique de compartiment, quelque chose comme :

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                  "s3:ListBucket",
                  "s3:GetBucketLocation",
                  "s3:GetObject",
                  "s3:DeleteObject",
                  "s3:DeleteObjectVersion",
                  "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::joplin-bucket",
                "arn:aws:s3:::joplin-bucket/*"
            ]
        }
    ]
}
```

### Paramètres de configuration pour les fournisseurs testés

Tous les fournisseurs auront besoin d'un compartiment, d'une clé d'accès et d'une clé secrète.

Si vous fournissez une configuration et que vous recevez "succès !" sur "vérifier la configuration", votre synchronisation S3 devrait fonctionner pour votre fournisseur. Si vous ne recevez pas de succès, vous devrez peut-être ajuster vos paramètres ou les enregistrer, redémarrer l'application et tenter une synchronisation. Cela peut révéler des messages d'erreur plus clairs qui vous aideront à déduire le problème.

### AWS

- URL: `https://s3.<region>.amazonaws.com/` (renseignez votre région, une liste complète des adresses des terminaux peut être trouvée [ici](https://docs.aws.amazon.com/general/latest/gr/s3.html))
- Région : obligatoire
- Forcer le style de chemin : décoché

### Linode

- URL: `https://<region>.linodeobjects.com` la région se trouve dans l'URL fournie par Linode ; cette URL est également la même que l'URL fournie par Linode avec le nom du compartiment supprimé)
- Région : tout ce que vous voulez saisir ne peut pas être laissé vide
- Forcer le style de chemin : décoché

### UpCloud

- URL: `https://<account>.<region>.upcloudobjects.com` (Ils vous fourniront plusieurs URL, celle qui suit ce modèle devrait fonctionner.)
- Région : obligatoire
- Forcer le style de chemin : décoché

# Chiffrement

Joplin prend en charge le chiffrement de bout en bout (E2EE) sur toutes les applications. E2EE est un système où seul le propriétaire des notes, carnets, tags ou ressources peut les lire. Il empêche les espions potentiels, y compris les fournisseurs de télécommunications, les fournisseurs d'accès Internet et même les développeurs de Joplin, d'accéder aux données. Veuillez consulter le [didacticiel sur le chiffrement de bout en bout](https://github.com/laurent22/joplin/blob/dev/readme/e2ee.md) pour plus d'informations sur cette fonctionnalité et comment l'activer.

Pour une description plus technique, principalement pertinente pour le développement ou pour revoir la méthode utilisée, veuillez consulter la [spécification du chiffrement](https://github.com/laurent22/joplin/blob/dev/readme/spec/e2ee.md).

# Historique des notes

Les applications Joplin enregistrent automatiquement les versions précédentes de vos notes à intervalles réguliers. Ces versions sont synchronisées sur tous les appareils et peuvent être consultées à partir de l'application de bureau. Pour cela, cliquez sur le bouton "Informations" d'une note, puis cliquez sur "Version précédente de cette note". À partir de cet écran, vous pouvez afficher les versions précédentes de la note ainsi que restaurer l'une d'entre elles.

Cette fonctionnalité peut être désactivée à partir de la section "Historique des notes" de [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md), and it is also possible to change for how long the history of a note is saved.

Pour plus d'informations, veuillez consulter la [page Historique des notes](https://github.com/laurent22/joplin/blob/dev/readme/note_history.md).

# Éditeur de texte externe

Les notes Joplin peuvent être ouvertes et modifiées à l'aide d'un éditeur externe de votre choix. Il peut s'agir d'un simple éditeur de texte comme Notepad ++ ou Sublime Text ou d'un véritable éditeur Markdown comme Typora. Dans ce cas, les images seront également affichées dans l'éditeur. Pour ouvrir la note dans un éditeur externe, cliquez sur l'icône dans la barre d'outils ou appuyez sur Ctrl+E (ou Cmd+E). Votre éditeur de texte par défaut sera utilisé pour ouvrir la note. Si nécessaire, vous pouvez également spécifier l'éditeur directement dans les Options générales, sous "Commande de l'éditeur de texte".

# Pièces jointes

Tout type de fichier peut être joint à une note. Dans Markdown, les liens vers ces fichiers sont représentés par un simple identifiant de la pièce jointe, cliquer sur ce lien ouvrira le fichier dans l'application par défaut. Dans le cas de fichiers audio, vidéo et pdf, ceux-ci seront affichés en ligne avec la note et pourront donc être visualisés ou lus dans Joplin.

Dans l'**application de bureau**, les fichiers peuvent être joints soit en cliquant sur l'icône "Joindre un fichier" dans l'éditeur, soit par glisser-déposer. Si vous préférez plutôt créer un lien vers un fichier local, maintenez la touche ALT enfoncée tout en effectuant l'opération de glisser-déposer. Vous pouvez également copier et coller des images directement dans l'éditeur via Ctrl+V.

Les ressources qui ne sont attachées à aucune note seront automatiquement supprimées conformément aux paramètres [l'historique de notes](#note-history).

**Important:** Les ressources supérieures à 10 Mo ne sont actuellement pas prises en charge sur mobile. Ils planteront l'application lors de la synchronisation, il est donc recommandé de ne pas attacher de telles ressources pour le moment. La question est à l'étude.

## Téléchargement de pièces jointes

La façon dont les pièces jointes sont téléchargées lors de la synchronisation peut être personnalisée dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md), , sous "Comportement de téléchargement des pièces jointes". L'option par défaut ("Toujours") consiste à télécharger toutes les pièces jointes, tout le temps, afin que les données soient disponibles même lorsque l'appareil est hors ligne. Il est également possible de télécharger les pièces jointes manuellement (option "Manuel"), en cliquant dessus, ou automatiquement (Option "Auto"), auquel cas les pièces jointes ne sont téléchargées qu'à l'ouverture d'une note. Ces options devraient permettre d'économiser de l'espace disque et de la bande passante réseau, en particulier sur mobile.

# Notifications

Dans les applications de bureau et mobiles, une alarme peut être associée à n'importe quelle tâche. Il sera déclenché à l'heure indiquée par l'affichage d'une notification. La façon dont la notification sera affichée dépend du système d'exploitation, car chacun a une manière différente de gérer cela. Veuillez voir ci-dessous les exigences pour les applications de bureau :

- **Windows**: >= 8. Assurez-vous que le Centre d'action est activé sous Windows. Ballon de la barre des tâches pour Windows < 8. Growl comme solution de repli. Growl est prioritaire sur les bulles Windows.
- **macOS** : >= 10.8 ou Growl si antérieur.
- **Linux**: `notify-send` outil, livré via des packages `notify-osd`, `libnotify-bin` or `libnotify-tools`. GNOME devrait l'avoir par défaut, mais installez-le `libnotify-tools` si vous utilisez KDE Plasma.

Voir la [documentation et organigramme pour le choix du système de notifcation](https://github.com/mikaelbr/node-notifier/blob/master/DECISION_FLOW.md)

Sur mobile, les alarmes seront affichées à l'aide du système de notification intégré.

Si pour une raison quelconque les notifications ne fonctionnent pas, veuillez [ouvrir un ticket](https://github.com/laurent22/joplin/issues).

# Sous-carnets

Les sous-blocs-notes permettent d'organiser plusieurs blocs-notes dans une arborescence de blocs-notes. Par exemple, il peut être utilisé pour regrouper tous les carnets liés au travail, à la famille ou à un projet particulier sous un carnet parent.

![](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/SubNotebooks.png)

- Dans l'**application de bureau** , pour créer un subnotebook, faites-le glisser et déposez-le sur un autre notebook. Pour le remettre à la racine, faites-le glisser et déposez-le sur l'en-tête "Notebooks". Actuellement, seule l'application de bureau peut être utilisée pour organiser les blocs-notes.
- Dans l'**application mobile** prend en charge l'affichage et la réduction/développement de l'arborescence des blocs-notes, mais elle ne prend pas actuellement en charge le déplacement des sous-blocs vers différents blocs-notes.
- Dans l'**application pour terminal** prend en charge l'affichage de l'arborescence des sous-notebooks, mais elle ne prend pas en charge leur réduction/développement ou le déplacement des sous-notebooks.

# Markdown

Joplin utilise et rend un Markdown à saveur Github avec quelques variations et ajouts. En particulier, il ajoute la prise en charge des formules mathématiques, des cases à cocher interactives et la prise en charge des liens de note. Joplin prend également en charge les plugins Markdown qui permettent d'activer et de désactiver diverses fonctionnalités avancées de Markdown. Consultez le [Guide Markdown](https://github.com/laurent22/joplin/blob/dev/readme/markdown.md) pour plus d'informations.

# Custom CSS

Le démarquage rendu peut être personnalisé en plaçant un fichier de style utilisateur dans le répertoire du profil  `~/.config/joplin-desktop/userstyle.css` (ce chemin peut être différent sur votre appareil - vérifiez en haut de la  `General` page de [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md) pour le chemin exact). Ce fichier prend en charge la syntaxe CSS standard. Joplin **doit** être redémarré pour que le nouveau css soit appliqué, veuillez vous assurer que Joplin ne se ferme pas sur le plateau, mais qu'il sort réellement. Notez que ce fichier est utilisé à la fois pour afficher les notes et pour imprimer les notes. Soyez conscient de la façon dont le CSS peut sembler imprimé (par exemple, l'impression de texte blanc sur un fond noir n'est généralement pas souhaitée).

L'ensemble de l'interface utilisateur peut être personnalisé en plaçant un fichier de style d'éditeur personnalisé dans le répertoire de profil `~/.config/joplin-desktop/userchrome.css`.

**Important** : userstyle.css et userchrome.css sont fournis pour votre commodité, mais ce sont des paramètres avancés, et les styles que vous définissez peuvent se casser d'une version à l'autre. Si vous souhaitez les utiliser, sachez que cela peut nécessiter un travail de développement régulier de votre part pour qu'ils continuent de fonctionner. L'équipe Joplin ne peut s'engager à maintenir la stabilité de la structure HTML de l'application.

# Plugins

L'**application de bureau** a la capacité d'étendre ses fonctionnalités standard par le biais de plugins. Ces plugins adhèrent à l'[API Joplin](https://joplinapp.org/api/references/plugin_api/classes/joplin.html) et peuvent être installés et configurés dans l'application via la page `Plugins` dans [l'écran de configuration](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md).

À partir de ce menu, vous pouvez rechercher des plugins téléchargés dans le référentiel [de plugins Joplin](https://github.com/joplin/plugins) ainsi que l'installation manuelle de plugins à l'aide d'un fichier 'Joplin Plugin Archive' (*.jpl).
Une fois l'application rechargée, les plugins apparaîtront dans le menu des plugins où ils pourront être activés/désactivés ou entièrement supprimés.

Pour plus d'informations, voir  [Plugins](https://github.com/laurent22/joplin/blob/dev/readme/plugins.md)

# Recherche

Joplin implémente l'extension SQLite Full Text Search (FTS4). Cela signifie que le contenu de toutes les notes est indexé en temps réel et que les requêtes de recherche renvoient des résultats très rapidement. [Les requêtes FTS simples](https://www.sqlite.org/fts3.html#simple_fts_queries) et [requêtes d'index de texte intégrale](https://www.sqlite.org/fts3.html#full_text_index_queries) sont prises en charge. Voir ci-dessous pour la liste des requêtes prises en charge :

Une mise en garde de SQLite FTS est qu'il ne prend pas en charge les langues qui n'utilisent pas les limites des mots latins (espaces, tabulations, ponctuation). Pour résoudre ce problème, Joplin dispose d'un mode de recherche personnalisé, qui n'utilise pas FTS, mais qui possède toujours toutes ses fonctionnalités (recherche multi-termes, filtres, etc.). L'un de ses inconvénients est qu'il peut devenir lent sur les grandes collections de notes. De plus, le tri des résultats sera moins précis, car l'algorithme de classement (BM25) n'est, pour l'instant, implémenté que pour FTS. Enfin, dans ce mode, il n'y a aucune restriction sur l'utilisation du  `*` caractère générique (`swim*`, `*swim` et `ast*rix` tout fonctionne).  
Ce mode de recherche est actuellement activé si l'une des langues suivantes est détectée :

- Chinois
- Japonais
- Coréen
- Thaïlandais

## Requêtes prises en charge

| Type de recherche | Description | Exemple |
| --- | --- | --- |
| Un seul mot | Renvoie toutes les notes qui contiennent ce terme. | Par exemple, la recherche de `cat` wrenverra toutes les notes qui contiennent ce mot exact. Remarque : il ne renverra pas les notes contenant la sous-chaîne - ainsi, pour "cat", les notes contenant "cataclysmic" ou "prevaricate" ne seront **pas** renvoyées. |
| Mot multiple | Renvoie toutes les notes qui contiennent **tous** ces mots, mais pas nécessairement les unes à côté des autres. | `dog cat` \- renverra toutes les notes contenant les mots "chien" et "chat" n'importe où dans la note, pas nécessairement dans cet ordre ni l'une à côté de l'autre. Il ne renverra pas les résultats contenant uniquement "chien" ou "chat". |
| Phrase | Ajoutez des guillemets doubles pour renvoyer les notes qui contiennent exactement cette phrase. | `"shopping list"` \- renverra les notes qui contiennent ces termes exacts les unes à côté des autres et dans cet ordre. Il ne renverra pas par exemple une note qui contient "faire du shopping avec ma liste". |
| Préfixe | 	Ajoutez un caractère générique pour renvoyer toutes les notes contenant un terme avec un préfixe spécifié. | `swim*` \- renverra toutes les notes qui contiennent par ex. "swim", mais aussi "swimming", "swimsuit", etc. IMPORTANT : le caractère générique ne peut être qu'à la fin - il sera ignoré au début d'un mot (par exemple `*swim`) et sera traité comme un astérisque littéral dans milieu d'un mot (ex `ast*rix`) |
| Passer à la recherche de base | L'un des inconvénients de la recherche en texte intégral est qu'elle ignore la plupart des caractères non alphabétiques. Cependant, dans certains cas, vous souhaiterez peut-être également le rechercher. Pour ce faire, vous pouvez utiliser la recherche de base. Vous passez dans ce mode en préfixant votre recherche par une barre oblique `/`. Cela ne fournira pas les avantages de FTS mais cela permettra de rechercher exactement ce dont vous avez besoin. Notez qu'il peut également être beaucoup plus lent, voire extrêmement lent, selon votre requête. | `/"- [ ]"` \- renverra toutes les notes qui contiennent des cases à cocher non cochées. |


## Ordre de recherche

Les notes sont triées par "pertinence". Actuellement, cela signifie que les notes qui contiennent les termes demandés le plus souvent sont en haut. Pour les requêtes contenant plusieurs termes, la proximité des termes est également importante. Ceci est un peu expérimental, donc si vous remarquez une requête de recherche qui renvoie des résultats inattendus, veuillez le signaler dans le forum, en fournissant autant de détails que possible pour reproduire le problème.

# Retrouvez toutes vos notes facilement

Dans l'application de bureau, appuyez sur <kbd>Ctrl+P</kbd> ou <kbd>Cmd+P</kbd> et saisissez un titre de note ou une partie de son contenu pour y accéder. Ou tapez <kbd>#</kbd> suivi d'un nom de balise ou <kbd>@</kbd> suivi d'un nom de carnet.

# Prise en charge de plusieurs profils

Pour créer un nouveau profil, ouvrez Fichier > Changer de profil et sélectionnez Créer un nouveau profil, entrez le nom du profil et appuyez sur OK. L'application basculera automatiquement vers ce nouveau profil, que vous pouvez maintenant configurer.

Pour revenir au profil précédent, ouvrez à nouveau Fichier > Changer de profil et sélectionnez Par défaut.

Notez que les profils partagent tous certains paramètres, tels que la langue, la taille de la police, le thème, etc. Ceci est fait pour que vous n'ayez pas à reconfigurer tous les détails lors du changement de profil. D'autres paramètres tels que la configuration de la synchronisation sont par profil.

La fonctionnalité n'est disponible que sur ordinateur pour le moment et devrait être portée sur mobile assez rapidement.

# Donations

Les dons à Joplin soutiennent le développement du projet. Développer des applications de qualité prend généralement du temps, mais il y a aussi des dépenses, comme les certificats numériques pour signer les applications, les frais d'app store, l'hébergement, etc. Surtout, votre don permettra de maintenir le standard de développement actuel.

Veuillez consulter la [page donation](https://github.com/laurent22/joplin/blob/dev/readme/donate.md) pour savoir comment soutenir le développement de Joplin.

# Communauté

| Nom | Description |
| --- | --- |
| [Forum Joplin](https://discourse.joplinapp.org/) | C'est le lieu principal pour les discussions générales sur Joplin, le support utilisateur, les questions de développement logiciel et pour discuter des nouvelles fonctionnalités. C'est également là que les dernières versions bêta sont publiées et discutées. |
| [Twitter](https://twitter.com/joplinapp) | Suivez-nous sur Twitter |
| [Mastodon](https://mastodon.social/@joplinapp) | Suivez-nous sur Mastodon |
| [Patreon](https://www.patreon.com/joplin) | Les dernières nouvelles y sont souvent postées |
| [Discord server](https://discord.gg/VSj7AFHvpq) | Rejoingnez notre discord, utile pour posez vos questions à nous ou à la communauté ou discuter de fonctionnalité de Joplin !|
| [LinkedIn](https://www.linkedin.com/company/joplin) | Notre page LinkedIn |
| [Sub-reddit](https://www.reddit.com/r/joplinapp/) | Egalement un bon endroit pour obtenir de l'aide |

# Contribution au devellopement

Veuillez consulter le guide pour savoir comment contribuer au développement de Joplin : https://github.com/laurent22/joplin/blob/dev/CONTRIBUTING.md

# Traduction de l'application

Joplin est actuellement disponible dans les langues ci-dessous. Si vous souhaitez contribuer une **nouvelle traduction** , c'est assez simple, veuillez suivre ces étapes :

- [Téléchargez Poedit](https://poedit.net/), l'éditeur de traduction, et installez-le.
- [Téléchargez le fichier à traduire .](https://raw.githubusercontent.com/laurent22/joplin/dev/packages/tools/locales/joplin.pot).
- Dans Poedit, ouvrez ce fichier .pot, allez dans le menu Catalogue et cliquez sur Configuration. Remplacez "Pays" et "Langue" par votre propre pays et votre propre langue.
- À partir de là, vous pouvez traduire le fichier.
-Une fois cela fait, veuillez [ouvrir une pull request](https://github.com/laurent22/joplin/pulls) et y ajouter le fichier.

Cette traduction s'appliquera aux trois applications - bureau, mobile et terminal.

Pour **mettre à jour une traduction** , suivez les mêmes étapes que ci-dessus mais au lieu d'obtenir le fichier .pot, obtenez le fichier .po pour votre langue à partir du tableau ci-dessous.

Traductions actuelles :

|     | Langue | Fichier Po | Dernier traducteur | Pourcentage traduit |
| --- | --- | --- | --- | --- |
| <img src="https://joplinapp.org/images/flags/country-4x3/arableague.png" width="16px" class="jop-noMdConv"> | Arabic | [ar](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ar.po) | [Whaell O](mailto:Whaell@protonmail.com) | 80% |
| <img src="https://joplinapp.org/images/flags/es/basque_country.png" width="16px" class="jop-noMdConv"> | Basque | [eu](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/eu.po) | juan.abasolo@ehu.eus | 23% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ba.png" width="16px" class="jop-noMdConv"> | Bosnian (Bosna i Hercegovina) | [bs_BA](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/bs_BA.po) | [Derviš T.](mailto:dervis.t@pm.me) | 58% |
| <img src="https://joplinapp.org/images/flags/country-4x3/bg.png" width="16px" class="jop-noMdConv"> | Bulgarian (България) | [bg_BG](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/bg_BG.po) |     | 45% |
| <img src="https://joplinapp.org/images/flags/es/catalonia.png" width="16px" class="jop-noMdConv"> | Catalan | [ca](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ca.po) | [Xavi Ivars](mailto:xavi.ivars@gmail.com) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/hr.png" width="16px" class="jop-noMdConv"> | Croatian (Hrvatska) | [hr_HR](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/hr_HR.po) | [Milo Ivir](mailto:mail@milotype.de) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/cz.png" width="16px" class="jop-noMdConv"> | Czech (Česká republika) | [cs_CZ](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/cs_CZ.po) | [Michal Stanke](mailto:michal@stanke.cz) | 77% |
| <img src="https://joplinapp.org/images/flags/country-4x3/dk.png" width="16px" class="jop-noMdConv"> | Dansk (Danmark) | [da_DK](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/da_DK.po) | ERYpTION | 99% |
| <img src="https://joplinapp.org/images/flags/country-4x3/de.png" width="16px" class="jop-noMdConv"> | Deutsch (Deutschland) | [de_DE](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/de_DE.po) | [MrKanister](mailto:pueblos_spatulas@aleeas.com) | 99% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ee.png" width="16px" class="jop-noMdConv"> | Eesti Keel (Eesti) | [et_EE](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/et_EE.po) |     | 44% |
| <img src="https://joplinapp.org/images/flags/country-4x3/gb.png" width="16px" class="jop-noMdConv"> | English (United Kingdom) | [en_GB](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/en_GB.po) |     | 100% |
| <img src="https://joplinapp.org/images/flags/country-4x3/us.png" width="16px" class="jop-noMdConv"> | English (United States of America) | [en_US](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/en_US.po) |     | 100% |
| <img src="https://joplinapp.org/images/flags/country-4x3/es.png" width="16px" class="jop-noMdConv"> | Español (España) | [es_ES](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/es_ES.po) | [Francisco Villaverde](mailto:teko.gr@gmail.com) | 99% |
| <img src="https://joplinapp.org/images/flags/esperanto.png" width="16px" class="jop-noMdConv"> | Esperanto | [eo](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/eo.po) | Marton Paulo | 25% |
| <img src="https://joplinapp.org/images/flags/country-4x3/fi.png" width="16px" class="jop-noMdConv"> | Finnish (Suomi) | [fi_FI](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/fi_FI.po) | mrkaato0 | 95% |
| <img src="https://joplinapp.org/images/flags/country-4x3/fr.png" width="16px" class="jop-noMdConv"> | Français (France) | [fr_FR](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/fr_FR.po) | Laurent Cozic | 99% |
| <img src="https://joplinapp.org/images/flags/es/galicia.png" width="16px" class="jop-noMdConv"> | Galician (España) | [gl_ES](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/gl_ES.po) | [Marcos Lans](mailto:marcoslansgarza@gmail.com) | 29% |
| <img src="https://joplinapp.org/images/flags/country-4x3/id.png" width="16px" class="jop-noMdConv"> | Indonesian (Indonesia) | [id_ID](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/id_ID.po) | [Wisnu Adi Santoso](mailto:waditos@gmail.com) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/it.png" width="16px" class="jop-noMdConv"> | Italiano (Italia) | [it_IT](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/it_IT.po) | [Manuel Tassi](mailto:mannivuwiki@gmail.com) | 81% |
| <img src="https://joplinapp.org/images/flags/country-4x3/hu.png" width="16px" class="jop-noMdConv"> | Magyar (Magyarország) | [hu_HU](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/hu_HU.po) | [Magyari Balázs](mailto:balmag@gmail.com) | 78% |
| <img src="https://joplinapp.org/images/flags/country-4x3/be.png" width="16px" class="jop-noMdConv"> | Nederlands (België, Belgique, Belgien) | [nl_BE](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/nl_BE.po) |     | 79% |
| <img src="https://joplinapp.org/images/flags/country-4x3/nl.png" width="16px" class="jop-noMdConv"> | Nederlands (Nederland) | [nl_NL](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/nl_NL.po) | [MHolkamp](mailto:mholkamp@users.noreply.github.com) | 88% |
| <img src="https://joplinapp.org/images/flags/country-4x3/no.png" width="16px" class="jop-noMdConv"> | Norwegian (Norge, Noreg) | [nb_NO](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/nb_NO.po) | [Mats Estensen](mailto:code@mxe.no) | 88% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ir.png" width="16px" class="jop-noMdConv"> | Persian | [fa](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/fa.po) | [Kourosh Firoozbakht](mailto:kourox@protonmail.com) | 55% |
| <img src="https://joplinapp.org/images/flags/country-4x3/pl.png" width="16px" class="jop-noMdConv"> | Polski (Polska) | [pl_PL](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/pl_PL.po) | [X3NO](mailto:X3NO@disroot.org) | 91% |
| <img src="https://joplinapp.org/images/flags/country-4x3/br.png" width="16px" class="jop-noMdConv"> | Português (Brasil) | [pt_BR](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/pt_BR.po) | [Renato Nunes Bastos](mailto:rnbastos@gmail.com) | 88% |
| <img src="https://joplinapp.org/images/flags/country-4x3/pt.png" width="16px" class="jop-noMdConv"> | Português (Portugal) | [pt_PT](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/pt_PT.po) | [Diogo Caveiro](mailto:dcaveiro@yahoo.com) | 73% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ro.png" width="16px" class="jop-noMdConv"> | Română | [ro](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ro.po) | [Cristi Duluta](mailto:cristi.duluta@gmail.com) | 51% |
| <img src="https://joplinapp.org/images/flags/country-4x3/si.png" width="16px" class="jop-noMdConv"> | Slovenian (Slovenija) | [sl_SI](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/sl_SI.po) | [Martin Korelič](mailto:martin.korelic@protonmail.com) | 80% |
| <img src="https://joplinapp.org/images/flags/country-4x3/se.png" width="16px" class="jop-noMdConv"> | Svenska | [sv](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/sv.po) | [Jonatan Nyberg](mailto:jonatan@autistici.org) | 96% |
| <img src="https://joplinapp.org/images/flags/country-4x3/th.png" width="16px" class="jop-noMdConv"> | Thai (ประเทศไทย) | [th_TH](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/th_TH.po) |     | 36% |
| <img src="https://joplinapp.org/images/flags/country-4x3/vn.png" width="16px" class="jop-noMdConv"> | Tiếng Việt | [vi](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/vi.po) |     | 78% |
| <img src="https://joplinapp.org/images/flags/country-4x3/tr.png" width="16px" class="jop-noMdConv"> | Türkçe (Türkiye) | [tr_TR](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/tr_TR.po) | [Arda Kılıçdağı](mailto:arda@kilicdagi.com) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ua.png" width="16px" class="jop-noMdConv"> | Ukrainian (Україна) | [uk_UA](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/uk_UA.po) | [Vyacheslav Andreykiv](mailto:vandreykiv@gmail.com) | 72% |
| <img src="https://joplinapp.org/images/flags/country-4x3/gr.png" width="16px" class="jop-noMdConv"> | Ελληνικά (Ελλάδα) | [el_GR](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/el_GR.po) | [Harris Arvanitis](mailto:xaris@tuta.io) | 88% |
| <img src="https://joplinapp.org/images/flags/country-4x3/ru.png" width="16px" class="jop-noMdConv"> | Русский (Россия) | [ru_RU](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ru_RU.po) | [Dmitriy Q](mailto:krotesk@mail.ru) | 99% |
| <img src="https://joplinapp.org/images/flags/country-4x3/rs.png" width="16px" class="jop-noMdConv"> | српски језик (Србија) | [sr_RS](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/sr_RS.po) |     | 65% |
| <img src="https://joplinapp.org/images/flags/country-4x3/cn.png" width="16px" class="jop-noMdConv"> | 中文 (简体) | [zh_CN](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/zh_CN.po) | [wh201906](mailto:wh201906@yandex.com) | 97% |
| <img src="https://joplinapp.org/images/flags/country-4x3/tw.png" width="16px" class="jop-noMdConv"> | 中文 (繁體) | [zh_TW](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/zh_TW.po) | [Kevin Hsu](mailto:kevin.hsu.hws@gmail.com) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/jp.png" width="16px" class="jop-noMdConv"> | 日本語 (日本) | [ja_JP](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ja_JP.po) | [genneko](mailto:genneko217@gmail.com) | 89% |
| <img src="https://joplinapp.org/images/flags/country-4x3/kr.png" width="16px" class="jop-noMdConv"> | 한국어 | [ko](https://github.com/laurent22/joplin/blob/dev/packages/tools/locales/ko.po) | [Ji-Hyeon Gim](mailto:potatogim@potatogim.net) | 89% |

# Contributeurs

Merci à tous ceux qui ont contribué au code source de Joplin !

|     |     |     |     |     |
| --- | --- | --- | --- | --- |
| <img width="50" src="https://avatars.githubusercontent.com/u/1285584?v=4" class="jop-noMdConv"><br>[laurent22](https://github.com/laurent22) | <img width="50" src="https://avatars.githubusercontent.com/u/223439?v=4" class="jop-noMdConv"><br>[tessus](https://github.com/tessus) | <img width="50" src="https://avatars.githubusercontent.com/u/2179547?v=4" class="jop-noMdConv"><br>[CalebJohn](https://github.com/CalebJohn) | <img width="50" src="https://avatars.githubusercontent.com/u/1732810?v=4" class="jop-noMdConv"><br>[mic704b](https://github.com/mic704b) | <img width="50" src="https://avatars.githubusercontent.com/u/995612?v=4" class="jop-noMdConv"><br>[roman-r-m](https://github.com/roman-r-m) |
| <img width="50" src="https://avatars.githubusercontent.com/u/29672555?v=4" class="jop-noMdConv"><br>[genneko](https://github.com/genneko) | <img width="50" src="https://avatars.githubusercontent.com/u/63491353?v=4" class="jop-noMdConv"><br>[j-krl](https://github.com/j-krl) | <img width="50" src="https://avatars.githubusercontent.com/u/4553672?v=4" class="jop-noMdConv"><br>[tanrax](https://github.com/tanrax) | <img width="50" src="https://avatars.githubusercontent.com/u/30305957?v=4" class="jop-noMdConv"><br>[naviji](https://github.com/naviji) | <img width="50" src="https://avatars.githubusercontent.com/u/3542031?v=4" class="jop-noMdConv"><br>[PackElend](https://github.com/PackElend) |
| <img width="50" src="https://avatars.githubusercontent.com/u/8701534?v=4" class="jop-noMdConv"><br>[rtmkrlv](https://github.com/rtmkrlv) | <img width="50" src="https://avatars.githubusercontent.com/u/10997189?v=4" class="jop-noMdConv"><br>[fmrtn](https://github.com/fmrtn) | <img width="50" src="https://avatars.githubusercontent.com/u/4374338?v=4" class="jop-noMdConv"><br>[potatogim](https://github.com/potatogim) | <img width="50" src="https://avatars.githubusercontent.com/u/6979755?v=4" class="jop-noMdConv"><br>[devonzuegel](https://github.com/devonzuegel) | <img width="50" src="https://avatars.githubusercontent.com/u/26695184?v=4" class="jop-noMdConv"><br>[anjulalk](https://github.com/anjulalk) |
| <img width="50" src="https://avatars.githubusercontent.com/u/16101778?v=4" class="jop-noMdConv"><br>[gabcoh](https://github.com/gabcoh) | <img width="50" src="https://avatars.githubusercontent.com/u/10927304?v=4" class="jop-noMdConv"><br>[matsest](https://github.com/matsest) | <img width="50" src="https://avatars.githubusercontent.com/u/6319051?v=4" class="jop-noMdConv"><br>[abonte](https://github.com/abonte) | <img width="50" src="https://avatars.githubusercontent.com/u/1685517?v=4" class="jop-noMdConv"><br>[Abijeet](https://github.com/Abijeet) | <img width="50" src="https://avatars.githubusercontent.com/u/27751740?v=4" class="jop-noMdConv"><br>[ishantgupta777](https://github.com/ishantgupta777) |
| <img width="50" src="https://avatars.githubusercontent.com/u/24863925?v=4" class="jop-noMdConv"><br>[JackGruber](https://github.com/JackGruber) | <img width="50" src="https://avatars.githubusercontent.com/u/2063957?v=4" class="jop-noMdConv"><br>[Ardakilic](https://github.com/Ardakilic) | <img width="50" src="https://avatars.githubusercontent.com/u/44024553?v=4" class="jop-noMdConv"><br>[rabeehrz](https://github.com/rabeehrz) | <img width="50" src="https://avatars.githubusercontent.com/u/35633575?v=4" class="jop-noMdConv"><br>[coderrsid](https://github.com/coderrsid) | <img width="50" src="https://avatars.githubusercontent.com/u/208212?v=4" class="jop-noMdConv"><br>[foxmask](https://github.com/foxmask) |
| <img width="50" src="https://avatars.githubusercontent.com/u/6557454?v=4" class="jop-noMdConv"><br>[innocuo](https://github.com/innocuo) | <img width="50" src="https://avatars.githubusercontent.com/u/54268438?v=4" class="jop-noMdConv"><br>[Rahulm2310](https://github.com/Rahulm2310) | <img width="50" src="https://avatars.githubusercontent.com/u/1904967?v=4" class="jop-noMdConv"><br>[readingsnail](https://github.com/readingsnail) | <img width="50" src="https://avatars.githubusercontent.com/u/7415668?v=4" class="jop-noMdConv"><br>[mablin7](https://github.com/mablin7) | <img width="50" src="https://avatars.githubusercontent.com/u/3985557?v=4" class="jop-noMdConv"><br>[XarisA](https://github.com/XarisA) |
| <img width="50" src="https://avatars.githubusercontent.com/u/49979415?v=4" class="jop-noMdConv"><br>[jonath92](https://github.com/jonath92) | <img width="50" src="https://avatars.githubusercontent.com/u/4237724?v=4" class="jop-noMdConv"><br>[alexdevero](https://github.com/alexdevero) | <img width="50" src="https://avatars.githubusercontent.com/u/35904727?v=4" class="jop-noMdConv"><br>[Runo-saduwa](https://github.com/Runo-saduwa) | <img width="50" src="https://avatars.githubusercontent.com/u/5365582?v=4" class="jop-noMdConv"><br>[marcosvega91](https://github.com/marcosvega91) | <img width="50" src="https://avatars.githubusercontent.com/u/37639389?v=4" class="jop-noMdConv"><br>[petrz12](https://github.com/petrz12) |
| <img width="50" src="https://avatars.githubusercontent.com/u/51550769?v=4" class="jop-noMdConv"><br>[rnbastos](https://github.com/rnbastos) | <img width="50" src="https://avatars.githubusercontent.com/u/32396?v=4" class="jop-noMdConv"><br>[ProgramFan](https://github.com/ProgramFan) | <img width="50" src="https://avatars.githubusercontent.com/u/4245227?v=4" class="jop-noMdConv"><br>[zblesk](https://github.com/zblesk) | <img width="50" src="https://avatars.githubusercontent.com/u/5730052?v=4" class="jop-noMdConv"><br>[vsimkus](https://github.com/vsimkus) | <img width="50" src="https://avatars.githubusercontent.com/u/3194829?v=4" class="jop-noMdConv"><br>[moltenform](https://github.com/moltenform) |
| <img width="50" src="https://avatars.githubusercontent.com/u/36989112?v=4" class="jop-noMdConv"><br>[nishantwrp](https://github.com/nishantwrp) | <img width="50" src="https://avatars.githubusercontent.com/u/5199995?v=4" class="jop-noMdConv"><br>[zuphilip](https://github.com/zuphilip) | <img width="50" src="https://avatars.githubusercontent.com/u/54576074?v=4" class="jop-noMdConv"><br>[Rishabh-malhotraa](https://github.com/Rishabh-malhotraa) | <img width="50" src="https://avatars.githubusercontent.com/u/559346?v=4" class="jop-noMdConv"><br>[metbril](https://github.com/metbril) | <img width="50" src="https://avatars.githubusercontent.com/u/47623588?v=4" class="jop-noMdConv"><br>[WhiredPlanck](https://github.com/WhiredPlanck) |
| <img width="50" src="https://avatars.githubusercontent.com/u/43657314?v=4" class="jop-noMdConv"><br>[milotype](https://github.com/milotype) | <img width="50" src="https://avatars.githubusercontent.com/u/32196447?v=4" class="jop-noMdConv"><br>[yaozeye](https://github.com/yaozeye) | <img width="50" src="https://avatars.githubusercontent.com/u/12264626?v=4" class="jop-noMdConv"><br>[ylc395](https://github.com/ylc395) | <img width="50" src="https://avatars.githubusercontent.com/u/17768566?v=4" class="jop-noMdConv"><br>[RenatoXSR](https://github.com/RenatoXSR) | <img width="50" src="https://avatars.githubusercontent.com/u/54888685?v=4" class="jop-noMdConv"><br>[RedDocMD](https://github.com/RedDocMD) |
| <img width="50" src="https://avatars.githubusercontent.com/u/31567272?v=4" class="jop-noMdConv"><br>[q1011](https://github.com/q1011) | <img width="50" src="https://avatars.githubusercontent.com/u/12906090?v=4" class="jop-noMdConv"><br>[amitsin6h](https://github.com/amitsin6h) | <img width="50" src="https://avatars.githubusercontent.com/u/628474?v=4" class="jop-noMdConv"><br>[Atalanttore](https://github.com/Atalanttore) | <img width="50" src="https://avatars.githubusercontent.com/u/42747216?v=4" class="jop-noMdConv"><br>[Mannivu](https://github.com/Mannivu) | <img width="50" src="https://avatars.githubusercontent.com/u/23281486?v=4" class="jop-noMdConv"><br>[martonpaulo](https://github.com/martonpaulo) |
| <img width="50" src="https://avatars.githubusercontent.com/u/390889?v=4" class="jop-noMdConv"><br>[mmahmoudian](https://github.com/mmahmoudian) | <img width="50" src="https://avatars.githubusercontent.com/u/4497566?v=4" class="jop-noMdConv"><br>[rccavalcanti](https://github.com/rccavalcanti) | <img width="50" src="https://avatars.githubusercontent.com/u/1540054?v=4" class="jop-noMdConv"><br>[ShaneKilkelly](https://github.com/ShaneKilkelly) | <img width="50" src="https://avatars.githubusercontent.com/u/7091080?v=4" class="jop-noMdConv"><br>[sinkuu](https://github.com/sinkuu) | <img width="50" src="https://avatars.githubusercontent.com/u/6734573?v=4" class="jop-noMdConv"><br>[stweil](https://github.com/stweil) |
| <img width="50" src="https://avatars.githubusercontent.com/u/692072?v=4" class="jop-noMdConv"><br>[conyx](https://github.com/conyx) | <img width="50" src="https://avatars.githubusercontent.com/u/49116134?v=4" class="jop-noMdConv"><br>[anihm136](https://github.com/anihm136) | <img width="50" src="https://avatars.githubusercontent.com/u/937861?v=4" class="jop-noMdConv"><br>[archont00](https://github.com/archont00) | <img width="50" src="https://avatars.githubusercontent.com/u/32770029?v=4" class="jop-noMdConv"><br>[bradmcl](https://github.com/bradmcl) | <img width="50" src="https://avatars.githubusercontent.com/u/22592201?v=4" class="jop-noMdConv"><br>[tfinnberg](https://github.com/tfinnberg) |
| <img width="50" src="https://avatars.githubusercontent.com/u/8716226?v=4" class="jop-noMdConv"><br>[amandamcg](https://github.com/amandamcg) | <img width="50" src="https://avatars.githubusercontent.com/u/3870964?v=4" class="jop-noMdConv"><br>[marcushill](https://github.com/marcushill) | <img width="50" src="https://avatars.githubusercontent.com/u/102242?v=4" class="jop-noMdConv"><br>[nathanleiby](https://github.com/nathanleiby) | <img width="50" src="https://avatars.githubusercontent.com/u/226708?v=4" class="jop-noMdConv"><br>[RaphaelKimmig](https://github.com/RaphaelKimmig) | <img width="50" src="https://avatars.githubusercontent.com/u/20461071?v=4" class="jop-noMdConv"><br>[Vaso3](https://github.com/Vaso3) |
| <img width="50" src="https://avatars.githubusercontent.com/u/36303913?v=4" class="jop-noMdConv"><br>[sensor-freak](https://github.com/sensor-freak) | <img width="50" src="https://avatars.githubusercontent.com/u/63918341?v=4" class="jop-noMdConv"><br>[lkiThakur](https://github.com/lkiThakur) | <img width="50" src="https://avatars.githubusercontent.com/u/28987176?v=4" class="jop-noMdConv"><br>[infinity052](https://github.com/infinity052) | <img width="50" src="https://avatars.githubusercontent.com/u/21161146?v=4" class="jop-noMdConv"><br>[BartBucknill](https://github.com/BartBucknill) | <img width="50" src="https://avatars.githubusercontent.com/u/2494769?v=4" class="jop-noMdConv"><br>[mrwulf](https://github.com/mrwulf) |
| <img width="50" src="https://avatars.githubusercontent.com/u/560571?v=4" class="jop-noMdConv"><br>[chrisb86](https://github.com/chrisb86) | <img width="50" src="https://avatars.githubusercontent.com/u/1686759?v=4" class="jop-noMdConv"><br>[chrmoritz](https://github.com/chrmoritz) | <img width="50" src="https://avatars.githubusercontent.com/u/58074586?v=4" class="jop-noMdConv"><br>[Daeraxa](https://github.com/Daeraxa) | <img width="50" src="https://avatars.githubusercontent.com/u/71190696?v=4" class="jop-noMdConv"><br>[Elaborendum](https://github.com/Elaborendum) | <img width="50" src="https://avatars.githubusercontent.com/u/5001259?v=4" class="jop-noMdConv"><br>[ethan42411](https://github.com/ethan42411) |
| <img width="50" src="https://avatars.githubusercontent.com/u/2733783?v=4" class="jop-noMdConv"><br>[JOJ0](https://github.com/JOJ0) | <img width="50" src="https://avatars.githubusercontent.com/u/17108695?v=4" class="jop-noMdConv"><br>[jalajcodes](https://github.com/jalajcodes) | <img width="50" src="https://avatars.githubusercontent.com/u/238088?v=4" class="jop-noMdConv"><br>[jblunck](https://github.com/jblunck) | <img width="50" src="https://avatars.githubusercontent.com/u/3140223?v=4" class="jop-noMdConv"><br>[jdrobertso](https://github.com/jdrobertso) | <img width="50" src="https://avatars.githubusercontent.com/u/37297218?v=4" class="jop-noMdConv"><br>[Jesssullivan](https://github.com/Jesssullivan) |
| <img width="50" src="https://avatars.githubusercontent.com/u/339645?v=4" class="jop-noMdConv"><br>[jmontane](https://github.com/jmontane) | <img width="50" src="https://avatars.githubusercontent.com/u/69011?v=4" class="jop-noMdConv"><br>[johanhammar](https://github.com/johanhammar) | <img width="50" src="https://avatars.githubusercontent.com/u/4168339?v=4" class="jop-noMdConv"><br>[solariz](https://github.com/solariz) | <img width="50" src="https://avatars.githubusercontent.com/u/25288?v=4" class="jop-noMdConv"><br>[maicki](https://github.com/maicki) | <img width="50" src="https://avatars.githubusercontent.com/u/2136373?v=4" class="jop-noMdConv"><br>[mjjzf](https://github.com/mjjzf) |
| <img width="50" src="https://avatars.githubusercontent.com/u/27608187?v=4" class="jop-noMdConv"><br>[rt-oliveira](https://github.com/rt-oliveira) | <img width="50" src="https://avatars.githubusercontent.com/u/2486806?v=4" class="jop-noMdConv"><br>[sebastienjust](https://github.com/sebastienjust) | <img width="50" src="https://avatars.githubusercontent.com/u/28362310?v=4" class="jop-noMdConv"><br>[sealch](https://github.com/sealch) | <img width="50" src="https://avatars.githubusercontent.com/u/34258070?v=4" class="jop-noMdConv"><br>[StarFang208](https://github.com/StarFang208) | <img width="50" src="https://avatars.githubusercontent.com/u/59690052?v=4" class="jop-noMdConv"><br>[Subhra264](https://github.com/Subhra264) |
| <img width="50" src="https://avatars.githubusercontent.com/u/1782292?v=4" class="jop-noMdConv"><br>[SubodhDahal](https://github.com/SubodhDahal) | <img width="50" src="https://avatars.githubusercontent.com/u/5912371?v=4" class="jop-noMdConv"><br>[TobiasDev](https://github.com/TobiasDev) | <img width="50" src="https://avatars.githubusercontent.com/u/13502069?v=4" class="jop-noMdConv"><br>[Whaell](https://github.com/Whaell) | <img width="50" src="https://avatars.githubusercontent.com/u/29891001?v=4" class="jop-noMdConv"><br>[jyuvaraj03](https://github.com/jyuvaraj03) | <img width="50" src="https://avatars.githubusercontent.com/u/15380913?v=4" class="jop-noMdConv"><br>[kowalskidev](https://github.com/kowalskidev) |
| <img width="50" src="https://avatars.githubusercontent.com/u/337455?v=4" class="jop-noMdConv"><br>[alexchee](https://github.com/alexchee) | <img width="50" src="https://avatars.githubusercontent.com/u/5077221?v=4" class="jop-noMdConv"><br>[axq](https://github.com/axq) | <img width="50" src="https://avatars.githubusercontent.com/u/8808502?v=4" class="jop-noMdConv"><br>[barbowza](https://github.com/barbowza) | <img width="50" src="https://avatars.githubusercontent.com/u/42007357?v=4" class="jop-noMdConv"><br>[eresytter](https://github.com/eresytter) | <img width="50" src="https://avatars.githubusercontent.com/u/4316805?v=4" class="jop-noMdConv"><br>[lightray22](https://github.com/lightray22) |
| <img width="50" src="https://avatars.githubusercontent.com/u/11711053?v=4" class="jop-noMdConv"><br>[lscolombo](https://github.com/lscolombo) | <img width="50" src="https://avatars.githubusercontent.com/u/36228623?v=4" class="jop-noMdConv"><br>[mrkaato](https://github.com/mrkaato) | <img width="50" src="https://avatars.githubusercontent.com/u/17399340?v=4" class="jop-noMdConv"><br>[pf-siedler](https://github.com/pf-siedler) | <img width="50" src="https://avatars.githubusercontent.com/u/17232523?v=4" class="jop-noMdConv"><br>[ruuti](https://github.com/ruuti) | <img width="50" src="https://avatars.githubusercontent.com/u/23638148?v=4" class="jop-noMdConv"><br>[s1nceri7y](https://github.com/s1nceri7y) |
| <img width="50" src="https://avatars.githubusercontent.com/u/10117386?v=4" class="jop-noMdConv"><br>[kornava](https://github.com/kornava) | <img width="50" src="https://avatars.githubusercontent.com/u/7471938?v=4" class="jop-noMdConv"><br>[ShuiHuo](https://github.com/ShuiHuo) | <img width="50" src="https://avatars.githubusercontent.com/u/11596277?v=4" class="jop-noMdConv"><br>[ikunya](https://github.com/ikunya) | <img width="50" src="https://avatars.githubusercontent.com/u/8184424?v=4" class="jop-noMdConv"><br>[Ahmad45123](https://github.com/Ahmad45123) | <img width="50" src="https://avatars.githubusercontent.com/u/59133880?v=4" class="jop-noMdConv"><br>[bedwardly-down](https://github.com/bedwardly-down) |
| <img width="50" src="https://avatars.githubusercontent.com/u/50335724?v=4" class="jop-noMdConv"><br>[dcaveiro](https://github.com/dcaveiro) | <img width="50" src="https://avatars.githubusercontent.com/u/47456195?v=4" class="jop-noMdConv"><br>[hexclover](https://github.com/hexclover) | <img width="50" src="https://avatars.githubusercontent.com/u/45535789?v=4" class="jop-noMdConv"><br>[2jaeyeol](https://github.com/2jaeyeol) | <img width="50" src="https://avatars.githubusercontent.com/u/25622825?v=4" class="jop-noMdConv"><br>[thackeraaron](https://github.com/thackeraaron) | <img width="50" src="https://avatars.githubusercontent.com/u/15862474?v=4" class="jop-noMdConv"><br>[aaronxn](https://github.com/aaronxn) |
| <img width="50" src="https://avatars.githubusercontent.com/u/40672207?v=4" class="jop-noMdConv"><br>[xUser5000](https://github.com/xUser5000) | <img width="50" src="https://avatars.githubusercontent.com/u/56785486?v=4" class="jop-noMdConv"><br>[iamabhi222](https://github.com/iamabhi222) | <img width="50" src="https://avatars.githubusercontent.com/u/63443657?v=4" class="jop-noMdConv"><br>[Aksh-Konda](https://github.com/Aksh-Konda) | <img width="50" src="https://avatars.githubusercontent.com/u/3660978?v=4" class="jop-noMdConv"><br>[alanfortlink](https://github.com/alanfortlink) | <img width="50" src="https://avatars.githubusercontent.com/u/53372753?v=4" class="jop-noMdConv"><br>[AverageUser2](https://github.com/AverageUser2) |
| <img width="50" src="https://avatars.githubusercontent.com/u/4056990?v=4" class="jop-noMdConv"><br>[afischer211](https://github.com/afischer211) | <img width="50" src="https://avatars.githubusercontent.com/u/26230870?v=4" class="jop-noMdConv"><br>[a13xk](https://github.com/a13xk) | <img width="50" src="https://avatars.githubusercontent.com/u/14836659?v=4" class="jop-noMdConv"><br>[apankratov](https://github.com/apankratov) | <img width="50" src="https://avatars.githubusercontent.com/u/7045739?v=4" class="jop-noMdConv"><br>[teterkin](https://github.com/teterkin) | <img width="50" src="https://avatars.githubusercontent.com/u/215668?v=4" class="jop-noMdConv"><br>[avanderberg](https://github.com/avanderberg) |
| <img width="50" src="https://avatars.githubusercontent.com/u/41290751?v=4" class="jop-noMdConv"><br>[serenitatis](https://github.com/serenitatis) | <img width="50" src="https://avatars.githubusercontent.com/u/4408379?v=4" class="jop-noMdConv"><br>[lex111](https://github.com/lex111) | <img width="50" src="https://avatars.githubusercontent.com/u/60134194?v=4" class="jop-noMdConv"><br>[Alkindi42](https://github.com/Alkindi42) | <img width="50" src="https://avatars.githubusercontent.com/u/7129815?v=4" class="jop-noMdConv"><br>[Jumanjii](https://github.com/Jumanjii) | <img width="50" src="https://avatars.githubusercontent.com/u/19962243?v=4" class="jop-noMdConv"><br>[AlphaJack](https://github.com/AlphaJack) |
| <img width="50" src="https://avatars.githubusercontent.com/u/65647302?v=4" class="jop-noMdConv"><br>[Lord-Aman](https://github.com/Lord-Aman) | <img width="50" src="https://avatars.githubusercontent.com/u/14096959?v=4" class="jop-noMdConv"><br>[richtwin567](https://github.com/richtwin567) | <img width="50" src="https://avatars.githubusercontent.com/u/487182?v=4" class="jop-noMdConv"><br>[ajilderda](https://github.com/ajilderda) | <img width="50" src="https://avatars.githubusercontent.com/u/922429?v=4" class="jop-noMdConv"><br>[adrynov](https://github.com/adrynov) | <img width="50" src="https://avatars.githubusercontent.com/u/94937?v=4" class="jop-noMdConv"><br>[andrewperry](https://github.com/andrewperry) |
| <img width="50" src="https://avatars.githubusercontent.com/u/5417051?v=4" class="jop-noMdConv"><br>[tekdel](https://github.com/tekdel) | <img width="50" src="https://avatars.githubusercontent.com/u/54475686?v=4" class="jop-noMdConv"><br>[anshuman9999](https://github.com/anshuman9999) | <img width="50" src="https://avatars.githubusercontent.com/u/25694659?v=4" class="jop-noMdConv"><br>[rasklaad](https://github.com/rasklaad) | <img width="50" src="https://avatars.githubusercontent.com/u/17809291?v=4" class="jop-noMdConv"><br>[Technik-J](https://github.com/Technik-J) | <img width="50" src="https://avatars.githubusercontent.com/u/498326?v=4" class="jop-noMdConv"><br>[Shaxine](https://github.com/Shaxine) |
| <img width="50" src="https://avatars.githubusercontent.com/u/9095073?v=4" class="jop-noMdConv"><br>[antonio-ramadas](https://github.com/antonio-ramadas) | <img width="50" src="https://avatars.githubusercontent.com/u/28067395?v=4" class="jop-noMdConv"><br>[heyapoorva](https://github.com/heyapoorva) | <img width="50" src="https://avatars.githubusercontent.com/u/201215?v=4" class="jop-noMdConv"><br>[assimd](https://github.com/assimd) | <img width="50" src="https://avatars.githubusercontent.com/u/26827848?v=4" class="jop-noMdConv"><br>[Atrate](https://github.com/Atrate) | <img width="50" src="https://avatars.githubusercontent.com/u/60288895?v=4" class="jop-noMdConv"><br>[Beowulf2](https://github.com/Beowulf2) |
| <img width="50" src="https://avatars.githubusercontent.com/u/7034200?v=4" class="jop-noMdConv"><br>[bimlas](https://github.com/bimlas) | <img width="50" src="https://avatars.githubusercontent.com/u/47641641?v=4" class="jop-noMdConv"><br>[brenobaptista](https://github.com/brenobaptista) | <img width="50" src="https://avatars.githubusercontent.com/u/60824?v=4" class="jop-noMdConv"><br>[brttbndr](https://github.com/brttbndr) | <img width="50" src="https://avatars.githubusercontent.com/u/16287077?v=4" class="jop-noMdConv"><br>[carlbordum](https://github.com/carlbordum) | <img width="50" src="https://avatars.githubusercontent.com/u/20382?v=4" class="jop-noMdConv"><br>[carlosedp](https://github.com/carlosedp) |
| <img width="50" src="https://avatars.githubusercontent.com/u/105843?v=4" class="jop-noMdConv"><br>[chaifeng](https://github.com/chaifeng) | <img width="50" src="https://avatars.githubusercontent.com/u/549349?v=4" class="jop-noMdConv"><br>[charles-e](https://github.com/charles-e) | <img width="50" src="https://avatars.githubusercontent.com/u/19870089?v=4" class="jop-noMdConv"><br>[cyy5358](https://github.com/cyy5358) | <img width="50" src="https://avatars.githubusercontent.com/u/32337926?v=4" class="jop-noMdConv"><br>[Chillu1](https://github.com/Chillu1) | <img width="50" src="https://avatars.githubusercontent.com/u/2348463?v=4" class="jop-noMdConv"><br>[Techwolf12](https://github.com/Techwolf12) |
| <img width="50" src="https://avatars.githubusercontent.com/u/2282880?v=4" class="jop-noMdConv"><br>[cloudtrends](https://github.com/cloudtrends) | <img width="50" src="https://avatars.githubusercontent.com/u/17257053?v=4" class="jop-noMdConv"><br>[idcristi](https://github.com/idcristi) | <img width="50" src="https://avatars.githubusercontent.com/u/15956322?v=4" class="jop-noMdConv"><br>[damienmascre](https://github.com/damienmascre) | <img width="50" src="https://avatars.githubusercontent.com/u/1044056?v=4" class="jop-noMdConv"><br>[daniellandau](https://github.com/daniellandau) | <img width="50" src="https://avatars.githubusercontent.com/u/12847693?v=4" class="jop-noMdConv"><br>[danil-tolkachev](https://github.com/danil-tolkachev) |
| <img width="50" src="https://avatars.githubusercontent.com/u/7279100?v=4" class="jop-noMdConv"><br>[darshani28](https://github.com/darshani28) | <img width="50" src="https://avatars.githubusercontent.com/u/26189247?v=4" class="jop-noMdConv"><br>[daukadolt](https://github.com/daukadolt) | <img width="50" src="https://avatars.githubusercontent.com/u/28535750?v=4" class="jop-noMdConv"><br>[NeverMendel](https://github.com/NeverMendel) | <img width="50" src="https://avatars.githubusercontent.com/u/26790323?v=4" class="jop-noMdConv"><br>[dervist](https://github.com/dervist) | <img width="50" src="https://avatars.githubusercontent.com/u/11378282?v=4" class="jop-noMdConv"><br>[diego-betto](https://github.com/diego-betto) |
| <img width="50" src="https://avatars.githubusercontent.com/u/215270?v=4" class="jop-noMdConv"><br>[erdody](https://github.com/erdody) | <img width="50" src="https://avatars.githubusercontent.com/u/10371667?v=4" class="jop-noMdConv"><br>[domgoodwin](https://github.com/domgoodwin) | <img width="50" src="https://avatars.githubusercontent.com/u/72066?v=4" class="jop-noMdConv"><br>[b4mboo](https://github.com/b4mboo) | <img width="50" src="https://avatars.githubusercontent.com/u/5131923?v=4" class="jop-noMdConv"><br>[donbowman](https://github.com/donbowman) | <img width="50" src="https://avatars.githubusercontent.com/u/579727?v=4" class="jop-noMdConv"><br>[sirnacnud](https://github.com/sirnacnud) |
| <img width="50" src="https://avatars.githubusercontent.com/u/47756?v=4" class="jop-noMdConv"><br>[dflock](https://github.com/dflock) | <img width="50" src="https://avatars.githubusercontent.com/u/7990534?v=4" class="jop-noMdConv"><br>[drobilica](https://github.com/drobilica) | <img width="50" src="https://avatars.githubusercontent.com/u/21699905?v=4" class="jop-noMdConv"><br>[educbraga](https://github.com/educbraga) | <img width="50" src="https://avatars.githubusercontent.com/u/67867099?v=4" class="jop-noMdConv"><br>[eduardokimmel](https://github.com/eduardokimmel) | <img width="50" src="https://avatars.githubusercontent.com/u/30393516?v=4" class="jop-noMdConv"><br>[VodeniZeko](https://github.com/VodeniZeko) |
| <img width="50" src="https://avatars.githubusercontent.com/u/17415256?v=4" class="jop-noMdConv"><br>[ei-ke](https://github.com/ei-ke) | <img width="50" src="https://avatars.githubusercontent.com/u/1962738?v=4" class="jop-noMdConv"><br>[einverne](https://github.com/einverne) | <img width="50" src="https://avatars.githubusercontent.com/u/16492558?v=4" class="jop-noMdConv"><br>[eodeluga](https://github.com/eodeluga) | <img width="50" src="https://avatars.githubusercontent.com/u/16875937?v=4" class="jop-noMdConv"><br>[fathyar](https://github.com/fathyar) | <img width="50" src="https://avatars.githubusercontent.com/u/3057302?v=4" class="jop-noMdConv"><br>[fer22f](https://github.com/fer22f) |
| <img width="50" src="https://avatars.githubusercontent.com/u/43272148?v=4" class="jop-noMdConv"><br>[fpindado](https://github.com/fpindado) | <img width="50" src="https://avatars.githubusercontent.com/u/1714374?v=4" class="jop-noMdConv"><br>[FleischKarussel](https://github.com/FleischKarussel) | <img width="50" src="https://avatars.githubusercontent.com/u/18525376?v=4" class="jop-noMdConv"><br>[talkdirty](https://github.com/talkdirty) | <img width="50" src="https://avatars.githubusercontent.com/u/19814827?v=4" class="jop-noMdConv"><br>[gmaubach](https://github.com/gmaubach) | <img width="50" src="https://avatars.githubusercontent.com/u/6190183?v=4" class="jop-noMdConv"><br>[gmag11](https://github.com/gmag11) |
| <img width="50" src="https://avatars.githubusercontent.com/u/6209647?v=4" class="jop-noMdConv"><br>[Jackymancs4](https://github.com/Jackymancs4) | <img width="50" src="https://avatars.githubusercontent.com/u/297578?v=4" class="jop-noMdConv"><br>[Glandos](https://github.com/Glandos) | <img width="50" src="https://avatars.githubusercontent.com/u/24235344?v=4" class="jop-noMdConv"><br>[vibraniumdev](https://github.com/vibraniumdev) | <img width="50" src="https://avatars.githubusercontent.com/u/2257024?v=4" class="jop-noMdConv"><br>[gusbemacbe](https://github.com/gusbemacbe) | <img width="50" src="https://avatars.githubusercontent.com/u/64917442?v=4" class="jop-noMdConv"><br>[HOLLYwyh](https://github.com/HOLLYwyh) |
| <img width="50" src="https://avatars.githubusercontent.com/u/18524580?v=4" class="jop-noMdConv"><br>[Fvbor](https://github.com/Fvbor) | <img width="50" src="https://avatars.githubusercontent.com/u/22606250?v=4" class="jop-noMdConv"><br>[bennetthanna](https://github.com/bennetthanna) | <img width="50" src="https://avatars.githubusercontent.com/u/67231570?v=4" class="jop-noMdConv"><br>[harshitkathuria](https://github.com/harshitkathuria) | <img width="50" src="https://avatars.githubusercontent.com/u/1716229?v=4" class="jop-noMdConv"><br>[Vistaus](https://github.com/Vistaus) | <img width="50" src="https://avatars.githubusercontent.com/u/6509881?v=4" class="jop-noMdConv"><br>[ianjs](https://github.com/ianjs) |
| <img width="50" src="https://avatars.githubusercontent.com/u/19862172?v=4" class="jop-noMdConv"><br>[iahmedbacha](https://github.com/iahmedbacha) | <img width="50" src="https://avatars.githubusercontent.com/u/1533624?v=4" class="jop-noMdConv"><br>[IrvinDominin](https://github.com/IrvinDominin) | <img width="50" src="https://avatars.githubusercontent.com/u/33200024?v=4" class="jop-noMdConv"><br>[ishammahajan](https://github.com/ishammahajan) | <img width="50" src="https://avatars.githubusercontent.com/u/6916297?v=4" class="jop-noMdConv"><br>[ffadilaputra](https://github.com/ffadilaputra) | <img width="50" src="https://avatars.githubusercontent.com/u/19985741?v=4" class="jop-noMdConv"><br>[JRaiden16](https://github.com/JRaiden16) |
| <img width="50" src="https://avatars.githubusercontent.com/u/11466782?v=4" class="jop-noMdConv"><br>[jacobherrington](https://github.com/jacobherrington) | <img width="50" src="https://avatars.githubusercontent.com/u/9365179?v=4" class="jop-noMdConv"><br>[jamesadjinwa](https://github.com/jamesadjinwa) | <img width="50" src="https://avatars.githubusercontent.com/u/20801821?v=4" class="jop-noMdConv"><br>[jrwrigh](https://github.com/jrwrigh) | <img width="50" src="https://avatars.githubusercontent.com/u/4995433?v=4" class="jop-noMdConv"><br>[jaredcrowe](https://github.com/jaredcrowe) | <img width="50" src="https://avatars.githubusercontent.com/u/4087105?v=4" class="jop-noMdConv"><br>[volatilevar](https://github.com/volatilevar) |
| <img width="50" src="https://avatars.githubusercontent.com/u/47724360?v=4" class="jop-noMdConv"><br>[innkuika](https://github.com/innkuika) | <img width="50" src="https://avatars.githubusercontent.com/u/163555?v=4" class="jop-noMdConv"><br>[JoelRSimpson](https://github.com/JoelRSimpson) | <img width="50" src="https://avatars.githubusercontent.com/u/6965062?v=4" class="jop-noMdConv"><br>[joeltaylor](https://github.com/joeltaylor) | <img width="50" src="https://avatars.githubusercontent.com/u/242107?v=4" class="jop-noMdConv"><br>[exic](https://github.com/exic) | <img width="50" src="https://avatars.githubusercontent.com/u/13716151?v=4" class="jop-noMdConv"><br>[JonathanPlasse](https://github.com/JonathanPlasse) |
| <img width="50" src="https://avatars.githubusercontent.com/u/1248504?v=4" class="jop-noMdConv"><br>[joesfer](https://github.com/joesfer) | <img width="50" src="https://avatars.githubusercontent.com/u/6048003?v=4" class="jop-noMdConv"><br>[joybinchen](https://github.com/joybinchen) | <img width="50" src="https://avatars.githubusercontent.com/u/37601331?v=4" class="jop-noMdConv"><br>[kaustubhsh](https://github.com/kaustubhsh) | <img width="50" src="https://avatars.githubusercontent.com/u/1560189?v=4" class="jop-noMdConv"><br>[y-usuzumi](https://github.com/y-usuzumi) | <img width="50" src="https://avatars.githubusercontent.com/u/1660460?v=4" class="jop-noMdConv"><br>[xuhcc](https://github.com/xuhcc) |
| <img width="50" src="https://avatars.githubusercontent.com/u/16933735?v=4" class="jop-noMdConv"><br>[kirtanprht](https://github.com/kirtanprht) | <img width="50" src="https://avatars.githubusercontent.com/u/37491732?v=4" class="jop-noMdConv"><br>[k0ur0x](https://github.com/k0ur0x) | <img width="50" src="https://avatars.githubusercontent.com/u/7824233?v=4" class="jop-noMdConv"><br>[kklas](https://github.com/kklas) | <img width="50" src="https://avatars.githubusercontent.com/u/8622992?v=4" class="jop-noMdConv"><br>[xmlangel](https://github.com/xmlangel) | <img width="50" src="https://avatars.githubusercontent.com/u/1055100?v=4" class="jop-noMdConv"><br>[troilus](https://github.com/troilus) |
| <img width="50" src="https://avatars.githubusercontent.com/u/2599210?v=4" class="jop-noMdConv"><br>[lboullo0](https://github.com/lboullo0) | <img width="50" src="https://avatars.githubusercontent.com/u/1562062?v=4" class="jop-noMdConv"><br>[dbinary](https://github.com/dbinary) | <img width="50" src="https://avatars.githubusercontent.com/u/15436007?v=4" class="jop-noMdConv"><br>[marc-bouvier](https://github.com/marc-bouvier) | <img width="50" src="https://avatars.githubusercontent.com/u/5699725?v=4" class="jop-noMdConv"><br>[mvonmaltitz](https://github.com/mvonmaltitz) | <img width="50" src="https://avatars.githubusercontent.com/u/11036464?v=4" class="jop-noMdConv"><br>[mlkood](https://github.com/mlkood) |
| <img width="50" src="https://avatars.githubusercontent.com/u/2480960?v=4" class="jop-noMdConv"><br>[plextoriano](https://github.com/plextoriano) | <img width="50" src="https://avatars.githubusercontent.com/u/5788516?v=4" class="jop-noMdConv"><br>[Marmo](https://github.com/Marmo) | <img width="50" src="https://avatars.githubusercontent.com/u/29300939?v=4" class="jop-noMdConv"><br>[mcejp](https://github.com/mcejp) | <img width="50" src="https://avatars.githubusercontent.com/u/640949?v=4" class="jop-noMdConv"><br>[freaktechnik](https://github.com/freaktechnik) | <img width="50" src="https://avatars.githubusercontent.com/u/79802125?v=4" class="jop-noMdConv"><br>[martinkorelic](https://github.com/martinkorelic) |
| <img width="50" src="https://avatars.githubusercontent.com/u/287105?v=4" class="jop-noMdConv"><br>[Petemir](https://github.com/Petemir) | <img width="50" src="https://avatars.githubusercontent.com/u/5218859?v=4" class="jop-noMdConv"><br>[matsair](https://github.com/matsair) | <img width="50" src="https://avatars.githubusercontent.com/u/12831489?v=4" class="jop-noMdConv"><br>[mgroth0](https://github.com/mgroth0) | <img width="50" src="https://avatars.githubusercontent.com/u/21796?v=4" class="jop-noMdConv"><br>[silentmatt](https://github.com/silentmatt) | <img width="50" src="https://avatars.githubusercontent.com/u/76700192?v=4" class="jop-noMdConv"><br>[maxs-test](https://github.com/maxs-test) |
| <img width="50" src="https://avatars.githubusercontent.com/u/59669349?v=4" class="jop-noMdConv"><br>[MichBoi](https://github.com/MichBoi) | <img width="50" src="https://avatars.githubusercontent.com/u/51273874?v=4" class="jop-noMdConv"><br>[MichipX](https://github.com/MichipX) | <img width="50" src="https://avatars.githubusercontent.com/u/53177864?v=4" class="jop-noMdConv"><br>[MrTraduttore](https://github.com/MrTraduttore) | <img width="50" src="https://avatars.githubusercontent.com/u/48156230?v=4" class="jop-noMdConv"><br>[sanjarcode](https://github.com/sanjarcode) | <img width="50" src="https://avatars.githubusercontent.com/u/43955099?v=4" class="jop-noMdConv"><br>[Mustafa-ALD](https://github.com/Mustafa-ALD) |
| <img width="50" src="https://avatars.githubusercontent.com/u/9076687?v=4" class="jop-noMdConv"><br>[NJannasch](https://github.com/NJannasch) | <img width="50" src="https://avatars.githubusercontent.com/u/8016073?v=4" class="jop-noMdConv"><br>[zomglings](https://github.com/zomglings) | <img width="50" src="https://avatars.githubusercontent.com/u/10386884?v=4" class="jop-noMdConv"><br>[Frichetten](https://github.com/Frichetten) | <img width="50" src="https://avatars.githubusercontent.com/u/5541611?v=4" class="jop-noMdConv"><br>[nicolas-suzuki](https://github.com/nicolas-suzuki) | <img width="50" src="https://avatars.githubusercontent.com/u/12369770?v=4" class="jop-noMdConv"><br>[Ouvill](https://github.com/Ouvill) |
| <img width="50" src="https://avatars.githubusercontent.com/u/43815417?v=4" class="jop-noMdConv"><br>[shorty2380](https://github.com/shorty2380) | <img width="50" src="https://avatars.githubusercontent.com/u/15014287?v=4" class="jop-noMdConv"><br>[dist3r](https://github.com/dist3r) | <img width="50" src="https://avatars.githubusercontent.com/u/19418601?v=4" class="jop-noMdConv"><br>[rakleed](https://github.com/rakleed) | <img width="50" src="https://avatars.githubusercontent.com/u/7881932?v=4" class="jop-noMdConv"><br>[idle-code](https://github.com/idle-code) | <img width="50" src="https://avatars.githubusercontent.com/u/168931?v=4" class="jop-noMdConv"><br>[bobchao](https://github.com/bobchao) |
| <img width="50" src="https://avatars.githubusercontent.com/u/6306608?v=4" class="jop-noMdConv"><br>[Diadlo](https://github.com/Diadlo) | <img width="50" src="https://avatars.githubusercontent.com/u/42793024?v=4" class="jop-noMdConv"><br>[pranavmodx](https://github.com/pranavmodx) | <img width="50" src="https://avatars.githubusercontent.com/u/50834839?v=4" class="jop-noMdConv"><br>[R3dError](https://github.com/R3dError) | <img width="50" src="https://avatars.githubusercontent.com/u/42652941?v=4" class="jop-noMdConv"><br>[rajprakash00](https://github.com/rajprakash00) | <img width="50" src="https://avatars.githubusercontent.com/u/32304956?v=4" class="jop-noMdConv"><br>[rahil1304](https://github.com/rahil1304) |
| <img width="50" src="https://avatars.githubusercontent.com/u/8257474?v=4" class="jop-noMdConv"><br>[rasulkireev](https://github.com/rasulkireev) | <img width="50" src="https://avatars.githubusercontent.com/u/17312341?v=4" class="jop-noMdConv"><br>[reinhart1010](https://github.com/reinhart1010) | <img width="50" src="https://avatars.githubusercontent.com/u/60484714?v=4" class="jop-noMdConv"><br>[Retew](https://github.com/Retew) | <img width="50" src="https://avatars.githubusercontent.com/u/10456131?v=4" class="jop-noMdConv"><br>[ambrt](https://github.com/ambrt) | <img width="50" src="https://avatars.githubusercontent.com/u/15892014?v=4" class="jop-noMdConv"><br>[Derkades](https://github.com/Derkades) |
| <img width="50" src="https://avatars.githubusercontent.com/u/49439044?v=4" class="jop-noMdConv"><br>[fourstepper](https://github.com/fourstepper) | <img width="50" src="https://avatars.githubusercontent.com/u/54365?v=4" class="jop-noMdConv"><br>[rodgco](https://github.com/rodgco) | <img width="50" src="https://avatars.githubusercontent.com/u/96014?v=4" class="jop-noMdConv"><br>[Ronnie76er](https://github.com/Ronnie76er) | <img width="50" src="https://avatars.githubusercontent.com/u/79168?v=4" class="jop-noMdConv"><br>[roryokane](https://github.com/roryokane) | <img width="50" src="https://avatars.githubusercontent.com/u/744655?v=4" class="jop-noMdConv"><br>[ruzaq](https://github.com/ruzaq) |
| <img width="50" src="https://avatars.githubusercontent.com/u/20490839?v=4" class="jop-noMdConv"><br>[szokesandor](https://github.com/szokesandor) | <img width="50" src="https://avatars.githubusercontent.com/u/19328605?v=4" class="jop-noMdConv"><br>[SamuelBlickle](https://github.com/SamuelBlickle) | <img width="50" src="https://avatars.githubusercontent.com/u/80849457?v=4" class="jop-noMdConv"><br>[livingc0l0ur](https://github.com/livingc0l0ur) | <img width="50" src="https://avatars.githubusercontent.com/u/1776?v=4" class="jop-noMdConv"><br>[bronson](https://github.com/bronson) | <img width="50" src="https://avatars.githubusercontent.com/u/24606935?v=4" class="jop-noMdConv"><br>[semperor](https://github.com/semperor) |
| <img width="50" src="https://avatars.githubusercontent.com/u/607938?v=4" class="jop-noMdConv"><br>[shawnaxsom](https://github.com/shawnaxsom) | <img width="50" src="https://avatars.githubusercontent.com/u/9937486?v=4" class="jop-noMdConv"><br>[SFoskitt](https://github.com/SFoskitt) | <img width="50" src="https://avatars.githubusercontent.com/u/505011?v=4" class="jop-noMdConv"><br>[kcrt](https://github.com/kcrt) | <img width="50" src="https://avatars.githubusercontent.com/u/538584?v=4" class="jop-noMdConv"><br>[xissy](https://github.com/xissy) | <img width="50" src="https://avatars.githubusercontent.com/u/164962?v=4" class="jop-noMdConv"><br>[tams](https://github.com/tams) |
| <img width="50" src="https://avatars.githubusercontent.com/u/466122?v=4" class="jop-noMdConv"><br>[Tekki](https://github.com/Tekki) | <img width="50" src="https://avatars.githubusercontent.com/u/2112477?v=4" class="jop-noMdConv"><br>[ThatcherC](https://github.com/ThatcherC) | <img width="50" src="https://avatars.githubusercontent.com/u/21969426?v=4" class="jop-noMdConv"><br>[TheoDutch](https://github.com/TheoDutch) | <img width="50" src="https://avatars.githubusercontent.com/u/8731922?v=4" class="jop-noMdConv"><br>[tbroadley](https://github.com/tbroadley) | <img width="50" src="https://avatars.githubusercontent.com/u/114300?v=4" class="jop-noMdConv"><br>[Kriechi](https://github.com/Kriechi) |
| <img width="50" src="https://avatars.githubusercontent.com/u/3457339?v=4" class="jop-noMdConv"><br>[tkilaker](https://github.com/tkilaker) | <img width="50" src="https://avatars.githubusercontent.com/u/802148?v=4" class="jop-noMdConv"><br>[Tim-Erwin](https://github.com/Tim-Erwin) | <img width="50" src="https://avatars.githubusercontent.com/u/4201229?v=4" class="jop-noMdConv"><br>[tcyrus](https://github.com/tcyrus) | <img width="50" src="https://avatars.githubusercontent.com/u/834914?v=4" class="jop-noMdConv"><br>[tobias-grasse](https://github.com/tobias-grasse) | <img width="50" src="https://avatars.githubusercontent.com/u/6691273?v=4" class="jop-noMdConv"><br>[strobeltobias](https://github.com/strobeltobias) |
| <img width="50" src="https://avatars.githubusercontent.com/u/1677578?v=4" class="jop-noMdConv"><br>[kostegit](https://github.com/kostegit) | <img width="50" src="https://avatars.githubusercontent.com/u/70296?v=4" class="jop-noMdConv"><br>[tbergeron](https://github.com/tbergeron) | <img width="50" src="https://avatars.githubusercontent.com/u/10265443?v=4" class="jop-noMdConv"><br>[Ullas-Aithal](https://github.com/Ullas-Aithal) | <img width="50" src="https://avatars.githubusercontent.com/u/6104498?v=4" class="jop-noMdConv"><br>[MyTheValentinus](https://github.com/MyTheValentinus) | <img width="50" src="https://avatars.githubusercontent.com/u/2830093?v=4" class="jop-noMdConv"><br>[vassudanagunta](https://github.com/vassudanagunta) |
| <img width="50" src="https://avatars.githubusercontent.com/u/54314949?v=4" class="jop-noMdConv"><br>[vijayjoshi16](https://github.com/vijayjoshi16) | <img width="50" src="https://avatars.githubusercontent.com/u/59287619?v=4" class="jop-noMdConv"><br>[max-keviv](https://github.com/max-keviv) | <img width="50" src="https://avatars.githubusercontent.com/u/598576?v=4" class="jop-noMdConv"><br>[vandreykiv](https://github.com/vandreykiv) | <img width="50" src="https://avatars.githubusercontent.com/u/26511487?v=4" class="jop-noMdConv"><br>[WisdomCode](https://github.com/WisdomCode) | <img width="50" src="https://avatars.githubusercontent.com/u/1921957?v=4" class="jop-noMdConv"><br>[xsak](https://github.com/xsak) |
| <img width="50" src="https://avatars.githubusercontent.com/u/11031696?v=4" class="jop-noMdConv"><br>[ymitsos](https://github.com/ymitsos) | <img width="50" src="https://avatars.githubusercontent.com/u/63324960?v=4" class="jop-noMdConv"><br>[abolishallprivateproperty](https://github.com/abolishallprivateproperty) | <img width="50" src="https://avatars.githubusercontent.com/u/11336076?v=4" class="jop-noMdConv"><br>[aerotog](https://github.com/aerotog) | <img width="50" src="https://avatars.githubusercontent.com/u/39854348?v=4" class="jop-noMdConv"><br>[albertopasqualetto](https://github.com/albertopasqualetto) | <img width="50" src="https://avatars.githubusercontent.com/u/44570278?v=4" class="jop-noMdConv"><br>[asrient](https://github.com/asrient) |
| <img width="50" src="https://avatars.githubusercontent.com/u/621360?v=4" class="jop-noMdConv"><br>[bestlibre](https://github.com/bestlibre) | <img width="50" src="https://avatars.githubusercontent.com/u/35600612?v=4" class="jop-noMdConv"><br>[boring10](https://github.com/boring10) | <img width="50" src="https://avatars.githubusercontent.com/u/13894820?v=4" class="jop-noMdConv"><br>[cadolphs](https://github.com/cadolphs) | <img width="50" src="https://avatars.githubusercontent.com/u/12461043?v=4" class="jop-noMdConv"><br>[colorchestra](https://github.com/colorchestra) | <img width="50" src="https://avatars.githubusercontent.com/u/30935096?v=4" class="jop-noMdConv"><br>[cybertramp](https://github.com/cybertramp) |
| <img width="50" src="https://avatars.githubusercontent.com/u/15824892?v=4" class="jop-noMdConv"><br>[dartero](https://github.com/dartero) | <img width="50" src="https://avatars.githubusercontent.com/u/9694906?v=4" class="jop-noMdConv"><br>[delta-emil](https://github.com/delta-emil) | <img width="50" src="https://avatars.githubusercontent.com/u/926263?v=4" class="jop-noMdConv"><br>[doc75](https://github.com/doc75) | <img width="50" src="https://avatars.githubusercontent.com/u/5589253?v=4" class="jop-noMdConv"><br>[dsp77](https://github.com/dsp77) | <img width="50" src="https://avatars.githubusercontent.com/u/2903013?v=4" class="jop-noMdConv"><br>[ebayer](https://github.com/ebayer) |
| <img width="50" src="https://avatars.githubusercontent.com/u/9206310?v=4" class="jop-noMdConv"><br>[elsiehupp](https://github.com/elsiehupp) | <img width="50" src="https://avatars.githubusercontent.com/u/701050?v=4" class="jop-noMdConv"><br>[espinosa](https://github.com/espinosa) | <img width="50" src="https://avatars.githubusercontent.com/u/18619090?v=4" class="jop-noMdConv"><br>[exponentactivity](https://github.com/exponentactivity) | <img width="50" src="https://avatars.githubusercontent.com/u/16708935?v=4" class="jop-noMdConv"><br>[exprez135](https://github.com/exprez135) | <img width="50" src="https://avatars.githubusercontent.com/u/9768112?v=4" class="jop-noMdConv"><br>[fab4x](https://github.com/fab4x) |
| <img width="50" src="https://avatars.githubusercontent.com/u/47755037?v=4" class="jop-noMdConv"><br>[fabianski7](https://github.com/fabianski7) | <img width="50" src="https://avatars.githubusercontent.com/u/14201321?v=4" class="jop-noMdConv"><br>[rasperepodvipodvert](https://github.com/rasperepodvipodvert) | <img width="50" src="https://avatars.githubusercontent.com/u/748808?v=4" class="jop-noMdConv"><br>[gasolin](https://github.com/gasolin) | <img width="50" src="https://avatars.githubusercontent.com/u/47191051?v=4" class="jop-noMdConv"><br>[githubaccount073](https://github.com/githubaccount073) | <img width="50" src="https://avatars.githubusercontent.com/u/43672033?v=4" class="jop-noMdConv"><br>[hms5232](https://github.com/hms5232) |
| <img width="50" src="https://avatars.githubusercontent.com/u/11388094?v=4" class="jop-noMdConv"><br>[hydrandt](https://github.com/hydrandt) | <img width="50" src="https://avatars.githubusercontent.com/u/61012185?v=4" class="jop-noMdConv"><br>[iamtalwinder](https://github.com/iamtalwinder) | <img width="50" src="https://avatars.githubusercontent.com/u/557540?v=4" class="jop-noMdConv"><br>[jabdoa2](https://github.com/jabdoa2) | <img width="50" src="https://avatars.githubusercontent.com/u/29166402?v=4" class="jop-noMdConv"><br>[jduar](https://github.com/jduar) | <img width="50" src="https://avatars.githubusercontent.com/u/2678545?v=4" class="jop-noMdConv"><br>[jibedoubleve](https://github.com/jibedoubleve) |
| <img width="50" src="https://avatars.githubusercontent.com/u/53862536?v=4" class="jop-noMdConv"><br>[johanvanheusden](https://github.com/johanvanheusden) | <img width="50" src="https://avatars.githubusercontent.com/u/38327267?v=4" class="jop-noMdConv"><br>[jtagcat](https://github.com/jtagcat) | <img width="50" src="https://avatars.githubusercontent.com/u/61631665?v=4" class="jop-noMdConv"><br>[konhi](https://github.com/konhi) | <img width="50" src="https://avatars.githubusercontent.com/u/54991735?v=4" class="jop-noMdConv"><br>[krzysiekwie](https://github.com/krzysiekwie) | <img width="50" src="https://avatars.githubusercontent.com/u/12849008?v=4" class="jop-noMdConv"><br>[lighthousebulb](https://github.com/lighthousebulb) |
| <img width="50" src="https://avatars.githubusercontent.com/u/4140247?v=4" class="jop-noMdConv"><br>[luzpaz](https://github.com/luzpaz) | <img width="50" src="https://avatars.githubusercontent.com/u/29355048?v=4" class="jop-noMdConv"><br>[majsterkovic](https://github.com/majsterkovic) | <img width="50" src="https://avatars.githubusercontent.com/u/77744862?v=4" class="jop-noMdConv"><br>[mak2002](https://github.com/mak2002) | <img width="50" src="https://avatars.githubusercontent.com/u/30428258?v=4" class="jop-noMdConv"><br>[nmiquan](https://github.com/nmiquan) | <img width="50" src="https://avatars.githubusercontent.com/u/31123054?v=4" class="jop-noMdConv"><br>[nullpointer666](https://github.com/nullpointer666) |
| <img width="50" src="https://avatars.githubusercontent.com/u/2979926?v=4" class="jop-noMdConv"><br>[oscaretu](https://github.com/oscaretu) | <img width="50" src="https://avatars.githubusercontent.com/u/36965591?v=4" class="jop-noMdConv"><br>[oskarsh](https://github.com/oskarsh) | <img width="50" src="https://avatars.githubusercontent.com/u/52031346?v=4" class="jop-noMdConv"><br>[osso73](https://github.com/osso73) | <img width="50" src="https://avatars.githubusercontent.com/u/29743024?v=4" class="jop-noMdConv"><br>[over-soul](https://github.com/over-soul) | <img width="50" src="https://avatars.githubusercontent.com/u/42961947?v=4" class="jop-noMdConv"><br>[pensierocrea](https://github.com/pensierocrea) |
| <img width="50" src="https://avatars.githubusercontent.com/u/45542782?v=4" class="jop-noMdConv"><br>[pomeloy](https://github.com/pomeloy) | <img width="50" src="https://avatars.githubusercontent.com/u/10206967?v=4" class="jop-noMdConv"><br>[rhtenhove](https://github.com/rhtenhove) | <img width="50" src="https://avatars.githubusercontent.com/u/16728217?v=4" class="jop-noMdConv"><br>[rikanotank1](https://github.com/rikanotank1) | <img width="50" src="https://avatars.githubusercontent.com/u/24560368?v=4" class="jop-noMdConv"><br>[rxliuli](https://github.com/rxliuli) | <img width="50" src="https://avatars.githubusercontent.com/u/14062932?v=4" class="jop-noMdConv"><br>[simonsan](https://github.com/simonsan) |
| <img width="50" src="https://avatars.githubusercontent.com/u/5004545?v=4" class="jop-noMdConv"><br>[stellarpower](https://github.com/stellarpower) | <img width="50" src="https://avatars.githubusercontent.com/u/20983267?v=4" class="jop-noMdConv"><br>[suixinio](https://github.com/suixinio) | <img width="50" src="https://avatars.githubusercontent.com/u/12995773?v=4" class="jop-noMdConv"><br>[sumomo-99](https://github.com/sumomo-99) | <img width="50" src="https://avatars.githubusercontent.com/u/367170?v=4" class="jop-noMdConv"><br>[xtatsux](https://github.com/xtatsux) | <img width="50" src="https://avatars.githubusercontent.com/u/6908872?v=4" class="jop-noMdConv"><br>[taw00](https://github.com/taw00) |
| <img width="50" src="https://avatars.githubusercontent.com/u/10956653?v=4" class="jop-noMdConv"><br>[tcassaert](https://github.com/tcassaert) | <img width="50" src="https://avatars.githubusercontent.com/u/46327531?v=4" class="jop-noMdConv"><br>[victante](https://github.com/victante) | <img width="50" src="https://avatars.githubusercontent.com/u/7252567?v=4" class="jop-noMdConv"><br>[Voltinus](https://github.com/Voltinus) | <img width="50" src="https://avatars.githubusercontent.com/u/2216902?v=4" class="jop-noMdConv"><br>[xcffl](https://github.com/xcffl) | <img width="50" src="https://avatars.githubusercontent.com/u/46404814?v=4" class="jop-noMdConv"><br>[yourcontact](https://github.com/yourcontact) |
| <img width="50" src="https://avatars.githubusercontent.com/u/37692927?v=4" class="jop-noMdConv"><br>[zaoyifan](https://github.com/zaoyifan) | <img width="50" src="https://avatars.githubusercontent.com/u/10813608?v=4" class="jop-noMdConv"><br>[zawnk](https://github.com/zawnk) | <img width="50" src="https://avatars.githubusercontent.com/u/55245068?v=4" class="jop-noMdConv"><br>[zen-quo](https://github.com/zen-quo) | <img width="50" src="https://avatars.githubusercontent.com/u/23507174?v=4" class="jop-noMdConv"><br>[zozolina123](https://github.com/zozolina123) | <img width="50" src="https://avatars.githubusercontent.com/u/25315?v=4" class="jop-noMdConv"><br>[xcession](https://github.com/xcession) |
| <img width="50" src="https://avatars.githubusercontent.com/u/34542665?v=4" class="jop-noMdConv"><br>[paventyang](https://github.com/paventyang) | <img width="50" src="https://avatars.githubusercontent.com/u/608014?v=4" class="jop-noMdConv"><br>[jackytsu](https://github.com/jackytsu) | <img width="50" src="https://avatars.githubusercontent.com/u/1308646?v=4" class="jop-noMdConv"><br>[zhangmx](https://github.com/zhangmx) |     |     |
