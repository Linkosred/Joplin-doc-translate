# Web Clipper Joplin 

Le Web Clipper est une extension de navigateur qui vous permet d'enregistrer des pages Web et des captures d'écran à partir de votre navigateur. Pour commencer à l'utiliser, ouvrez l'application de bureau Joplin, **accédez aux options du Web Clipper** et suivez les instructions.

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/WebExtensionScreenshot.png" style="max-width: 50%; border: 1px solid gray;">

# Dépannage du service Web Clipper

The web clipper extension and the Joplin application communicates via a service, which is started by the Joplin desktop app.

However certain things can interfere with this service and prevent it from being accessible or from starting. If something does not work, check the following:

Cependant certaines choses peuvent interférer avec ce service et l'empêcher d'être accessible ou de démarrer. Si quelque chose ne fonctionne pas, vérifiez ce qui suit :

- Vérifiez que le service est démarré. Vous pouvez le vérifier dans les options du Web Clipper de l'application de bureau.
- Vérifiez que le port utilisé par le service n'est pas bloqué par un pare-feu. Vous pouvez trouver le numéro de port dans les options du Web clipper de l'application de bureau Joplin.
- Vérifiez qu'aucun proxy n'est en cours d'exécution sur la machine ou assurez-vous que les requêtes du service Web Clipper sont filtrées et autorisées. Par exemple https://github.com/laurent22/joplin/issues/561#issuecomment-392220191

Si rien de tout cela ne fonctionne, veuillez le signaler sur le [forum](https://discourse.joplinapp.org/) ou [le suivi de problème GitHub](https://github.com/laurent22/joplin/issues)

# Débogage de l'extension

## Dans Chrome

Pour fournir autant d'informations que possible lors du signalement d'un problème, vous pouvez fournir le journal des différentes consoles Chrome.

Pour ce faire, activez d'abord le mode développeur dans [chrome://extensions/](chrome://extensions/)

- Débogage de la fenêtre contextuelle : faites un clic droit sur l'icône de l'extension Joplin et sélectionnez "Inspecter la fenêtre contextuelle".
- Débogage du script d'arrière-plan : Dans `chrome://extensions/`, , cliquez sur "Inspecter le script d'arrière-plan".
- Débogage du script de contenu : Appuyez sur Ctrl+Maj+I pour ouvrir la console de la page en cours.

## Dans Firefox

- Ouvrir [à propos : débogage](about:debugging) dans Firefox.
- Assurez-vous que la case "Activer le débogage des modules complémentaires" est cochée.
- Faites défiler jusqu'à l'extension Joplin Web Clipper.
- Cliquez sur "Débogage" - cela devrait ouvrir une nouvelle fenêtre de console.

Appuyez également sur F12 pour ouvrir la console Firefox standard (certains messages de l'extension Joplin peuvent également y aller).

Utilisez maintenant l'extension normalement et reproduisez le bogue que vous rencontrez.

Copiez et collez le contenu de la fenêtre de débogage et de la console Firefox, et publiez-le sur le [forum](https://discourse.joplinapp.org/).

# Utilisation du service Web Clipper

Le service Web Clipper permet de créer, modifier ou supprimer des notes, carnets, tags, etc. depuis n'importe quelle autre application. Il expose une API avec un certain nombre de méthodes pour gérer les données de Joplin. Pour plus d'informations sur cette API et son utilisation, veuillez consulter la [documentation de l'API Joplin](https://joplinapp.org/api/references/rest_api/).