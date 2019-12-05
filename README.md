## Introduction
<img src="https://user-images.githubusercontent.com/31917400/65374429-a3e38680-dc81-11e9-887a-ce3802f0daa8.jpg" />

## Four concepts explaining a Complex System
__1.Systems within a System:__ 
 - Herbert Simons gives us this definition; "A system that can be analyzed into many components having relatively many relations among them, so that the behavior of each component depends on the behavior of others."
 - Jerome Singer tells us; "A system that involves **numerous interacting agents** whose aggregate behaviors are to be understood. **`Such aggregate activity is nonlinear`**, hence it cannot simply be derived from summation of individual components behavior."
 - the Emergence Theory? Put things together...Something emerges. The emergence is the special phenomenon that results from the interaction of mutiple elements. Walking is the emergence. It's not about double hopping of two legs. It's a synergistic interaction between two legs. 

-> `Elements are nested inside of subsystems (Multi-dimensional property) and many elements on many different scales with all of these levels affecting each other.` How relationship between multiple parts give rise to the **collective behaviors** of a system ? 
<img src="https://user-images.githubusercontent.com/31917400/65376419-6f7ac500-dc97-11e9-889f-215a08fda75a.jpg" />

__2.Nonlinearity + Chaos:__
 - Nonlinearity arises from the fact that when we put multiple things together, the result may not necessarily be a simple addition of each element's property in isolation. This is Post-Newtonian! 
 
-> `Some small change in input value to the **system** can (via dynamics of feedback loops) trigger a large sysmetic effect that is a **combined effect** greater/less than the simple sum of each element's property because of their interdependent nature.` This is referred to as **sensitivity of initial conditions** which is the central idea of the Chaos theory. 
<img src="https://user-images.githubusercontent.com/31917400/65376608-e1540e00-dc99-11e9-8c0f-a4c4929ef4e1.jpg" />
 
__3.Network:__
 - the Graph Theory?
 
-> `The connection density`(**degree**) `or connection pattern`(**position**: How things flow in the network) `defines the **system** as opposed to the element's properties.` 
<img src="https://user-images.githubusercontent.com/31917400/65376769-b66ab980-dc9b-11e9-83e2-e2e0b4a37910.jpg" />

__4.Adaptation + Self Organization:__
 - When a certain degree of **autonomy** that each element has is coupled with the loosened **"top-down centralized mechanism"** for coordinating the whole system, the elements can synchronize their state locally, resulting in the **emergence of the system from the "bottom-up"**...the Agent-based modeling takes the bottom-up approach? 
 - the Game Theory? Cooperation + Competition
 - To model how the system evolves over times, we give the small rules to each eleement and let them develop and see what happens. We have computers that can simulate this process. This is the "Agent Based Modeling". What macro pattern emerges over time?  

-> `This is the system of diversity and evolution.`
  - `Heterogeneity` with high levels of **diversity**!!! such as ..ecosystems...multicultural societies
  - `Being subject to the evolutionary force` of Selection & Replication...which makes an **evolution**!!!
<img src="https://user-images.githubusercontent.com/31917400/65376982-84a72200-dc9e-11e9-81e5-7a8630b82bcd.jpg" />

Complexity Theory as a generic framework for modeling is the composite of the four perspectives discussed above.

---------------------------------------------------------------------------------------------------------------
## Network Analysis
<img src="https://user-images.githubusercontent.com/31917400/69678662-1ddb2600-109e-11ea-93f9-dbcd9801e3e8.jpg" />

 - Undirected: `Graph01 = nx.Graph()`
 - Directed: `Graph01 = nx.DiGraph()`
 - Multiple relation: `Graph01 = nx.MultiGraph()`
```
import networkx as nx
Graph01 = nx.Graph()

Graph01.add_node("A")
Graph01.add_nodes_from(["B","C"])
Graph01.add_edge('A', 'B', weight=2, sign="+", relation="friend")
Graph01.add_edge('B', 'C', weight=6, sign="-", relation="enemy")
```










---------------------------------------------------------------------------------------------------------------
## How do `individual interactions` aggregate to produce `collective behavior`? and how the collectives behave as an organic whole?
<img src="https://user-images.githubusercontent.com/31917400/69735709-144ad000-1129-11ea-815b-e9c9adb9d2f6.jpg" />

> What does Individial Interaction generate?
 - Patterns of segregation
 - Patterns of inequality
 - Emergence of collective movement
 - Norms that change across time?????
 - **Agent-Based Simulation** helps explain the complex processes generated by individual interactions.
   - We build a system by giving individuals rules and observing the outcome. 

### EX_1. Segregation Model 
<img src="https://user-images.githubusercontent.com/31917400/70067714-9c781c00-15e6-11ea-8f84-866dbc2c09f4.jpg" />

Thomas Schelling was asking, where does segregation come from, and how can we prevent it? **racism? unfair housing practices?** But we also have this intuition that `individuals` produce that phenomenon (Individuals have preferences!). What if we removed all those external forces? traditional explanations of where segregation comes from? Schelling asked the question about the fundamental origins of where segregation comes from. And what the kinds of mechanisms are there that can bring it about. **What the collective pattern of settlement would be in terms of a segregated/integrated society?** Asking counterfactual question!
 - focus on each individual!
 - If we were to remove some important factors such as history, job location, etc. would it still be possible to generate similar outcomes?
 - An agent-based model allows us to test whether a set of conditions or parameters are sufficient to produce a certain outcome.
 - This project models the behavior of two types of agents in a neighborhood. The <orange> agents and <blue> agents get along with one another. But each agent wants to make sure that it lives near some of “its own.” The simulation shows how these individual preferences ripple through the neighborhood, leading to large-scale patterns. 
 
