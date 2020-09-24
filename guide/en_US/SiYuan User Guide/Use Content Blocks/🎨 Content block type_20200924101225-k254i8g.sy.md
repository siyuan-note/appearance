Hover the mouse over the content block and the corresponding icon will appear on the left side of the content block. For layout usage, please refer to ((20200825162036-4dx365o "Markdown complete example")).
{: id="20200924101242-qo0msk0"}

| Logo | Type |
| - | - |
| ![paragraph](assets/paragraph.svg) | Paragraph block |
| ![heading](assets/heading.svg) | Title block |
| ![math-block](assets/math-block.svg) | Math formula block |
| ![math-block](assets/code-block.svg) | Code block |
| ![math-block](assets/unordered-list.svg) | Unordered List Block |
| ![math-block](assets/ordered-list.svg) | Ordered List Block |
| ![math-block](assets/task-list.svg) | To-do list block |
| ![math-block](assets/table.svg) | Table block |
| ![math-block](assets/blockquote.svg) | Blockquote block |
| ![doc](assets/doc.svg) | Document block |
{: id="20200924101242-98g1jf0"}

Below we introduce the details of these content block types.
{: id="20200924101242-iepviyn"}

## Paragraph block
{: id="20200924101242-hs49y8s"}

![paragraph](assets/paragraph.svg)
{: id="20200924101242-jjo4w4q"}

Here is a sample paragraph.
{: id="20200924101242-6bzmjkm"}

Press Enter directly after a paragraph to form a new paragraph.
{: id="20200924101242-93zdaet"}

## Title block
{: id="20200924101242-vvybu2g"}

![heading](assets/heading.svg)
{: id="20200924101242-nhmi8go"}

The above is the title block, which supports level one to six.
{: id="20200924101242-i7jbsdq"}

When using block citation embedded rendering (`((id "*"))`), related content blocks under the title block will be automatically aggregated according to the title level.
{: id="20200924101242-m635m7i"}

## Mathematical formula block
{: id="20200924101242-jbs78yb"}

![math-block](assets/math-block.svg)
{: id="20200924101242-zt3utlz"}

$$
a^2 + b^2 = c^2
$$
{: id="20200924101242-jwemmsc"}

You can switch the math formula block rendering engine in the settings, the default is `MathJax`.
{: id="20200924101242-99phlsd"}

## Code block
{: id="20200924101242-c3wxa9o"}

![math-block](assets/code-block.svg)
{: id="20200924101242-as2jt6f"}

```js
function hello() {}
```
{: id="20200924101242-k8wht6b"}

## Unordered List Block
{: id="20200924101242-s5yv2fy"}

![math-block](assets/unordered-list.svg)
{: id="20200924101242-hsolbv6"}

* List item one
* List item two
{: id="20200924101242-8mywjfu"}

If you need to wrap a line in a list item, use <kbd>Shift Enter</kbd>.
{: id="20200924101242-pg0qt0r"}

## Ordered List Block
{: id="20200924101242-r7u1f3a"}

![math-block](assets/ordered-list.svg)
{: id="20200924101242-caf6dvv"}

1. List item one
2. List item two
{: id="20200924101242-wb1pcnw"}

## To do list block
{: id="20200924101242-pylw1lr"}

![math-block](assets/task-list.svg)
{: id="20200924101242-ah5kl2a"}

-[X] To do one
-[] To do two
{: id="20200924101242-uexgmfm"}

## Table block
{: id="20200924101242-fcvwu0x"}

![math-block](assets/table.svg)
{: id="20200924101242-6oo9fv5"}

| Column 1 | Column 2 |
| - | - |
| Row One Column One | Row One Column Two |
| Row Two Column One | Row Two Column Two |
{: id="20200924101242-1w5kcvg"}

If you need to use `|` in the form, please use `\` to escape, that is, you need to enter `\|`.
{: id="20200924101242-o6pa7bp"}

## Block Quote Block
{: id="20200924101242-a89edjl"}

![math-block](assets/blockquote.svg)
{: id="20200924101242-hd2tesh"}

> Note that it is not a content block quote, but a block quote (Blockquote).
> {: id="20200924101242-wrjy7f5"}
{: id="20200924101242-2fao3xe"}

## Documentation
{: id="20200924101242-1o5wkcy"}

![doc](assets/doc.svg)
{: id="20200924101242-g4sfc9s"}

The entire document is also a block.
{: id="20200924101241-p5abwte"}
