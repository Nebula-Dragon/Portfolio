Source code: 
https://gitlab.com/AlexElliott/3rd-year-project

This is my 3rd year project and dissertation, a computer graphics project to procedurally generate a city using C++ and OpenGL. The aim is to create a program that can, with given parameters, generate a unique and randomised city layout with accompanying buildings. This is an extensive project that is still in progress. It's divided into three parts: primary road generation, secondary road generation, and building generation. This is based off of research papers I studied while researching the topic, particularly the method from [Kelly and McCabe 2007](https://www.researchgate.net/publication/357658334_Citygen_An_Interactive_System_for_Procedural_City_Generation).

Primary road generation is the creation of the road network that defines the layout of the city. Secondary road generation is the creation of smaller sets of road that fill in the areas bounded by the primary roads. Building generation is the construction of buildings along the secondary roads. Currently only primary road generation has progress made.

Primary road generation is done by iteratively adding nodes in random directions and then drawing links between them. When done at 90 degree angles it looks like this:

<img src="https://user-images.githubusercontent.com/57454635/156932550-1a799082-bdc5-4d19-bcc4-b93c7377761f.PNG" width=50% height=50%>
<img src="https://user-images.githubusercontent.com/57454635/156932565-de0e4f4e-077d-402a-8d21-c1936171d4ff.PNG" width=50% height=50%>

The road at different angles is still in-progress.
