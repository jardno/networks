# networks
SNA data for AH162

<b>Sample data for basic manual encoding</b>

As we discussed in class, creating a dataset from a narrative requires making a series of decisions about who constitutes an actor, how to assess the directionality of interactions between actors, and how to weigh (quantify) the relationship.

If you [wanna go fast](https://www.netflix.com/title/70044894): for those of you with grounding in Python and R, the Natural Language Processing community has developed a variety of excellent tools to automate the markup and parsing of texts. Bookworm, which you can find in this [forked repository](https://github.com/jardno/bookworm), scans through .txt files to divide a text into sequences (sentences, words, characters) and can identify parts of speech to make some predictions about the relationship between characters (or, really, proper nouns). One downside of NPL techniques is that they tend to be concerned with co-occurence (physical proximity within a sentence; bookworm = names within a distance of 15 words of each other) and cannot detect nuance in relationships. 

The forked repository for the <i>Game of Thrones</i> novels contains datasets created from co-occurence tests. You can get a sense of how plot lines develop (e.g., what's going on in Martin's mind) but gain fewer insights into the meaning of the co-occurence (e.g., if characters appear together because they are rivals at war or because they have familial ties....or...both).

The point here is that you need to have a plan ahead of time to determine where measurements of co-occurence can work productively for the type of question you're asking. Your "good question" should also keep in mind how you can assess the directionality of relationships, which determines how you will need to detect, sort, and present your data.

<b>Undirected relationships</b>: characters are in conversation or appear together within a scene.

<b>Directed relationships</b>: characters reference other characters (reciprocity not required).

<b>Weighted relationships</b>: the relationship between characters is a function of a certain variable (length of conversation, absence/presence of a transaction or gift, etc.)

The GOT networks assess undirected relationships (proximity within sentence, chapter, book). An influencer network takes the form of directed relationships (i.e., I cite an author's famous text but that text may not cite my work). We could improve the GOT data by qualifying the nature of the relationships. For example, we could manually markup the texts to determine the nature of the interaction between any two characters in terms of allies (1), enemies (2), or neither (3). We could also use a binary appraisal of familial relationships (Lannister to Lannister = 1; Lannister to non-Lannister = 0).

NOTE: text mining and topic modeling tools can help you better assess the relationship nature; you'll just need to model terms (like we did with <i>Robots Reading Vogue</i>) that you believe will assess an antagonistic relationship, for example, then iterate over the corpus. 

Before diving into <i>The Handmaid's Tale</i>, let's take a look at lower hanging fruit: animated television shows. Shows like <i>Family Guy</i>, <i>the Simpsons</i>, <i>Archer</i>, and <i>Rick and Morty</i> (used here) have a limited number of recurring characters, which reduces our workload to encode relationships. Another benefit is that people love making extensive wikis about these shows; this information can help you trace a character's appearance over one or multiple seasons. Last, the internet is abound with scripts that break episodes into specific scenes and use formatting that clearly identifies when a character speaks and to whom. 

The files below show you my process of manually encoding <i>Rick and Morty</i> s01e01 ("Pilot").

[rick-and-morty-nodes.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot-nodes.csv) provides a simple list of all named characters that appear in the episode with gender as an additional attribute. Each character has a unique id. This node file should be paired with [rich-and-morty-pilot.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot.csv), which lists the number of interactions <i>between</i> <b>each character</b> <i>within</i> <b>each scene</b>. I considered an interaction any instance a character spoke directly to another character or indirectly to a group of characters. The numbers in the Source and Target columns derive from the Id list in the node file.

[rick-and-morty-new.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot-new.csv) aggregates the number of interactions between two characters <i>across the entire episode</i> as a <b>weight</b> (e.g., Morty -> speaks to -> Rick -> x number of times).

<b>SOFTWARE/PLATFORMS</b>: We haven't talked about where to use this data. The third file (...new.csv) is best suited for Palladio (no Id number, clear weight for source-target interactions). The first two (...nodes.csv and ...pilot.csv) will work better with [Gephi](https://gephi.org/), an open-source application that has a very qGIS kind of feel. You are not required to download this software but it improves on Palladio's limitations. (And there are other platforms, too! I've listed them here with links to tutorials and overviews.)

For the purposes of class 14.1, we'll examine a few datasets that you can explore more superficially (with Palladio) or in more analytical detail (with Gephi) depending on your interest in this topic. These datasets do not need to be reproduced; rather, you should use them as inspiration to decide how you will approach Atwood's The Handmaid's Tale.

<b>Dataset #1</b>: [Characters of <i>Les Misèrables</i>](https://github.com/jardno/networks/blob/master/les-mis.md)

<b>Dataset #2</b>: The affiliations of American revolutionaries

<b>Dataset #3</b>: <i>Rick and Morty</i>
