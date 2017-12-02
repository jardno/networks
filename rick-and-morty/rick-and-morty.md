<h1>Dataset 3: <i>Rick and Morty</i></h1>

Before diving into <i>The Handmaid's Tale</i>, let's take a look at lower hanging fruit: animated television shows. Shows like <i>Family Guy</i>, <i>the Simpsons</i>, <i>Archer</i>, and <i>Rick and Morty</i> (used here) have a limited number of recurring characters, which reduces our workload to encode relationships. 

Another benefit is that people love making extensive wikis about these shows; this information can help you trace a character's appearance over one or multiple seasons. Last, the internet is abound with scripts that break episodes into specific scenes and use formatting that clearly identifies when a character speaks and to whom.

![screen shot 2017-12-01 at 8 55 46 pm](https://user-images.githubusercontent.com/24833217/33511930-20633750-d6da-11e7-82d8-cbc051013c11.png)

The files below show you my process of manually encoding <i>Rick and Morty</i> [s01e01 ("Pilot")](http://dai.ly/x2syy9m).

* [rick-and-morty-nodes.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot-nodes.csv) provides a simple list of all named characters that appear in the episode with gender as an additional attribute. Each character has a unique id. 
* This node file should be paired with [rich-and-morty-edges.csv](https://github.com/jardno/networks/blob/master/rick-and-morty/rick-morty%20-%20edges.csv), which lists the number of interactions <i>between</i> <b>each character</b> <i>within</i> <b>each scene</b>. I considered an interaction any instance a character spoke directly to another character or indirectly to a group of characters. The numbers in the Source and Target columns derive from the Id list in the node file.
* [rick-and-morty-new.csv](https://github.com/jardno/networks/blob/master/rick-and-morty/rick-and-morty-pilot-new.csv) aggregates the number of interactions between two characters <i>across the entire episode</i> as a <b>weight</b> (e.g., Morty -> speaks to -> Rick -> x number of times).
* Try manipulating the .csv data to join edges and notes. In Gephi, you should check to ensure the interactions between characters become the weight of the edges. If Gephi autogenerates the wrong weights, use the option "Copy data to other column" in Data Laboratory view to replace the Weight column values with the Interaction column values.
* Palladio seems to have an issue reading small networks, so this might be a good chance to download and install Gephi. Here's my final file so you can check your work against the network visualized below: [rick-morty.gefx](https://github.com/jardno/networks/blob/master/rick-and-morty/rick-morty.gexf.zip)

![rick-morty-weighted](https://user-images.githubusercontent.com/24833217/33511875-16d2d2dc-d6d9-11e7-9af5-3095ca078bbb.png)
