# À propos de l'éditeur de texte Rich texte

**TLDR:** évitez d'utiliser les plug-ins Markdown si vous avez principalement l'intention d'utiliser l'éditeur de texte enrichi et soyez conscient des limites de l'éditeur.

À la base, Joplin stocke les notes au [format Markdown](https://github.com/laurent22/joplin/blob/dev/readme/markdown.md). Markdown est un moyen simple de formater du texte qui a fière allure sur n'importe quel appareil et, bien qu'il s'agisse de texte formaté, il semble toujours parfaitement lisible dans un éditeur de texte brut.

Dans certains cas cependant, le format de balisage supplémentaire qui apparaît dans les notes peut être considéré comme un inconvénient. Le texte en gras le sera `look **like this**`  par exemple, et les tableaux pourraient ne pas être particulièrement lisibles. Pour cette raison, Joplin propose également un éditeur de texte enrichi, qui vous permet d'éditer des notes avec une expérience d'édition  [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG) Le texte en gras " ressemblera **à ceci**" et les tableaux seront plus lisibles, entre autres.

Cependant, **il y a un hic**: dans Joplin, les notes, même lorsqu'elles sont éditées avec cet éditeur de texte enrichi, sont **toujours Markdown**  sous le capot. C'est généralement une bonne chose, car cela signifie que vous pouvez basculer à tout moment entre Markdown et l'éditeur de texte enrichi, et la note est toujours lisible. C'est aussi bien si vous synchronisez avec l'application mobile, qui n'a pas d'éditeur de texte enrichi. Le hic, c'est que puisque Markdown est utilisé sous le capot, cela signifie que l'éditeur de texte enrichi a un certain nombre de limitations dont il hérite de ce format :

- Pour commencer, **la plupart des plugins Markdown ne seront pas compatibles**. Si vous ouvrez une note Markdown qui utilise un tel plugin dans l'éditeur de texte enrichi, il est probable que vous perdiez le formatage spécial du plugin. Les seuls plugins pris en charge sont les plugins "clôturés" - ceux qui enveloppent une section de texte dans des backticks triples (par exemple, KaTeX, Mermaid, etc. fonctionnent). Vous pouvez voir la compatibilité d'un plugin sur l'écran de configuration de Markdown.

- Il n'est pas possible d'avoir plusieurs nouvelles lignes à la suite. Parce que dans Markdown, plusieurs nouvelles lignes seraient réduites en une seule lors du rendu.

- Les tableaux doivent avoir un en-tête, car il s'agit d'une exigence dans Markdown. Lorsque vous créez un tableau, il vous permettra de le créer sans en-tête, mais sous le capot, il en ajoutera un vide. Et la prochaine fois que vous ouvrirez la note, cet en-tête vide sera présent.

- Les éléments de liste (puces, listes numérotées et cases à cocher) dans les cellules du tableau peuvent être créés mais ne seront pas enregistrés correctement ; les listes dans les tables ne font actuellement partie d'aucune spécification Markdown.

- Tous les éléments d'une liste doivent être du même type, par exemple toutes les cases à cocher ou toutes les puces. Si vous avez besoin de deux types différents, vous devez créer deux listes différentes séparées par une règle horizontale ou similaire.

- Les modes de clavier spéciaux "vim" et "emacs" ne sont pas pris en charge.

- Si une note est de 'Markup - Markdown' et contient une mise en forme HTML, celle-ci peut être perdue lors de l'édition dans l'éditeur de texte enrichi car elle ne peut pas être convertie en Markdown. Les notes de 'Markup - HTML' ne sont pas affectées par les modifications dans l'éditeur de texte enrichi car cette conversion n'a pas lieu.

- Tous les liens de référence (`[title][link-name]`) sont convertis en liens intégrés (`[title](https://example.com)`) sont convertis en liens intégrés

Ce sont les limites connues, mais si vous remarquez un autre problème non répertorié ici, veuillez nous en informer [sur le forum](https://discourse.joplinapp.org/).