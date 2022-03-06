Source code:
https://gitlab.com/AlexElliott/Skyscraper

This was a graphics project, the most major piece of coursework for the computer graphics module. It involved creating a complex scene in OpenGL, which used C++. The scene I created was a city plaza scene with a skyscraper in the middle, consisting of pavement, road, decorations and moving objects. Seen here:
![skyscraper2](https://user-images.githubusercontent.com/57454635/156931236-1d35dd0a-2cb1-4d35-9ad6-6d99b1c52c8c.gif)

The scene makes full use of simple and complex objects, lighting, textures, animation and user interactivity. Some of the objects were made manually while others are 'glut' objects. Many elements also respond dynamically to changes in other parts of the scene, such as position of the pavement and the car when the road's width changes, or the speed of the lift when the tower changes height.

This project took quite a few weeks of work. I first spent a lot of time figuring out how to make the different layers of the ground grow dynamically, that is, how to get them to change their position and size when the ones closer to the middle change. What I ended up with was a sort of rolling set of calculations where the width and midpoint of each layer is used to calculate the next. The animations also took some time to get right, as they also had to change size or position depending on other factors, such as the lift always taking the same amount of time to go up and down the skyscraper no matter its height. Texturing was a particularly difficult nut to crack as different sources gave me different methods, but I eventually found a way that worked for my implementation.

I got a fairly good mark for this in the end, and a 1st for the module overall. Primarily it taught me a lot about OpenGL and how to create the most important parts of a scene in it. I'm using what I learnt here in my 3rd year project, which also uses OpenGL and has a similar urban theme.

Note: When running the program, the textures may nor may not show depending on what operating system you are using. Currently it is set to work on Windows, though a simple change to the file path format will make it work for Mac and Linux.
