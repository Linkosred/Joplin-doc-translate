# Partager un cahier avec Joplin Cloud

En utilisant Joplin Cloud, vous pouvez partager des cahiers entre les utilisateurs et collaborer dessus - c'est-à-dire que n'importe quel participant peut afficher ou modifier des notes dans le cahier partagé.

## Comment ça marche?

Lorsqu'il est connecté à Joplin Cloud, un nouvel élément de menu "Partager le cahier" est disponible lorsque vous cliquez avec le bouton droit sur un carnet.

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/share_notebook/Sidebar.png" width="50%"/>

Cliquez dessus et une nouvelle boîte de dialogue s'affichera dans laquelle vous pourrez ajouter n'importe quel nombre de destinataires. À partir de cette boîte de dialogue, vous pouvez également supprimer un destinataire ou annuler le partage de l'ensemble du cahier, auquel cas il sera supprimé de la collection de notes de tout le monde, sauf la vôtre.

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/share_notebook/Dialog.png" width="50%"/>

Une fois cela fait, le ou les destinataires recevront une notification dans Joplin la prochaine fois qu'ils synchroniseront leurs données :

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/share_notebook/Notification.png" width="75%"/>

Puis, enfin, une fois l'invitation acceptée, Joplin téléchargera tous les carnets et notes partagés. Un cahier partagé est signalé par l'icône Partager habituelle. Désormais, l'utilisateur invité peut lire ou modifier les notes partagées, ajouter des pièces jointes, etc. et les modifications seront visibles par toutes les personnes ayant accès au cahier.

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/share_notebook/SidebarShared.png" width="50%"/>

## FAQ

### Quelle est la disponibilité de la fonctionnalité de partage de cahier ?

La fonctionnalité de partage de cahier est disponible sur Joplin Cloud.

Sur le bureau, vous pouvez partager des cahier et bien sûr afficher ou modifier tout cahier partagé avec vous.

Sur mobile et CLI, vous ne pouvez actuellement pas partager de cahier, mais vous pouvez afficher ou modifier tout cahier qui a été partagé avec vous.

### Si je partage un cahier avec quelqu'un, quel accès a-t-il ?

Actuellement, ils ont un accès complet aux données, y compris la lecture, l'écriture et la suppression de cahiers ou de notes.

### Qu'est-ce qui est réellement partagé ?

Tous les sous-cahiers, notes et ressources du cahier partagé sont partagés.

### Fonctionne-t-il avec le chiffrement de bout en bout ?

Oui. Le partageur et le destinataire doivent avoir activé E2EE pour que cela fonctionne.

### À quoi peut-il servir ?

Quelques idées:

* Planifiez un voyage avec des amis ou au sein d'une petite organisation. Par exemple, les notes pourraient contenir les cartes, les réservations d'hôtel et de vol, etc. ou tout document ou note concernant le voyage. Et tous les participants y auraient accès.

* Travailler sur un projet avec des collègues. Tout le monde peut accéder à divers documents liés au travail, les compléter, les modifier, etc. Cela pourrait servir de base de connaissances pour un projet.

* Une autre utilisation possible, qui a été demandée à plusieurs reprises, est de prendre en charge plusieurs profils. Vous pouvez créer un profil principal qui a accès à toutes les notes, et y créer un cahiers professionnel et personnel. Ensuite, vous créeriez un compte séparé pour le travail. Vous pouvez ensuite partager votre carnet de travail avec cet autre compte. De cette façon, le compte professionnel n'aura accès qu'aux cahiers professionnels. Vous pouvez utiliser cette technique de différentes manières pour répartir vos cahiers entre plusieurs comptes et garantir une séparation stricte entre les ensembles de données.