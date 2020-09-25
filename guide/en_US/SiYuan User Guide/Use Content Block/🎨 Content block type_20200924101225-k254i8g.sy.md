## Content Block type cheatsheet
{: id="20200925102606-ie96t5e"}

Hover the mouse over the content block and the corresponding icon will appear on the left side of the content block. For format usage, please refer to ((20200924093441-ft2rhps "Markdown Complete Demo")).
{: id="20200925102708-sxalcrw"}

| Icon | Type | ((20200925102736-x94e40g "Meta Type")) |
| - | - | - |
| ![paragraph](assets/paragraph.svg) | Paragraph block | Leaf block |
| ![heading](assets/heading.svg) | Heading block | Leaf block |
| ![math-block](assets/math-block.svg) | Math Formula Block | Leaf Block |
| ![math-block](assets/code-block.svg) | Code block | Leaf block |
| ![math-block](assets/unordered-list.svg) | Unordered List Block | Container block |
| ![math-block](assets/ordered-list.svg) | Ordered List Block | Container block |
| ![math-block](assets/task-list.svg) | To-do list block | Container block |
| ![math-block](assets/table.svg) | Table block | Leaf block |
| ![math-block](assets/blockquote.svg) | Blockquote block | Container block |
| ![doc](assets/doc.svg) | Document block | Container block |
{: id="20200925102648-puujfp0"}

## Details of content block types
{: id="20200925102648-s2y9w9j"}

Below we introduce the details of these content block types.
{: id="20200925103337-6s3lq6k"}

### Paragraph block
{: id="20200925103337-sk88gul"}

![paragraph](assets/paragraph.svg)
{: id="20200925103337-di3y3oo"}

Here is a sample paragraph.
{: id="20200925103337-f9q0rgh"}

Press Enter directly after a paragraph to form a new paragraph.
{: id="20200925103337-rq4eka2"}

### Heading block
{: id="20200925103001-xh7gcj6"}

![heading](assets/heading.svg)
{: id="20200925103001-9eog2ws"}

The above is the heading block, which supports level one to six.
{: id="20200925103033-wuq1pyh"}

When using ((20200924101312-jj4e0v3 "Content block reference")) or ((20200924101312-385dey5 "embedding")), related content blocks under the title block will be automatically aggregated according to the heading level.
{: id="20200925103043-xhbrr8k"}

### Mathematical formula block
{: id="20200925103337-lr0uj2a"}

![math-block](assets/math-block.svg)
{: id="20200925103337-17ex0sx"}

$$
a^2 + b^2 = c^2
$$
{: id="20200925103337-2b8h2np"}

You can switch the math formula block rendering engine in the settings, the default is `MathJax`.
{: id="20200925103337-re23oms"}

### Code block
{: id="20200925103337-izp2r4v"}

![math-block](assets/code-block.svg)
{: id="20200925103337-d3pywfy"}

```js
function hello() {}
```
{: id="20200925103337-8mynmh0"}

### Unordered List Block
{: id="20200925103337-tmkxg9a"}

![math-block](assets/unordered-list.svg)
{: id="20200925103337-j2ujogf"}

* List item one
* List item two
{: id="20200925103337-lhz932m"}

The unordered list block is a type ((20200925102736-x94e40g "block container")).
{: id="20200925102833-ey929t7"}

If you need to wrap a line in a list item, use <kbd>Shift Enter</kbd>.
{: id="20200925102833-3x5rjit"}

### Ordered List Block
{: id="20200925103337-fpvt3aq"}

![math-block](assets/ordered-list.svg)
{: id="20200925103337-79vk3em"}

1. List item one
2. List item two
{: id="20200925103337-3wupq39"}

An ordered list block is a type ((20200925102736-x94e40g "block container")).
{: id="20200925102920-9kzmq59"}

### To do list block
{: id="20200925103337-an4iksl"}

![math-block](assets/task-list.svg)
{: id="20200925103337-xe4f019"}

-[X] To do one
-[] To do two
{: id="20200925103337-e9s5hk8"}

The to-do list block is a type ((20200925102736-x94e40g "block container")).
{: id="20200925102923-1x5hphd"}

### Table block
{: id="20200925103337-6o0q7hb"}

![math-block](assets/table.svg)
{: id="20200925103337-rnbwwds"}

| Column 1 | Column 2 |
| - | - |
| Row One Column One | Row One Column Two |
| Row Two Column One | Row Two Column Two |
{: id="20200925103337-wm4yqil"}

If you need to use `|` in the form, please use `\` to escape, that is, you need to enter `\|`.
{: id="20200925103337-p06d0qm"}

### Block Quote Block
{: id="20200925103337-2yqqaje"}

![math-block](assets/blockquote.svg)
{: id="20200925103337-dvlj1js"}

> Note that it is not a content block quote, but a block quote (Blockquote).
> {: id="20200925103337-zjnxkqa"}
{: id="20200925103337-3k191et"}

The block reference block is a type ((20200925102736-x94e40g "block container")).
{: id="20200925102926-gpj3ey0"}

### Documentation block
{: id="20200925102953-8qxo8tf"}

![doc](assets/doc.svg)
{: id="20200925103337-h77fegc"}

The entire document is a block, and the document block is a type ((20200925102736-x94e40g "block container")).
{: id="20200925102928-85doufh"}

## Content Block meta type
{: id="20200925102736-x94e40g"}

The content block is logically divided into a leaf block and a container block. The leaf block cannot contain other blocks, and the container block can contain other blocks, following the CommonMark/GFM specification.
{: id="20200925102736-1ybd2yh"}

There are several types of container blocks:
{: id="20200925103337-ll6kj8m"}

* List block: can only contain list item blocks (Siyuan Note does not support list item blocks for the time being, that is, it cannot link a single list item), list item blocks can contain any other non-document blocks
* Block reference block: can contain any non-document block
* Super block #TODO#: can contain any non-document block
* Document block: can contain any non-document content block
{: id="20200925102607-dg093r9"}

{: id="20200925102556-53f79lg"}
