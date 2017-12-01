# networks
SNA data for AH162

[rick-and-morty-nodes.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot-nodes.csv) provides a simple list of all named characters that appear in the episode with gender as an additional attribute. Each character has a unique id. This node file should be paired with [rich-and-morty-pilot.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot.csv), which lists the number of interactions between each character within each scene. I considered an interaction any instance a character spoke directly to another character or indirectly to a group of characters. The numbers in the Source and Target columns derive from the Id list in the node file.

[rick-and-morty-new.csv](https://github.com/jardno/networks/blob/master/rick-and-morty-pilot-new.csv) aggregates the number of interactions between two characters <i>across the entire episode</i> as a <b>weight</b> (e.g., Morty -> speaks to -> Rick -> x number of times).
