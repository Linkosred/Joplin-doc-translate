# À propos du chiffrement de bout en bout (E2EE)

Le chiffrement de bout en bout (E2EE) est un système où seul le propriétaire des données (c'est-à-dire des notes, des cahiers, des balises ou des ressources) peut les lire. Il empêche les espions potentiels, y compris les fournisseurs de télécommunications, les fournisseurs d'accès Internet et même les développeurs de Joplin, d'accéder aux données.

Le système est conçu pour vaincre toute tentative de surveillance ou de falsification, car aucun tiers ne peut déchiffrer les données communiquées ou stockées.

L'utilisation d'E2EE entraîne une légère surcharge, car les données doivent constamment être cryptées et décryptées, alors demandez-vous si vous avez vraiment besoin de cette fonctionnalité.

# Activation d'E2EE

En raison de la nature décentralisée de Joplin, E2EE doit d'abord être activé manuellement sur un seul appareil (cela créera une clé principale pour le cryptage sécurisé par votre mot de passe), puis il doit être synchronisé avec tous les autres appareils restants. Il est recommandé de commencer par l'application de bureau ou de terminal car ils fonctionnent généralement sur des appareils plus puissants (contrairement à l'application mobile), et ainsi ils peuvent crypter les données initiales plus rapidement.

Pour l'activer, veuillez suivre ces étapes :

1. Sur votre premier appareil (par exemple, sur l'application de bureau), accédez à l'écran de configuration du cryptage et cliquez sur "Activer le cryptage"
2. Saisissez votre mot de passe. Il s'agit du mot de passe Master Key qui sera utilisé pour crypter toutes vos notes. Assurez-vous de ne pas l'oublier car, pour des raisons de sécurité, il ne peut pas être récupéré.
3. Vous devez maintenant synchroniser toutes vos notes afin qu'elles soient envoyées chiffrées à la cible de synchronisation (par exemple, à OneDrive, Nextcloud, etc.). Attendez toute synchronisation éventuellement en cours et cliquez sur "Synchroniser".
4. Attendez que cette opération de synchronisation se termine. Étant donné que toutes les données doivent être renvoyées (chiffrées) à la cible de synchronisation, cela peut prendre beaucoup de temps, surtout si vous avez beaucoup de notes et de ressources. Notez que même si la synchronisation semble bloquée, elle est probablement toujours en cours d'exécution - ne l'annulez pas et laissez-la simplement fonctionner toute la nuit si nécessaire.
5. Une fois cette première opération de synchronisation effectuée, ouvrez le prochain appareil avec lequel vous vous synchronisez. Cliquez sur "Synchroniser" et attendez que l'opération de synchronisation soit terminée. L'appareil recevra la clé principale et vous devrez fournir le mot de passe correspondant. À ce stade, E2EE sera automatiquement activé sur cet appareil. Une fois terminé, cliquez à nouveau sur Synchroniser et attendez qu'il se termine.
6. Répétez l'étape 5 pour chaque périphérique.

N'activez pas manuellement le chiffrement sur plusieurs appareils en parallèle, mais attendez plutôt que les autres se synchronisent avec le premier appareil déjà chiffré. Sinon, vous risquez de vous retrouver avec plusieurs clés de chiffrement (ce qui est pris en charge par Joplin mais probablement pas ce que vous voulez).

Une fois que tous les appareils sont synchronisés avec E2EE activé, le cryptage/décryptage doit être principalement transparent. Parfois, vous pouvez voir des éléments cryptés, mais ils seront éventuellement décryptés en arrière-plan.

# Désactiver E2EE

Suivez la même procédure que ci-dessus, mais désactivez à la place E2EE sur chaque appareil un par un. Encore une fois, il pourrait être plus simple de le faire un appareil à la fois et d'attendre à chaque fois que la synchronisation se termine.

# Spécifications techniques

Pour une description plus technique, principalement pertinente pour le développement ou pour revoir la méthode utilisée, veuillez consulter la [spécification de l'encryption](https://github.com/laurent22/joplin/blob/dev/readme/spec/e2ee.md).