---
published: false
---
## Indexed Pathfinding
# and why its important

### Indexed Pathfinding, what is that?
Indexed Pathfinding is essentially just doing Pathfinding on a pre-loaded Dataset, instead of Live Reloading the Enviroment data every Calculation, it is especially important when working with large datasets, or when working with a lot of overall calculations.

This article will Show a little bit about my journey to a efficent Pathfinding algorithm,
Starting with a few basic Tree Concepts.
I will use the C# Language (.Net Core, and Unity) and Minecraft, which recently Published its Scripting language "mcfunction".

### Trees
A Tree is basically only a representation of Nodes.
for example, a tree with three nodes coud look like this:
![3NodeTree](/assets/3-Node-Tree.PNG)]

It has 3 Nodes, A, B, C.
Pathfinding is simply navigating between nodes of a Tree.
Usually each Connection between nodes is both way, and has a certain cost.
If im not using a Picture, i will discribe a Connection like this:
Source Node -Cost-> Target Node
so for example, assuming all costs in the above tree are 1:
A -1-> B
A -1-> C
Often i also will only Describe the Connections in one way, but if not said, i still mean both ways.

Before we get started i also have to explain one last thing.
*Most* of the time we dont know the entire Graph, usually we only have one node, and can get any paths, "discovering" the Graph over time.

ok, so thats all nice, but where is the use?
