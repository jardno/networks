<h1>Dataset #1: <i>Les Misérables</i></hi>

<h2>*This tutorial works best in Gephi.</h2> 

<b>Step 1</b>: Download and [install Gephi.](https://gephi.org/) 

<b>Step 2</b>: Open Gephi and go to File > New Project. Next, update your version of Gephi. Go to Help > Check for Updates. 

<b>Step 3</b>: Go to Window > Welcome and click on the Les Miserables.gexf file (this file comes pre-packaged within the program). This is an example of a character co-appearance network, based on Victor Hugo’s Les Misérables. You’ll see an Import Report telling you that this is an undirected graph with 77 nodes and 254 edges. Click OK.

<b>Step 4</b>: You should be in the Data Laboratory panel and see a data table with the 77 nodes. Notice how the data is structured. You’ll see column headers called Nodes, Id, Label, Modularity Class. Someone has already either run a modularity algorithm on this dataset, or they coded the data manually. Modularity is a useful form of “community detection.” More on that here. Communities will have dense connections in between nodes, and sparse connections with nodes in other communities, very much like friend or family groups.

<b>Step 5</b>: In the upper lefthand corner, next to nodes, you should see a tab called edges. Click on it. This is the edge list, also known as the connections or relationships in between the nodes. This is an undirected network, meaning that the relationships are symmetrical. In other words, Javert talks to Valjean, but it could just as truthfully be said that Valjean talks to Javert (symmetry indicates repciprocity!).

![Image of Le Mis nodes](https://user-images.githubusercontent.com/24833217/33508100-3ce9fe90-d6ad-11e7-8ebc-54c91a4c5913.png)

<b>Step 6</b>: Click on the Overview panel (upper lefthand side). Click on the T on the lower navigation menu to show the node labels.

<b>Step 7</b>: Play around with the different presets in the Layout panel (bottom left of the screen). For example, you can select "ForceAtlas 2," enable the settings "Prevent Overlap" and "LinLog mode," the click "Run." Let the network readjust dynamically until it arrives at a place you think looks clearer to read, then click "Stop". You can then select the hand icon from the main middle panel and click-drag individual nodes into different positions.

<b>Step 8</b>: Examine the relationship between main characters. What does the network reveal? What other attributes would you want to encode? For example, would you try to geolocate the conversations? Or would you code each node for gender?

In the screenshot below, I'm hovering over Valjean to see his direct connections. The thicker the line, the more frequent co-appearances he has with another character.

![valjean](https://user-images.githubusercontent.com/24833217/33508565-f4838844-d6af-11e7-8dd9-ffb5379f043d.png)

<b>Step 9</b>: [OPTIONAL] You can explore more of Gephi's tools if you'd like. Let’s say we want to know which node in this character interaction network is the most important. 

* One measure to determine importance might be centrality. Let’s use Gephi’s Eigenvector centrality measure to find important nodes. Along the righthand side, you’ll find the network algorithms for analyzing the relationships. Click “Run” next to Eigenvector Centrality to start the analysis.Once the analysis runs, we’ll be presented with a graph of the centrality distribution. Click ok to return to the graph.

* Once the statistics are available, we can now apply the measures to various visual aspects of the graph. Since Eigenvector is a measure of node importance, let’s use the results to change the size of the nodes based on their centrality. In the “Appearance” pane in the upperlefthand side, select the “Size” tab (the three circle icon), select “Attribute”, and from the dropdown choose “Eigenvector Centrality.” Feel free to adjust the minimum and maximum size of the circles. Otherwise, select “Apply” and our nodes will resize based on their Eigenvector measure. We can now see the more important nodes in the network based on their centrality. 

* We can also do additional statistical measures such as modularity to find communities in the network. In the “Statistics” pane run “Modularity”. Once the measures are available, let’s color the nodes based on their communities. In the “Appearance” pane, select “Nodes,” select the “Color” tab (the painting palette), select “Attributes” and choose “Modularity Class” from the dropdown. You can change the color palette if you choose. Then “Apply” the changes to see the measure applied to the nodes.

<b>Step 8</b>: Next, click on the Preview panel. This is where you would go after you’ve got everything looking just the way you want it in the Overview panel. Click the Refresh button. Your labels will have dropped out again, but you can add them again by clicking on Show labels in the menu to your left and clicking on Refresh. You may find that the Proportional size option impairs the readability of the graph. If so uncheck it, and adjust the font manually to something like 24 pt, and click Refresh once more. You can also select different line types (curved, straight, etc.) from the preset drop down within the Preview Settings panel (Window > Preview Settings). 

<b>Step 9</b>: Save your graph as a PDF.

If you're interested in how other people have approached this data, check out the following blogs:

[Visualizing <i>Les Misérables</i> (Northwestern University)](https://lesmiserables.mla.hcommons.org/)

If you're having difficulty styling and filtering your data, [check out this tutorial](https://seinecle.github.io/gephi-tutorials/generated-html/using-filters-en.html) or [this one!](http://miriamposner.com/dh101f14/?p=1389)
