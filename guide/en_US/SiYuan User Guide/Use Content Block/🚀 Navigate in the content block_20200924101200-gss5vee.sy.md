## Link
{: id="20200924101210-p7g333d"}

There are two types of links in the document content:
{: id="20200924101210-d1j90tj"}

* Hyperlink, which is the form of `[foo](bar)` provided by Markdown standard syntax
* Content block link established by `((id))`
{: id="20200924101210-54t2af9"}

Both of these links can be opened by <kbd>Ctrl+ Click</kbd> to jump.
{: id="20200924101210-p5bqlm5"}

## Graph
{: id="20200924101210-zwf8ags"}

The relationship diagram is divided into document level and global. The relationship diagram of the document is expanded based on the current document block and presents all the content blocks (forward links and reverse links) related to the document; the global relationship diagram is all the block and link relationships in all notebooks.
{: id="20200924101210-xmlgl2z"}

We can open the corresponding document by double-clicking the node on the graph. If the normal block is clicked, it will be located on the specific content block in the document after opening. When editing a document, if the relationship diagram of the corresponding document is opened, it will automatically roam on the relationship diagram and highlight nodes according to the content block where the cursor is located.
{: id="20200924101210-sztned8"}

## Backlinks
{: id="20200924101210-3qfiiat"}

The backlink list is document-level, showing where the content block in the current corresponding document is referenced.
{: id="20200924101210-cpyj03s"}

* Clicking on the reference block in the backlink list will highlight the definition block in the current document
* The defined block in the current document where the cursor is located will highlight the quoted block in the backlink list (if there is a reference)
* Hover the mouse over the icon in front of the reference block in the backlink list to preview the content
* Double-click the reference block in the backlink list to jump
{: id="20200924125314-vui7023"}
