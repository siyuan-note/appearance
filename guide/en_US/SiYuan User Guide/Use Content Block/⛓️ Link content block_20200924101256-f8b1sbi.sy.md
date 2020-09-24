For ((20200924101106-19z4kaa "content block")), the most valuable way to use it is to link them through ((20200924101312-jj4e0v3 "reference")) and ((20200924094024-s0oyhvp "embedding")). A good link is directional:
{: id="20200924101312-p8jwek5"}

* Forwardlink, that is, which other content blocks are used in the current content block
* Backlink, that is, the current content block is used by those other content blocks
{: id="20200924101312-agpas45"}

The forward link is included in the content of the current block, which we can see intuitively. Backlinks need to be searched in other documents to know, and it is precisely this information that is more valuable to us. We can use the following two ways to help us better grasp the knowledge points or diverge ideas:
{: id="20200924101312-dag4nyi"}

* ((20200924101210-zwf8ags "Graph")): browse forward and backward link relationships between content blocks
* ((20200924101210-3qfiiat "Backlinks")): Display the backlinks of the current content block as a text list
{: id="20200924101312-x4rxp0v"}

### Content block reference
{: id="20200924101312-jj4e0v3"}

Entering `((` will trigger the content block quotation search, continue to enter as the search keyword, use the up and down keys to select in the search results and press Enter to complete the content block quotation.
{: id="20200924101312-0nexjwy"}

The complete syntax of the content block quote is: `((id "text"))`, where the `id` is like: `202008250000-a1b2c3d`, consisting of time and 7 random characters, the content block id is when the content block is created It will be automatically generated; the following `text` is the custom anchor text for the content block in the quote. After the content block quote is established, hover the mouse over the anchor text and a preview floating layer will pop up to show the quoted content block.
{: id="20200924101312-d74spxd"}

### Content block embedding
{: id="20200924101312-385dey5"}

Enter `!((` at the beginning of a new line and it will trigger the content block embedded search. Just like the content block reference, you can complete the embedding by selecting the content block you need in the search results. It also supports custom `text` anchor text After the embedding operation is completed, the embedded content block will be displayed directly below.
{: id="20200924101312-2lgxjg0"}

It is worth noting that the content block embedding itself is also a kind of content block, which means that we cannot use the content block embedding in the middle of a sentence, and can only embed at the beginning of a new line. The following is an example of content block embedding:
{: id="20200924101312-hltgb9x"}

!((20200923234102-fota8wn "content block embed demo"))
{: id="20200924125710-aqdjz28"}
