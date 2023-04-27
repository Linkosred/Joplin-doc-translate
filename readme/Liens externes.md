# Liens externes

Cette fonctionnalité permet de créer des liens vers des notes, des dossiers et des balises. Lors de l'ouverture d'un tel lien, Joplin démarrera, à moins qu'il ne soit déjà en cours d'exécution, et ouvrira l'élément correspondant.

Pour créer un lien, faites un clic droit sur une note, un dossier ou une balise dans la barre latérale et sélectionnez "Copier le lien externe". Le lien sera copié dans le presse-papiers.

## Format du lien

* `joplin://x-callback-url/openNote?id=<note id>` pour une note
* `joplin://x-callback-url/openFolder?id=<folder id>` pour un fichier
* `joplin://x-callback-url/openTag?id=<tag id>` pour un tag

## Problèmes connus

Sur macOS, si Joplin n'est pas en cours d'exécution, il démarrera mais il n'ouvrira pas la note. Si Joplin est en cours d'exécution mais sur un espace différent du lien externe, alors Joplin viendra au premier plan mais sans afficher la note.