### EX_2. Simple Contagion Network Model
What happens to the structure of this network? Starting from a Lattice(hardware 1D or 2D..) Network, **What happens in something (such as a rumor) is spreading on the network** as we rewire "short distance edges" to make them "long distance edges" (introducing "Random ties" to "Lattice ties" - Tying between nodes that does not share neighbors - Combining Lattice_Nwk + Random_Nwk)? It increases the speed of diffusion because the **`"long distance ties"`** provide **short-cuts** that reduce the average path length of a network! So the world get smaller and the diffusion get faster because of the short cuts.
<img src="https://user-images.githubusercontent.com/31917400/70138652-9cc8f380-1688-11ea-8163-9bb1b86ec8b4.jpg" />

What drives diffusion? The network science thinks about how the **structure of interactions** affects that `diffusion process`. How information and behavior can spread through system? The **theories of "virality"** focuses on the `quality of the idea or item` to be diffused as an explanation for why some contagions spread and why others don’t. In contrast, the network model gives an idea that **`variations`, the pattern of who-is-connected-to-whom** can explain why some contagions succeed while others fail. How can we operationalize it in a systematical way? The network science starts from **"graph theory"**(node and edge) which focuses on `ties`(edge) and `vertex`(individual node) between people. We trace the series of steps the thing takes and spread over the network. 
 - rumor, brain, transportation network, etc.
 - Spreading is governed by the shape of the network!!
 - voting activities can be an example of a thing that spreads through networks because people’s likelihood of participating increases as more of their `peers` participate and participation is determined not only by psychological dispositions, but by `peer` influences.

> ### Simple Types of Network
 - __Lattice Graph(Spatial Network)__ physical network?
   <img src="https://user-images.githubusercontent.com/31917400/70074574-e2d37800-15f2-11ea-972b-4da5f12a4855.jpg" />
   
   - 1D Lattice cares immediate adjacency(right next door) or something farther(more doors down).  
   - 2D Lattice cares 8 entities(up,down,left,right + 4 corners).
   - `High Clustering` Coefficient
     - high clustering: two randomly selected contacts are likely to have a lot of same neighbors in common
 - __Random Graph__ trenscending network?
   <img src="https://user-images.githubusercontent.com/31917400/70075714-3e066a00-15f5-11ea-8727-9ace6917af5b.jpg" />
   
   - Low Path Length(AVG)
     - In Lattice, if you randomly select two nodes that are far apart from each other, it will require a lot of hops across each edge in order to connect(message) one node to another node. In Random Graph, the average path length between two randomly selected nodes is very small, taking only a few hops to get from any node to any other node in the network.
   - `Low Clustering` Coefficient
     - If you randomly select nodes, it is possible that none of them can be neighboring...

### EX_3. Complex Contagion Network Model
Unlike simple contagions (where a mere single contact is sufficient for transmissions), complex contagions may require **multiple sources of contact(repeated exposure)** before thing is transmitted. For example, the transmission(adaption) may require a sort of a **sense of proof** about the credibility of that thing. 

 - __Threshold Model__
   - Contagion Threshold
     - A certain NO of contact(adaption by neighbors) is required to trigger transmission(adaption).
     <img src="https://user-images.githubusercontent.com/31917400/70147991-41edc700-169d-11ea-9170-148697938c73.jpg" />

   - Network structures & Types of Contagions to spread
     - __ASK:__ What `threshold rules` define a contagion that can spread in a system? what's the **largest threshold** that contagion could spread? **How many neighbors each node has and how many of them should show the adaption** so that contagion could spread? This might differ by the Graph structure.
     - We can measure this quantity of overlapping neighborhoods by using what's called a `clustering coefficient`. In general, networks with the **higher clustering coefficient** will be more effective at spreading contagions. 
       - > Lattice Graph - **Ring**
         <img src="https://user-images.githubusercontent.com/31917400/70173967-e71f9400-16cb-11ea-92b5-4bd12089f08b.jpg" />

         - Arranged on a ring, each node has the `same` number of neighbors. 
         - __0.5 Threshold:__ Each agent will adopt if `half` of their all neighbors have already adopted. 
           - `Seed Node` and the very **`Next Node` outside of the Seed Neighborhood** shares half of their neighbors. So node 1's neighborhood has adopted, node 4 is satisfied because half of their neighborhoods have adopted, thus node 4 will adopt the contagion. 
           -  We can see the pattern unfold because whenever a **given neighborhood has adopted**, the **`first node` outside that neighborhood** will always adopt!
           -  This will be true in the ring lattice no matter how many neighbors each node has.
           
       - > Lattice Graph - **Square**(Moore lattice)
         <img src="https://user-images.githubusercontent.com/31917400/70234521-b9ccf780-1758-11ea-82ea-e246d09308ce.jpg" />

         - Arranged on a grid, the nodes are connected to the neighbors to the "left|right|above|below|4 corners".  
         - One can see that the **`closest`** node to the **focal node** outside the seed neighborhood shares 3/8 of their neighbors with that **focal node**. And that means that from the outset, 3/8 of their neighbors have already adopted. 
         - This tells us that, at most, a threshold of `3/8` can spread in a square lattice. Any threshold with a contagion less than or equal to `3/8` will spread easily and the contagion cascades through the network. 
         - But the contagion with a threshold greater than `3/8` won't spread at all.
       - > Random Graph
         <img src="https://user-images.githubusercontent.com/31917400/70147991-41edc700-169d-11ea-9170-148697938c73.jpg" />

         -
         - 














































































