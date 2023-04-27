# Qu'est-ce qu'un conflit ?

Un conflit se produit lorsqu'une note ou une pièce jointe est modifiée à deux endroits différents, puis synchronisée. Dans ce cas, il n'est pas possible de déterminer quelle version de la note ou de la pièce jointe vous souhaitez conserver, et donc un conflit est généré.

# Que se passe-t-il en cas de conflit ?

Lorsque Joplin détecte un conflit, la note locale est copiée dans le carnet Conflit afin d'éviter toute perte de données. Ensuite, la note à distance est téléchargée. Vous pouvez ensuite inspecter les notes dans le bloc-notes Conflit, le comparer avec votre autre version et copier toute modification qui aurait pu être écrasée.

# Comment éviter les conflits ?

Les conflits sont toujours ennuyeux à gérer, il est donc préférable de les éviter autant que possible.

Pour cela, le mieux est de synchroniser le plus souvent possible, afin de toujours travailler avec les dernières versions de vos notes.

Joplin tente de le faire en téléchargeant vos dernières modifications en quelques secondes. Cependant, le téléchargement des modifications est effectué à intervalles fixes, toutes les quelques minutes (comme défini dans l'écran de configuration) et c'est là que des conflits peuvent survenir. Cela peut également arriver si l'un de vos appareils n'a pas eu de connexion Internet pendant un certain temps, puis se synchronise. Une mauvaise connexion Internet peut également entraver la synchronisation car elle interrompra le processus, qui devra peut-être être redémarré depuis le début pour assurer la cohérence.

Donc, si vous n'avez pas ouvert votre application depuis un certain temps, synchronisez-la manuellement et attendez qu'elle se termine, de cette façon vous êtes sûr que toute modification que vous apporterez sera sur la dernière version de la note.