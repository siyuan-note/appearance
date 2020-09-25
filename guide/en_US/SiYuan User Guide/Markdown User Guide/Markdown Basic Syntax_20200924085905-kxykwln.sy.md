> This article mainly introduces the basic syntax of Markdown, please refer to ((20200924092619-pw51c0y "Markdown Extended Syntax")).
> The concise version of the grammar can be browsed ((20200924095356-cips1k6 "Markdown Cheat Sheet")).
> {: id="20200924091042-0j41250"}
{: id="20200924091042-770q9kw"}

## Overview
{: id="20200924091042-9a5k5yy"}

Almost all Markdown engines support the [Basic Syntax](https://daringfireball.net/projects/markdown/syntax) designed by Markdown inventor John Gruber, but different Markdown processing engines have slightly different performance details, as follows Introduce them one by one.
{: id="20200924091042-panvhfl"}

## Heading
{: id="20200924091042-kq7v0s8"}

To create a title, just start with the hash sign `#`, the number of hash signs corresponds to the level of the title. For example, if you want to create a `<h3>`, you can start with three `#`: `### Three-level heading `. The title syntax using hash marks is called "ATX title" in the [CommonMark Specification](https://spec.commonmark.org).
{: id="20200924091042-rluz9kj"}

| Markdown | HTML | Rendering results |
| - | - | - |
| `# Level 1 heading ` | `<h1>First-level heading</h1>` |  <h1>First-level heading</h1> |
| `## Level 2 heading ` | `<h2>Level 2 heading</h2>` |  <h2>Level 2 heading</h2> |
| `### Level 3 heading ` | `<h3>Level 3 heading</h3>` |  <h3>Level 3 heading</h3> |
| `#### Level 4 heading ` | `<h4>Level 4 heading</h4>` |  <h4>Level 4 heading</h4> |
| `###### Level 5 heading ` | `<h5>Level 5 heading</h5>` |  <h5>Level 5 heading</h5> |
| `####### Level 6 heading ` | ` <h6>Level 6 heading</h6>` |  <h6>Level 6 heading</h6> |
{: id="20200924091042-bk9cuv2"}

### Heading optional syntax
{: id="20200924090103-urqcxz4"}

In addition to using ATX headings, we can also use Setext headings: in the next line of the text, use one or more equal signs `=` to indicate the first-level heading, and one or more dashes `-` to indicate the second-level heading.
{: id="20200924091042-lmgjmlk"}

| Markdown | HTML | Rendering results |
| - | - | - |
| First-level heading<br>====== | `<h1>First-level heading</h1>` | hhh <h1>First-level heading</h1> |
| Secondary Title<br>------------ | `<h2>Secondary Title</h2>` | hhh <h2>Secondary Title</h2> |
{: id="20200924091042-3av0mkj"}

### Heading Best Practices
{: id="20200924091042-cvxjan2"}

1. ATX headings between paragraphs are best separated by blank lines. Because some Markdown engines do not recognize the title syntax that lacks leading and trailing blank lines.
   {: id="20200924090101-nzirqbk"}

   | ✅ Safe | ❌ Unsafe |
   | - | - |
   | This is a paragraph.<br /><br /># First level heading<br /><br />Another paragraph. | This is a paragraph.<br /># First level heading<br />Another paragraph |
   {: id="20200924090101-soe03ur"}
2. **Be sure to add a space after the hash sign of the ATX heading**
   {: id="20200924090101-yyq0rog"}

   | ✅ Safe | ❌ Unsafe |
   | - | - |
   | # First-level heading | # First-level heading |
   {: id="20200924090101-piclde2"}
3. Try not to use Setext grammar to write headings, because Setext grammar can only write to secondary headings
   {: id="20200924090101-9pp4qgo"}
{: id="20200924090157-wn4b0sv"}

## Paragraph
{: id="20200924091042-0u7guq6"}

Use blank lines to separate text.
{: id="20200924091042-i482ixl"}

| Markdown | HTML | Rendering results |
| - | - | - |
| I love using Markdown.<br /><br />I will use Markdown to typeset all my documents. | `<p>I like to use Markdown. `<br>`<p>I will use Markdown to typeset all my documents. </p>` | <p>I like to use Markdown.</p><p>I will use Markdown to typeset all my documents.</p> |
{: id="20200925105055-kwxoy3w"}

### Paragraph best practices
{: id="20200924090236-yo3e36z"}

1. Do not use spaces or tabs (`\t` is the Tab key) to indent the beginning of the paragraph, otherwise it may be rendered as a code block.
   {: id="20200924090224-qx8y5j4"}

   | ✅ Safe | ❌ Unsafe |
   | - | - |
   | Do not indent the beginning.<br><br>Just keep the left alignment like this. | The beginning indentation may be rendered as a code block. |
   {: id="20200924090224-wsyuuyh"}
{: id="20200924090334-2falxhs"}

2. In traditional Chinese typesetting, there is a habit of "blank two spaces" at the beginning of a paragraph. You can use full-width spaces `　` or HTML entities `&emsp;`. It is recommended not to leave two spaces in the layout of articles in the field of science and technology.
{: id="20200924090224-4olt2y3"}

## Break
{: id="20200924090424-ngsc0qd"}

If you need to wrap the text `<br>`, you can add two or more spaces at the end of the text and press Enter.
{: id="20200924090424-te2girz"}

| Markdown | HTML | Rendering results |
| - | - | - |
| This is the first line.<br>This is the second line. | `<p>This is the first line. <br>This is the second line. </p>` | This is the first line.<br>This is the second line. |
{: id="20200924091042-gcbi7wr"}

### Best Practices for Breaking Lines
{: id="20200924091042-2mftqpg"}

At present, most Markdown engines will automatically convert the newline character `\n` to `<br>`, that is, soft line feed to hard line feed. So although it is safe to write two or more spaces at the end, it may also cause some minor problems: the trailing space is not visible in some editors; accidentally or habitually pressing it will cause wrong layout. Because of these minor problems, it may be the safest way to use `<br>` to wrap lines, but it is not very elegant. In addition, in the CommonMark specification, you can use a backslash `\` at the end of the text to break lines, but I don't recommend this way of writing.
{: id="20200924091042-991yjkx"}

In summary, my suggestion is to **do not use trailing spaces, `\` or `<br>`**, because almost all Markdown engines now basically support soft line breaks to hard line breaks.
{: id="20200924091042-usvyt5g"}

## Bold and emphasize
{: id="20200924091042-3kumpp2"}

Bold corresponds to bold, and emphasis corresponds to italics.
{: id="20200924091042-hsx8nks"}

### Bold
{: id="20200924091042-mdszhtg"}

To bold text, you can use two asterisks `**` or two underscores `__` to wrap the text to be bolded.
{: id="20200924091042-5zi0fgm"}

| Markdown | HTML | Rendering results |
| - | - | - |
| Bold the text\*\*Bold\*\*A click | `Bold the text <strong>Bold</strong> once` | Make the text<strong>Bold</strong> once |
| Make the text\_\_ bold\_\_ once | `Make the text <strong>bold</strong> once` | Make the text<strong> bold </strong> once |
{: id="20200924091042-53t5fn3"}

#### Bold best practice
{: id="20200924091042-ujmvh2b"}

The difference between using asterisks for bold and underscores is that spaces can be added before and after the asterisk, but underscores must be added.
{: id="20200924091042-a8xeycr"}

| ✅ Safe | ❌ Unsafe |
| - | - |
| `Asterisk **Bold** No spaces required` | `No spaces underscore __Bold__ invalid` |
{: id="20200924091042-j5bfcuy"}

### Emphasize
{: id="20200924091042-q0ulnhn"}

To emphasize text, you can use an asterisk `*` or an underscore `_` to wrap the text to be emphasized.
{: id="20200924091042-wnc5bfl"}

| Markdown | HTML | Rendering results |
| - | - | - |
| Put the text\*emphasized\* once | `<em>emphasize the text</em> once` | <em>emphasize the text</em> once |
| Put the text\_emphasized\_ once | `<em>emphasize the text</em> once` | <em>emphasize</em> the text once |
{: id="20200924091042-ipp5oiw"}

#### Emphasize best practices
{: id="20200924091042-7u9x86z"}

Similar to bold, spaces can be used before and after the asterisk, but the underscore must be added.
{: id="20200924091042-r4pdy9b"}

| ✅ Safe | ❌ Unsafe |
| - | - |
| `asterisk *emphasis*no space required` | `no space underscore_emphasis_invalid` |
{: id="20200924091042-rzty4kv"}

### Bold and emphasize
{: id="20200924091042-y09v136"}

If you need to emphasize the text while bolding it, you can use three asterisks `***` or three underscores `___` to wrap the text to be emphasized.
{: id="20200924091042-evkszil"}

| Markdown | HTML | Rendering results |
| - | - | - |
| Example of***bolding and emphasizing*** at the same time | `Example of <strong><em>bolding and emphasizing at the same time</em></strong>` | At the same time<strong><em>bolding and emphasizing </em></strong> Examples |
| Example of bolding and emphasizing ___ at the same time | `Example of <strong><em>bolding and emphasizing at the same time</em></strong> at the same time` | <strong><em>Bolding and emphasizing at the same time</em></strong> example |
| At the same time__*Bold and emphasized*__ example | `At the same time <strong><em>Bold and emphasized</em></strong> example` | At the same time<strong><em>Bold and emphasized</em></strong> example |
| At the same time**_Bold and emphasized_** example | `At the same time <strong><em>Bold and emphasized</em></strong> example` | At the same time<strong><em>Bold and emphasized</em></strong> Examples |
| Asterisk***can be omitted*** plus space | `Asterisk<strong><em>can be omitted</em></strong>Add space` | Asterisk<strong><em>can be omitted</em ></strong>Add space |
{: id="20200924091042-jz9pb53"}

## Block Quote
{: id="20200924091042-1prq0qw"}

To create a block quote `<blockquote>`, just add a greater than sign `>` before the paragraph.
{: id="20200924091042-hc2ogzi"}

```markdown
> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me
```
{: id="20200924091042-zuwv71z"}

Rendering result
{: id="20200924091042-2lkitba"}

> Forgive me for the uninhibited indulgence of love and freedom in my life, and I will be afraid of falling down
> Abandoned ideals, anyone can
> Even if one day only you and me
> {: id="20200924091042-7lfxb7n"}
{: id="20200924091042-9w97cj5"}

### Segment within block quote
{: id="20200924091042-fxsvmhr"}

If you need to segment, you can add a `>` before the blank line of the segment.
{: id="20200924091042-458n7ec"}

```markdown
> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me
```
{: id="20200924091042-87kwdrb"}

Rendering result:
{: id="20200924091042-i9oot3f"}

> Today I watched the snow drifting by in the cold night
> Floating far away with a cold heart
> {: id="20200924091042-e3yw28j"}
>
> Chasing in the wind and rain, but in the fog
> The sky is broad for you and me
> {: id="20200924091042-h62adzh"}
{: id="20200924091042-cojkqd9"}

### Nested block quotes
{: id="20200924091042-8ze0329"}

Block quotes can be nested, adding two greater than signs `>>` before the paragraph to indicate two levels of nesting.
{: id="20200924091042-2oc9djg"}

```markdown
> Block quoted paragraph
>
>> Nested block quotes
```
{: id="20200924091042-bqaq0gl"}

### Block quote contains other elements
{: id="20200924091042-sl0z99l"}

Block quotes can contain most other syntax elements. The CommonMark specification defines a block reference as a container block. The container block can contain any block-level element and row-level element, which means that a block reference can contain any other elements.
{: id="20200924091042-r59e1lt"}

```markdown
> ### The heading is a leaf block element
>
> * List item one is a container block element
> * List item two is also a container block element
>
> **Bold** and *Emphasis* are row-level elements.
```
{: id="20200924091042-r99eutl"}

Rendering result:
{: id="20200924091042-63tio8z"}

> ### The heading is a leaf block element
> {: id="20200925105404-qupomot"}
>
> * List item one is a container block element
> * List item two is also a container block element
> {: id="20200924091042-f79mdfi"}
>
> **Bold** and *Emphasis* are row-level elements.
> {: id="20200924091042-2w7us56"}
{: id="20200924091042-ew9yehm"}

## List
{: id="20200924091042-h23ohte"}

The list is divided into an ordered list and an unordered list. Lists in Markdown can only contain list item elements. List items, like block references, are container blocks. In other words, list items can contain any other elements.
{: id="20200924091042-i92uan0"}

### Ordered List
{: id="20200924091042-dyoelm1"}

An ordered list can be created by using Arabic numerals followed by `.` or `)`, and the numbers do not have to be consecutively incremented.
{: id="20200924091042-u75sica"}

| Markdown | HTML |
| - | - |
| 1. List item one<br>2. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| 1. List item one<br>1. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
| 1. List item one<br>3. List item two<br> | `<ol><li>List item one</li><li>List item two</li></ol>` |
{: id="20200924091014-zj5k9sl"}

### Unordered List
{: id="20200924091014-3lte16t"}

Unordered lists can start with a dash `-`, an asterisk `*`, or a plus sign `+`, followed by a space to separate the text content.
{: id="20200924091042-zclcdan"}

| Markdown | HTML |
| - | - |
| -List item one<br>- List item two<br> | `<ul><li>List item one</li><li>List item two</li></ul>` |
| * List item one<br>* List item two<br> | `<ul><li>List item one</li><li>List item two</li></ul>` |
| + List item one<br>+ List item two<br> | `<ul><li>List item one</li><li>List item two</li></ul>` |
{: id="20200924091042-840ue8k"}

### List item contains other elements
{: id="20200924091042-niawfoz"}

List items can contain any other elements, such as paragraphs, block quotes, code blocks, pictures, etc. The point of use is that the starting character of the element to be included should be "aligned" with the starting content of the list item.
{: id="20200924091042-q6inesf"}

#### List item contains paragraph
{: id="20200924091042-jrl42af"}

```markdown
* List item one
* The first paragraph of list item two
  
  This is the second paragraph
* List item three
```
{: id="20200924091042-346iykk"}

Rendering result:
{: id="20200924091042-rut2z7v"}

* List item one
  {: id="20200924091042-1e1gbti"}
* The first paragraph of list item two
  {: id="20200924091042-t78w6y8"}

  This is the second paragraph
  {: id="20200924091042-yu2yapv"}
* List item three
  {: id="20200924091042-dqhfscu"}
{: id="20200924091042-0uziw1g"}

#### List item contains block quote
{: id="20200924091042-6a1qtk0"}

```markdown
* List item one
* The first paragraph of list item two
  
  > The second paragraph is a block quote
* List item three
```
{: id="20200924091042-3qsuynh"}

Rendering result:
{: id="20200924091042-4yqbp6i"}

* List item one
* The first paragraph of list item two
  > The second paragraph is a block quote
  > {: id="20200924091042-jtqghup"}
  >
  {: id="20200924091042-mtlr1rq"}
* List item three
{: id="20200924091042-minv0sg"}

#### List item contains code block
{: id="20200924091042-izfh8ho"}

````markdown
* List item one
* The first paragraph of list item two
  
   ```
  Here is the code block
  echo Hello, world!
   ```
* List item three
````
{: id="20200924091042-ajtr3l4"}

Rendering result:
{: id="20200924091042-8pww8q0"}

* List item one
* The first paragraph of list item two
  ```
  Here is the code block
  echo Hello, world!
  ```
  {: id="20200924091042-wjbf2oz"}
* List item three
{: id="20200924091042-0hb5fih"}

#### List item contains pictures
{: id="20200924091042-evw0ef6"}

````markdown
* List item one
* The first paragraph of list item two
  
  ![B3log](https://static.b3log.org/images/brand/b3log-128.png "B3log Open Source Community")
* List item three
````
{: id="20200924091042-t4ck0a6"}

Rendering result:
{: id="20200924091042-mhi1qfm"}

* List item one
  {: id="20200924091042-krxzcca"}
* The first paragraph of list item two
  {: id="20200924091042-4afcsqd"}

  ![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)
  {: id="20200924091042-6898y99"}
* List item three
  {: id="20200924091042-ty9kn9y"}
{: id="20200924091042-obb4y52"}

## Code
{: id="20200924091042-32ok284"}

The code can be wrapped with backticks span</code>.
{: id="20200924091042-gemc2y3"}

| Markdown | HTML | Rendering results |
| - | - | - |
| The command to list files is\`ls\` | The command to list files isspan</code>` | The command to list files is span</code> |
{: id="20200924091042-p68o0c7"}

### Escaping backticks
{: id="20200924091042-u84ke19"}

If you need to display the backquote, you can use the escape character `\` to escape the backquote.
{: id="20200924091042-g1bh29q"}

| Markdown | HTML | Rendering results |
| - | - | - |
| Type a backtick\` | span</code> | Type a backtick ` |
{: id="20200924091042-5swzo8j"}

### Code block
{: id="20200924091042-cg3fg52"}

Code blocks can be indented with four spaces or tabs `\t`.
{: id="20200924091042-u13ryt4"}

```markdown
    <html>
      <head>
      </head>
    </html>
```
{: id="20200924091042-rgum1um"}

Rendering result:
{: id="20200924091042-99jqkib"}

```
<html>
  <head>
  </head>
</html>
```
{: id="20200924091042-napcoci"}

**It is recommended to use fence code block syntax to typeset code blocks**, that is, use span</code> to wrap the code block and specify the syntax highlighting language:
{: id="20200924091042-ekbxxkj"}

````markdown
```html
<html>
  <head>
  </head>
</html>
```
````
{: id="20200924091042-1ht4p64"}

## Thematic breaks
{: id="20200924091042-rac4qvd"}

Create a dividing line with three or more asterisks `***`, dashes `---`, or underscores `___`.
{: id="20200924091042-rpfvtr4"}

```markdown
***
---
___
```
{: id="20200924091042-cfnbyiu"}

Rendering result:
{: id="20200924091042-5y6i9iu"}

---

## Hyperlink
{: id="20200924092215-9pndcwq"}

Create a hyperlink by `[link text](URL)`.
{: id="20200924092215-cpuukj4"}

```markdown
We are from the niche open source community [B3log](https://b3log.org).
```
{: id="20200924092215-sfulk4s"}

Rendering result:
{: id="20200924092215-f3k04kj"}

We are from the niche open source community [B3log](https://b3log.org).
{: id="20200924092215-j6gqv7o"}

### Add hyperlink title
{: id="20200924092215-pxt6cb0"}

The link title is optional and is enclosed in double quotes after the URL in parentheses. When the mouse is moved over the hyperlink, the title content will appear.
{: id="20200924092215-s9of48i"}

```markdown
We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").
```
{: id="20200924092215-d96gph9"}

Rendering result:
{: id="20200924092215-tbvjdi9"}

We come from the niche open source community [B3log](https://b3log.org "B3log Open Source").
{: id="20200924092215-kbfw3q5"}

### URL and email address
{: id="20200924092215-cssvfjt"}

If you want to display the URL or email address directly, you can use `<` and `>` to wrap the URL or email address.
{: id="20200924092215-j73e4j7"}

```markdown
<https://b3log.org>

<os@b3log.org>
```
{: id="20200924092215-w7m08zj"}

Most Markdown engines also support automatic conversion, so you can omit `<>`:
{: id="20200924092215-bvqd5kk"}

```markdown
https://b3log.org

os@b3log.org
```
{: id="20200924092215-po08iwz"}

### Hyperlink format layout
{: id="20200924092215-0all5ae"}

Hyperlinks can be used together with element structures such as bold emphasis, code, etc.
{: id="20200924092215-00mwgxm"}

```markdown
We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).
```
{: id="20200924092215-9zk1e1h"}

Rendering result:
{: id="20200924092215-ax5thny"}

We are from the niche open source community **[B3log](https://b3log.org)**.
We are from the niche open source community [`B3log`](https://b3log.org).
{: id="20200924092215-ild4jt5"}

### Quote style hyperlink
{: id="20200924092215-8xii4c2"}

Use citation style hyperlinks to make the original Markdown easier to read. The citation style hyperlink is divided into two parts: link reference and link definition.
{: id="20200924092215-vrn7e7o"}

#### Link reference
{: id="20200924092215-h152xry"}

A link reference is used where a hyperlink needs to be inserted. It consists of two sets of square brackets. The first set of square brackets is used to specify the link text, the second set of square brackets is used to specify the link identifier, and the link identifier points to the link definition.
{: id="20200924092215-aglg7p1"}

```markdown
[Link text][Label]

[Label]: https://b3log.org
```
{: id="20200924092215-2iay1tm"}

Rendering result:
{: id="20200924092215-q56zoj0"}

[Link text][link logo][https://b3log.org](https://b3log.org)
{: id="20200924092215-ia7z62o"}

The link reference can also consist of only a set of square brackets, in which case the link identifier will be used for the link text.
{: id="20200924092215-ssudlcp"}

```markdown
[Link ID]

[Link ID]: https://b3log.org
```
{: id="20200924092215-qy2d38y"}

Rendering result:
{: id="20200924092215-zcs67e7"}

[Link ID][https://b3log.org](https://b3log.org)
{: id="20200924092215-ume7gag"}

#### Link definition
{: id="20200924092215-fzvkpfb"}

The link definition consists of three parts:
{: id="20200924092215-klk06rx"}

1. Square brackets wrap to define the link identifier, followed by a colon `:`
2. URL can be written directly or wrapped in angle brackets `<>`
3. Link title, this part is optional and can be wrapped in double quotes, single quotes or parentheses
{: id="20200924092215-hqt9ncw"}

```markdown
[Link ID]: https://b3log.org
[Link ID]: <https://b3log.org>
[Link logo]: https://b3log.org "B3log open source"
[Link logo]: https://b3log.org'B3log open source'
[Link logo]: https://b3log.org (B3log open source)
```
{: id="20200924092215-54k949g"}

The link definition can be placed anywhere in the entire Markdown text. Some people are accustomed to putting it after the quoted paragraph, and some people are accustomed to putting it at the end of the text.
{: id="20200924092215-unwddep"}

### Hyperlink Best Practice
{: id="20200924092215-t4e0w5s"}

The English content is naturally separated by spaces, so there is no separation problem when using automatic hyperlinks. But Chinese will have this problem, such as:
{: id="20200924092215-rbancf3"}

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```
{: id="20200924092215-erpnkib"}

This content will render incorrectly on many Markdown engines. In order to ensure compatibility as much as possible, consider using spaces to separate:
{: id="20200924092215-jl53ldb"}

```markdown
Our website is https://b3log.org. Open source enthusiasts are welcome to join!
```
{: id="20200924092215-3iwrn5l"}

Or use angle brackets `<>` to wrap:
{: id="20200924092215-6xq0fp5"}

```markdown
Our website is <https://b3log.org> Open source enthusiasts are welcome to join!
```
{: id="20200924092215-cn1vsuo"}

So you can get the expected rendering result:
{: id="20200924092215-c7v3ram"}

Our website is [https://b3log.org](https://b3log.org) Open source enthusiasts are welcome to join!
{: id="20200924092215-uqyxpm8"}

## Picture
{: id="20200924092215-iv1xlia"}

Use the exclamation mark `!` followed by a hyperlink to render the image.
{: id="20200924092215-2pazqq3"}

```markdown
![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)
```
{: id="20200924092215-yel5nzg"}

Rendering result:
{: id="20200924092215-p4ixkhl"}

![B3log Logo](https://static.b3log.org/images/brand/b3log-128.png)
{: id="20200924092215-ulj4q4n"}

### Hyperlink nested image
{: id="20200924092215-29fro5e"}

If you need to click on the picture to jump to the hyperlink, you only need to include the picture in the text part of the link.
{: id="20200924092215-x84srik"}

```markdown
[![LianDi](https://static.b3log.org/images/brand/hacpai-128.png)](https://ld246.com)
```
{: id="20200924092146-x0nwlxg"}

Rendering result:
{: id="20200924092146-2ym0f93"}

[![LianDi](https://static.b3log.org/images/brand/hacpai-128.png)](https://ld246.com)
{: id="20200924092156-efgdunm"}

## Escape character
{: id="20200924092215-gp1cf77"}

You can use the backslash `\` to escape the following characters:
{: id="20200924092215-b6ypa8v"}

| Characters | Chinese name |
| - | - |
| `\` | Backslash |
| span</code> | backtick |
| `*` | Asterisk |
| `_` | Underscore |
| `{}` | curly braces |
| `[]` | Square brackets |
| `()` | Parentheses |
| `#` | hashtag |
| `+` | plus sign |
| `-` | dash (minus sign) |
| `.` | Point |
| `!` | Exclamation mark |
| span</code> | Vertical bar (pipe symbol) |
{: id="20200924092215-d8kgojt"}

Almost all ASCII punctuation marks can be escaped with backslashes.
{: id="20200924092215-pmad714"}

## Embed HTML
{: id="20200924092215-65471eb"}

Markdown naturally supports embedding HTML code.
{: id="20200924092215-0x1mrcf"}

```markdown
**Markdown** and <em>HTML</em> mixed typesetting.
```
{: id="20200924092215-hq98bra"}

Rendering result:
{: id="20200924092215-bmahzfe"}

**Markdown** and <em>HTML</em> mixed typesetting.
{: id="20200924092215-37weit8"}

### Embedding HTML Best Practices
{: id="20200924092215-c1z8tr5"}

This is useful when you need to set the image size and font color, but we don’t recommend using HTML too much for typesetting, because this is actually not universal, because some Markdown engines filter some parts for security reasons Labels or attributes; secondly, because it is too Markdown!
{: id="20200924092215-zciwoaj"}

Also, don’t embed Markdown in HTML, it won’t work:
{: id="20200924092215-1567enj"}

```markdown
<p>**Bold** will not take effect. </p>
```
{: id="20200924092215-q9m9zoi"}

Rendering result:
{: id="20200924092215-pee2hpb"}

<p>**Bold** will not take effect. </p>

## Summary
{: id="20200924092211-ouqz7eb"}

Good use of blank lines and spaces is the key to Markdown typesetting. In many cases, it is because of missing blank lines or spaces that unexpected rendering results are produced.
{: id="20200924092211-zx5keii"}

With the improvement of the CommonMark/GFM specification and gradually becoming the industry's unified Markdown standard, more and more Markdown engines have implemented the specification. It is recommended that Markdown users should follow the specifications as much as possible for typesetting, so as to avoid detail rendering problems to the greatest extent.
{: id="20200924092215-ckfvj7c"}

## Reference
{: id="20200924092215-zv9fcc1"}

* [Markdown Guide](https://www.markdownguide.org)
* [CommonMark Spec](https://spec.commonmark.org)
{: id="20200924092215-w8nzlj4"}

[Link ID]: https://b3log.org
