> This article mainly introduces the extended syntax of Markdown, please refer to ((20200924085905-kxykwln "Markdown Basic Syntax")).
> The concise version of the grammar can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).
> {: id="20200924093226-mj73gxz"}
{: id="20200924093226-yz1558l"}

## Overview
{: id="20200924093226-9fyk3r9"}

In [Basic Grammar](https://ld246.com/article/1583129520165), we introduced the most commonly used typesetting usage of Markdown, but sometimes the basic grammar is not enough to meet the more complex typesetting needs, then you need to use the extended grammar Up.
{: id="20200924093226-6iiczak"}

Some individuals and organizations have extended the basic grammar, such as the introduction of tables, fenced code blocks, code highlighting, automatic links, footnotes and directories, etc. These extended grammars require specific Markdown engines to support.
{: id="20200924093226-8ylqvo2"}

## Availability
{: id="20200924093226-fluizf1"}

Not all Markdown engines support the extended syntax, so before using the extended syntax, you may need to confirm the specific Markdown engine support, and browse their usage documents to understand which elements can be supported.
{: id="20200924093226-q011tqu"}

### Mainstream Markdown grammar specifications
{: id="20200924093226-0qfgfg8"}

Markdown grammar specifications have not yet formed a standard. The following grammar specifications are more mainstream.
{: id="20200924093226-0tzsuwr"}

* [CommonMark](https://commonmark.org)
* [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm)
* [Markdown Extra](https://michelf.ca/projects/php-markdown/extra)
* [MultiMarkdown](https://fletcherpenney.net/multimarkdown)
* [R Markdown](https://rmarkdown.rstudio.com)
{: id="20200924093226-nsl9adc"}

Among them, CommonMark and GFM are currently the most likely to be standardized. GFM is an extension of GitHub based on CommonMark. It is almost a de facto standard. For the interpretation of CommonMark specifications, please refer to [here](https://ld246.com/article/1566893557720).
{: id="20200924093226-xyqr443"}

### Markdown engine
{: id="20200924093226-xc00wtu"}

[Here](https://github.com/markdown/markdown.github.com/wiki/Implementations) lists a lot of Markdown engine implementations, most of them support extended syntax by setting switches, the specific details Please refer to their documentation.
{: id="20200924093226-rwco9va"}

## Form
{: id="20200924093226-gekpd8y"}

Use dash `---` to separate the header and body of the table, and use the vertical bar `|` to separate the columns. The vertical bars at the beginning and end of each row are optional.
{: id="20200924093226-gtmhpv1"}

```markdown
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```
{: id="20200924093226-vyx356g"}

Rendering result:
{: id="20200924093226-1l2lavn"}

| Syntax | Description |
| - | - |
| Header | Title |
| Paragraph | Text |
{: id="20200924093226-aph1rts"}

Each column does not have to be aligned, the following example can also be rendered:
{: id="20200924093226-vxi37kk"}

```markdown
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```
{: id="20200924093226-frewwb1"}

### Table alignment
{: id="20200924093226-66bjgn2"}

If you need to align the table content to the left, center or right, you can add a colon `:` to `---`. The colon only appears on the left to indicate left alignment, on both sides indicates center alignment, and only on the right indicates right alignment.
{: id="20200924093226-q56ywe0"}

```markdown
| Syntax | Description | Test Text |
| :--- | :----: | ---: |
| Header | Title | Here's this |
| Paragraph | Text | And more |
```
{: id="20200924093226-yjypekh"}

Rendering result:
{: id="20200924093226-wmf3uoh"}

| Syntax | Description | Test Text |
| :- | :-: | -: |
| Header | Title | Here's this |
| Paragraph | Text | And more |
{: id="20200924093226-fktsia6"}

### Table content layout
{: id="20200924093226-t20l6gd"}

The content in the table can also be typeset, such as bolding, emphasizing text, inserting hyperlinks, etc. However, it is limited to the use of "span-level elements" for typesetting, and "block-level elements" cannot be used, such as headings, block quotes, lists, dividers, etc.
{: id="20200924093226-5ouu9cj"}

### Table content escape vertical bar
{: id="20200924093226-pqkgtwe"}

If you need to use the vertical bar `|` in the table content, you need to escape it. You can use `\|` to escape, but it is safer to write a vertical line HTML entity to represent `&#124;`, because some Markdown engines can’t handle the `\|` in the table content correctly.
{: id="20200924092723-pcxc6wb"}

## Fence code block
{: id="20200924092723-e8kycrw"}

In [Basic Syntax](https://ld246.com/article/1583129520165), we introduced that code blocks can be typeset by indentation with four spaces or tabs `\t`. But we recommend using the fenced code block syntax, that is, use three or more backquotes span</code> or three or more squiggles `~~~` to wrap the code block content:
{: id="20200924093226-r8hp23e"}

````markdown
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
{: id="20200924093226-7binzak"}

Rendering result:
{: id="20200924093226-vfpteo3"}

```text
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
{: id="20200924093226-s5xwore"}

If you need to display the original Markdown of the code block (like the example shown above), you can start with a larger number of backticks at the outermost layer, and the number of closed backticks is equal to the number at the beginning.
{: id="20200924093226-kdga1ty"}

``````markdown
````
```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
``````
{: id="20200924093226-i9w191z"}

### Code block syntax highlighting
{: id="20200924093226-9dalewm"}

The syntax highlighting of code blocks requires the support of the Markdown engine, and is typeset by adding the name of the programming language after the opening backquote.
{: id="20200924093226-uu1sf1d"}

````markdown
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
````
{: id="20200924093226-teyo1ft"}

Rendering result:
{: id="20200924093226-mib9zio"}

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
{: id="20200924093226-pfa7w4z"}

## Footnotes
{: id="20200924093226-v29y2yx"}

Footnotes are used to add details or references at the end of the text, so that the body of the article will look more concise and clear. After creating a footnote, a superscript number link will appear in the text where the footnote is quoted, and the reader will jump to the corresponding position defined by the footnote at the end of the text after clicking.
{: id="20200924093226-rb4q9xq"}

Footnote quotes are created by `[^identifier]`. The identifier part can be numbers or text, but cannot contain spaces or tabs. Identifiers are only used for associative references and definitions. When rendering, they will automatically be rendered in increasing numbers according to the order of the footnote definition. But this is not absolute, some Markdown engines also use the identifier part for rendering.
{: id="20200924093226-8yodwab"}

The footnote definition is created using `[^identifier]:`, and the detailed description or reference that needs to be added is after the colon. The footnote definition does not have to be placed at the end of the entire Markdown text, it can also work if it is sandwiched between paragraphs, lists, or block quotes.
{: id="20200924093226-1nqplp0"}

```markdown
Here is a footnote reference [^1], and here is another footnote reference [^bignote].

[^1]: The first footnote definition.
[^bignote]: The footnote definition can use multiple paragraphs.

    Indented paragraphs are included in this footnote definition.

    ```
    You can use code blocks.
    ```

    There are other line-level typesetting syntaxes, such as **bold** and [link](https://b3log.org).
```
{: id="20200924093226-nyy6l6j"}

## Heading designation ID {#heading-ids}
{: id="20200924093226-umai6b1"}

Some Markdown engines support specifying an ID for the title, while others automatically add an ID. The function of the title ID is to allow other places to jump directly to the title through the anchor point. The syntax of title designation ID is to wrap the ID in curly braces after the title.
{: id="20200924093226-omcr066"}

```markdown
### This is a title {#custom-id}
```
{: id="20200924093226-o1s5i5f"}

Rendered HTML:
{: id="20200924093226-346iwyn"}

```html
<h3 id="custom-id">This is a headline</h3>
```
{: id="20200924093226-d3wahe5"}

### Link to the specified heading
{: id="20200924093226-3df5hxf"}

You can link to the title in the text through the hyperlink syntax.
{: id="20200924093226-0x7sp8s"}

| Markdown | HTML | Rendering results |
| - | - | - |
| `[Heading Designation ID](#heading-ids)` | `<a href="#heading-ids">Heading Designation ID</a>` | [Heading Designation ID](%5Bhttps://ld246.com/%5D(https://ld246.com/)) article/1583305480675#heading-ids) |
{: id="20200924093226-wd3wfhr"}

If you need to link to the title of another page, you need to write the full link path, such as `[title designation ID](https://ld246.com/article/1583305480675#heading-ids)`.
{: id="20200924093226-6govomu"}

## Strikethrough
{: id="20200924093226-nsy030s"}

The text can be crossed out with a strikethrough, and the result will be typeset~just like this~. To create a strikethrough, you can wrap the text to be deleted with one `~` or two wavy lines `~~`.
{: id="20200924093226-i014yvy"}

```
~~ The earth is flat. ~~ Now we know that the earth is round.
```
{: id="20200924093226-trvaade"}

Rendering result:
{: id="20200924093226-7b5rmod"}

~~ The earth is flat. ~~ Now we know that the earth is round.
{: id="20200924093226-jpjvwm2"}

## task list
{: id="20200924093226-8a6591w"}

Render task list items by adding `[ ]` or `[x]` to ordinary list items.
{: id="20200924093226-riap7j2"}

```markdown
-[x] To-do one
-[] To-do list two
-[] To-do list three
```
{: id="20200924093226-1keur89"}

Rendering result:
{: id="20200924093226-c7rmtah"}

-[X] To-do one
-[] To-do list two
-[] To-do list three
{: id="20200924093226-x73kzzo"}

## Emoji
{: id="20200924093226-jju0tre"}

There are two ways to use Emoji: directly input Emoji characters or use the alias `:smile:`. For direct input, you need to make sure that the current editor uses UTF-8 encoding.
{: id="20200924093226-qwdvpnz"}

```markdown
The weather is really nice today :sunny:
Flower 🌻 smile at me
```
{: id="20200924093226-7b1kg7w"}

Rendering result:
{: id="20200924093226-csnaqjp"}

The weather is really nice today ☀️
Flower 🌻 smile at me
{: id="20200924093226-uhre4fl"}

## Prohibit automatic linking
{: id="20200924093226-hild6k0"}

Most Markdown engines enable automatic linking by default, so when we want to render a link as plain text, we need to turn it into code:
{: id="20200924093226-fhz3zdi"}

```markdown
`https://b3log.org`
```
{: id="20200924093226-lswowo1"}

Rendering result:
{: id="20200924093226-3plpwsd"}

`https://b3log.org`
{: id="20200924093226-b9l7xiu"}

## to sum up
{: id="20200924093226-g4uaka8"}

Try to use only the extended syntax defined by GFM, so that you can maximize the support of many Markdown engines and get consistent rendering results.
{: id="20200924093226-0dlm0yd"}

## Reference
{: id="20200924093226-lxgn0gp"}

* [Markdown Guide](https://www.markdownguide.org)
* [CommonMark Spec](https://spec.commonmark.org)
{: id="20200924093154-lzvrgdc"}
