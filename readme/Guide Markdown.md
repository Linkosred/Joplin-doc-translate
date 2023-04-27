# Guide Markdown

Markdown est un moyen simple de formater du texte qui a fière allure sur n'importe quel appareil. Il ne fait rien d'extraordinaire comme changer la taille, la couleur ou le type de la police - juste l'essentiel, en utilisant les symboles du clavier que vous connaissez déjà. Puisqu'il s'agit de texte brut, c'est un moyen facile de créer des notes et des documents et, si nécessaire, il peut être converti en un document HTML en texte enrichi.

Les applications de bureau et mobiles Joplin peuvent afficher à la fois le texte Markdown et le document de texte enrichi rendu.

Joplin suit la spécification [CommonMark](https://spec.commonmark.org/) avec des fonctionnalités supplémentaires ajoutées via des plugins.

## Aide-mémoire

Ceci est un bref résumé de la syntaxe Markdown.

|     | Markdown | Rendu |
| --- | --- | --- |
| **Titre 1** | <pre>\# Titre 1</pre> | # Titre 1 |
| **Titre 2** | <pre>\## Titre 2</pre> | ## Titre 2 |
| **Titre 3** | <pre>\### Titre 3</pre> | ### Titre 3 |
| **Gras** | <pre>Voici du `**texte gras**`</pre> | Voici du **texte gras** |
| **Italique** | <pre>Voici du `*texte italique*`</pre> | Voici du *italic text* |
| **Citations en bloc** | <pre>\> Kent.<br>\> Where's the king?<br>\> Gent.<br>\> Contending with the<br>\> fretful elements</pre> | > Kent.<br>> Where's the king?<br>> Gent.<br>> Contending with<br>> the fretful elements |
| **Liste** | <pre>\* Milk<br>\* Eggs<br>\* Beers<br>    \* Desperados<br>    \* Heineken<br>\* Ham</pre> | - Milk<br>- Eggs<br>- Beers<br>    - Desperados<br>    - Heineken<br>- Ham |
| **Liste ordonnée** | <pre>1\. Introduction<br>2\. Main topic<br>    1\. First sub-topic<br>    2\. Second sub-topic<br>3\. Conclusion</pre> | 1.  Introduction<br>2.  Main topic<br>    1.  First sub-topic<br>    2.  Second sub-topic<br>3.  Conclusion |
| **Ligne de code** | <pre>Ceci est  \`unpeudeJavaScript()\`</pre> | Ceci est `unpeudeJavaScript()` |
| **Block de code** | <pre>Voici un peu de code JavaScript:<br>```<br>function hello() {<br>    alert('hello');<br>}<br>```<br>Language is normally auto-detected,<br>but it can also be specified:<br>```sql<br>SELECT * FROM users;<br>DELETE FROM sessions;<br>```</pre> | Voici un peu de code JavaScript:<br><pre>function hello() {<br>    alert('hello');<br>}</pre><br>Language is normally auto-detected, but it can also be specified:<br><pre>SELECT * FROM users;<br>DELETE FROM sessions;</pre> |
| **Texte non formaté** | <pre>Retrait avec une tabulation ou 4 espaces <br>pour le texte non formaté. <br>    Ce texte ne sera pas formaté :<br>    Robert'); DROP TABLE students;--</pre> | Retrait avec une tabulation ou 4 espaces pour le texte non formaté.<br><pre>Ce texte ne sera pas formaté :<br>Robert'); DROP TABLE étudiants ;--</pre> |
| **Lien** | <pre>This is detected as a link:<br>`https://joplinapp.org`<br>And this is a link anchoring text content:<br>`[Joplin](https://joplinapp.org)`<br>And this is a link, with a title,<br>anchoring text content:<br>`[Joplin](https://joplinapp.org "Joplin project page")`</pre> | This is detected as a link:<br>https://joplinapp.org<br>And this is a link anchoring text content:<br>[Joplin](https://joplinapp.org)<br>And this is a link, with a title,<br>anchoring text content:<br>[Joplin](https://joplinapp.org "Joplin project page") (*hint: hover over the link*) |
| **Images** | ```<br>![Joplin icon](https://git.io/JenGk)<br>``` | ![Here's Joplin icon](https://git.io/JenGk) |
| **Règles horizontales** | <pre>One rule:<br>\*\*\*<br>Another rule:<br>\-\-\-</pre> | One rule:<br><br>* * *<br><br>Another rule:<br><br>* * * |
| **Tables** | [See below](#tables) |     |

### Tables

Les tableaux sont créés à l'aide de barres verticales `|` et de traits d'union  `-`. This is a Markdown table:

```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  | 
```

Qui est rendu comme suit :

| First Header | Second Header |
| --- | --- |
| Content Cell | Content Cell |
| Content Cell | Content Cell |

Notez qu'il doit y avoir au moins 3 tirets séparant chaque cellule d'en-tête.

Les deux-points peuvent être utilisés pour aligner les colonnes :

```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 | 
```

Qui est rendu comme suit :

| Tables | Are | Cool |
| --- | --- | --- |
| col 3 is | right-aligned | $1600 |
| col 2 is | centered | $12 |

## Suppléments Joplin

Outre la syntaxe Markdown standard, Joplin prend en charge plusieurs fonctionnalités supplémentaires.

### Liens vers d'autres notes

Vous pouvez créer un lien vers une note en spécifiant son ID dans l'URL. Par exemple:

```
[Link to my note](:/0b0d62d15e60409dac34f354b6e9e839) 
```

Étant donné que l'obtention de l'ID d'une note n'est pas simple, chaque application fournit un moyen de créer un tel lien. Dans l'**application de bureau**, faites glisser et déposez une note dans une autre note pour créer un lien. Ou faites un clic droit sur une note et sélectionnez "Copier le lien Markdown". Dans l'**application mobile**,  ouvrez une note et, dans le menu en haut à droite, sélectionnez "Copier le lien Markdown". Vous pouvez ensuite coller ce lien n'importe où dans une autre note.

### Notation mathématique

Des expressions mathématiques peuvent être ajoutées en utilisant la [notation KaTeX](https://khan.github.io/KaTeX/). Pour ajouter une équation en ligne, enveloppez l'expression dans `$EXPRESSION$`,  par exemple `$\sqrt{3x-1}+(1+x)^2$`. Pour créer un bloc d'expression, enveloppez-le comme suit :

```
$$
EXPRESSION
$$ 
```

Par exemple:

```
$$
f(x) = \int_{-\infty}^\infty
	\hat f(\xi)\,e^{2 \pi i \xi x}
	\,d\xi
$$ 
```

Voici un exemple avec le Markdown et le résultat rendu côte à côte :

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/Katex.png" height="345px" class="jop-noMdConv">

### Équations chimiques

Joplin prend en charge les équations chimiques via le plugin mhchem pour KaTeX. Ce plugin est automatiquement activé si vous activez la notation mathématique. Voir la [documentation mhchem](https://mhchem.github.io/MathJax-mhchem/) pour la syntaxe.

<img src="https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/Katex_mhchem.png" height="196px" class="jop-noMdConv">

### Diagrammes

Vous pouvez créer des diagrammes dans Joplin en utilisant la [syntaxe Mermaid](https://mermaidjs.github.io/). Pour ajouter un tel graphique, enveloppez le script Mermaid dans un bloc de code "```mermaid" comme ceci :

```
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
``` 
```

This is how it would look with the Markdown on the left, and rendered graph on the right:

![Mermaid support in Joplin](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/Mermaid.png)

Note that Mermaid graphs are always rendered on a white background regardless of the current theme. This is because they can contain various colours that may not be compatible with the current theme.

### Checkboxes

Checkboxes can be added like so:

```
- [ ] Milk
- [x] Rice
- [ ] Eggs 
```

Which would turn into:

![Checkbox support in Joplin](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/Markdown_checkbox.jpg)

The checkboxes can then be ticked in the mobile and desktop applications.

### HTML support

It is generally recommended to enter the notes as Markdown as it makes the notes easier to edit. However for cases where certain features aren't supported (such as strikethrough or to highlight text), you can also use HTML code directly. For example this would be a valid note:

```
This is <s>strikethrough text</s> mixed with regular **Markdown**. 
```

### Markdown Plugins

Joplin supports a number of plugins that can be toggled on/off to enable/disable markdown features on top of the standard Markdown features you would expect. These plugins are listed below. Unlike regular plugins, Markdown plugins must be enabled in the markdown section of the [Configuration screen](https://github.com/laurent22/joplin/blob/dev/readme/config_screen.md). Not all of the plugins are enabled by default, if the "enabled" field is 'no' below, then open the option screen to enable the plugin. Plugins can be disabled in the same manner.

The functionality added by these plugins is not part of the CommonMark spec so, while they will all work within Joplin, it is not guaranteed that they will work in other Markdown readers. Often this is not an issue but keep it in mind if you require compatibility with other Markdown applications.

| Plugin | Syntax | Description | Enabled | Screenshot |
| --- | --- | --- | --- | --- |
| Soft breaks | See [breaks](https://markdown-it.github.io/#md3=%7B%22source%22%3A%22This%20is%20line1%5CnThis%20is%20line2%5Cn%5CnThis%20is%20a%20line%20with%202%20trailing%20spaces%20%20%5CnNext%20line%5Cn%5CnClick%20the%20%60breaks%60%20checkbox%20above%20to%20see%20the%20difference.%5CnJoplin%27s%20default%20is%20hard%20breaks%20%28checked%20%60breaks%60%20checkbox%29.%22%2C%22defaults%22%3A%7B%22html%22%3Afalse%2C%22xhtmlOut%22%3Afalse%2C%22breaks%22%3Afalse%2C%22langPrefix%22%3A%22language-%22%2C%22linkify%22%3Afalse%2C%22typographer%22%3Afalse%2C%22_highlight%22%3Afalse%2C%22_strict%22%3Afalse%2C%22_view%22%3A%22html%22%7D%7D) markdown-it demo | Joplin uses hard breaks by default, which means that a line break is rendered as `<br>`. Enable soft breaks for traditional markdown line-break behaviour. | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/softbreaks_plugin.jpg) |
| Typographer | See [typographer](https://markdown-it.github.io/#md3=%7B%22source%22%3A%22%23%20Typographic%20replacements%5Cn%5Cn%28c%29%20%28C%29%20%28r%29%20%28R%29%20%28tm%29%20%28TM%29%20%28p%29%20%28P%29%20%2B-%5Cn%5Cntest..%20test...%20test.....%20test%3F.....%20test!....%5Cn%5Cn!!!!!!%20%3F%3F%3F%3F%20%2C%2C%20%20--%20---%5Cn%5Cn%5C%22Smartypants%2C%20double%20quotes%5C%22%20and%20%27single%20quotes%27%5Cn%22%2C%22defaults%22%3A%7B%22html%22%3Afalse%2C%22xhtmlOut%22%3Afalse%2C%22breaks%22%3Afalse%2C%22langPrefix%22%3A%22language-%22%2C%22linkify%22%3Atrue%2C%22typographer%22%3Atrue%2C%22_highlight%22%3Atrue%2C%22_strict%22%3Afalse%2C%22_view%22%3A%22html%22%7D%7D) markdown-it demo | Does typographic replacements, (c) -> © and so on | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/typographer_plugin.jpg) |
| Linkify | See [linkify](https://markdown-it.github.io/#md3=%7B%22source%22%3A%22Use%20the%20Linkify%20checkbox%20to%20switch%20link-detection%20on%20and%20off.%5Cn%5Cn%2A%2AThese%20links%20are%20auto-detected%3A%2A%2A%5Cn%5Cnhttps%3A%2F%2Fexample.com%5Cn%5Cnexample.com%5Cn%5Cntest%40example.com%5Cn%5Cn%2A%2AThese%20are%20always%20links%3A%2A%2A%5Cn%5Cn%5Blink%5D%28https%3A%2F%2Fjoplinapp.org%29%5Cn%5Cn%3Chttps%3A%2F%2Fexample.com%3E%22%2C%22defaults%22%3A%7B%22html%22%3Afalse%2C%22xhtmlOut%22%3Afalse%2C%22breaks%22%3Afalse%2C%22langPrefix%22%3A%22language-%22%2C%22linkify%22%3Atrue%2C%22typographer%22%3Atrue%2C%22_highlight%22%3Atrue%2C%22_strict%22%3Afalse%2C%22_view%22%3A%22html%22%7D%7D) markdown-it demo | Auto-detects URLs and convert them to clickable links | yes |     |
| [Katex](https://katex.org) | `$$math expr$$` or `$math$` | [See above](#math-notation) | yes | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/katex_plugin.jpg) |
| [Fountain](https://fountain.io) | ` ```fountain`<br>Your screenplay...<br>` ``` ` | Adds support for the Fountain markup language, a plain text markup language for screenwriting | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/fountain_plugin.jpg) |
| [Mermaid](https://mermaid-js.github.io/mermaid/) | ` ```mermaid`<br>mermaid syntax...<br>` ``` ` | See [plugin page](https://mermaid-js.github.io/mermaid/#/examples) for full description | yes | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/mermaid.jpg) |
| [Mark](https://github.com/markdown-it/markdown-it-mark) | `==marked==` | Transforms into `<mark>marked</mark>` (highlighted) | yes | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/mark_plugin.jpg) |
| [Footnote](https://github.com/markdown-it/markdown-it-footnote) | `Simples inline footnote ^[I'm inline!]` | See [plugin page](https://github.com/markdown-it/markdown-it-footnote) for full description | yes | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/footnote_plugin.jpg) |
| [TOC](https://github.com/nagaozen/markdown-it-toc-done-right) | Any of `${toc}, [[toc]], [toc], [[_toc_]]` | Adds a table of contents to the location of the toc page. Based on headings and sub-headings | yes | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/toc_plugin.jpg) |
| [Sub](https://github.com/markdown-it/markdown-it-sub) | `X~1~` | Transforms into X<sub>1</sub> | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/sub_plugin.jpg) |
| [Sup](https://github.com/markdown-it/markdown-it-sup) | `X^2^` | Transforms into X<sup>2</sup> | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/sup_plugin.jpg) |
| [Deflist](https://github.com/markdown-it/markdown-it-deflist) | See [pandoc](http://johnmacfarlane.net/pandoc/README.html#definition-lists) page for syntax | Adds the html `<dl>` tag accessible through markdown | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/deflist_plugin.jpg) |
| [Abbr](https://github.com/markdown-it/markdown-it-abbr) | *\[HTML\]: Hyper Text Markup Language<br>The HTML specification | Allows definition of abbreviations that can be hovered over later for a full expansion | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/abbr_plugin.jpg) |
| [Emoji](https://github.com/markdown-it/markdown-it-emoji) | `:smile:` | Transforms into 😄. See [this list](https://gist.github.com/rxaviers/7360908) for more emojis | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/emoji_plugin.jpg) |
| [Insert](https://github.com/markdown-it/markdown-it-ins) | `++inserted++` | Transforms into `<ins>inserted</ins>` (<ins>inserted</ins>) | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/insert_plugin.jpg) |
| [Multitable](https://github.com/RedBug312/markdown-it-multimd-table) | See [MultiMarkdown](https://fletcher.github.io/MultiMarkdown-6/syntax/tables.html) page | Adds more power and customization to markdown tables | no  | [View](https://raw.githubusercontent.com/laurent22/joplin/dev/Assets/WebsiteAssets/images/md_plugins/multitable_plugin.jpg) |