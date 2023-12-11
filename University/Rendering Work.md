This is information on academic projects I did for coursework in the Foundations of Modelling and Rendering module in my fourth year of uni. These were all done in C++ with OpenGL. Unforunately, due to university rules, I am not allowed to share the actual source code. Personal thoughts can be found at the end.

## Coursework 1 - Raytracing
The first coursework had us implement raytracing from scratch. We were provided with a scene in OpenGL and a framework in which to implement the functions. We had to implement:
- Geometric intersections, calculating whether a ray intersected any triangle in the scene.
- Barycentric interpolation, utilising barycentric coordinates to interpolate normal values.
- Blinn-Phong Shading, considering every light in the scene.
- Shadow rays, for adding shadows.
- Reflection, checking if a surface is mirrored and calculating for a reflected ray if so.
- Refraction, checking if a surface has transparency, calculating refracted directions and final shading.
- Fresnel equations, turning some of the refracted and diffuse light into reflected light.
- Monte-Carlo sampled indirect lighting. 

This coursework went fairly well; I successfully completed most of the tasks, although did not get to do Monte-Carlo and didn't finish Fresnel. It was a pain to get started on, and I had many hours where my raytracing results were insane acid trips, but once I discovered my early mistakes everything began falling into place. 
The content we learnt for this was very interesting too, learning about how raytracing properly works, however it was not the main focus of the course and the next unit of content was even more interesting

## Coursework 2 - Rasterisation
The second coursework had us implement rasterisation from scratch. We were similarly provided with a scene in OpenGL and a framwork of functions to implement. We had to implement:
- Manipulating the buffer, clearing it every frame.
- Rendering a single point.
- Changing the point size.
- Matrix transformations, allowing the point to be rotated and translated.
- Rendering lines and colour gradients.
- Rendering triangles, as well as displaying texture coordinates.
- Depth testing.
- Lighting, and light transformations.
- Textures, including combining textures with lighting and bilinear filtering.
- Clipping and culling, to improve render time.
- Parellelisation, introducing multi-threading.

This coursework went ok. I implemented most of the functions except for clipping and I didn't have time to parellelise, however there were a few mistakes throughout that lost me marks, like bilinear filtering. This was partially due to me actually having trouble with some parts, but I was also suffering from burnout in the latter weeks of this coursework which contributed a lot to not being able to complete things.
Nonetheless, this part of the module was extremely interesting. Rasterisation is how video games do their rendering, so to finally learn the basics of this process was like unlocking a great secret. Knowing all the techniques that go on in every frame of a game has made me look at them in a whole new way ever since, and laid the groundwork for me having more success in the High-Performance Graphics module in the next semester.

## Coursework 3 - Shaders
The third coursework introduced us to shaders. We were similarly provided with a scene in OpenGL, and this time shaders to implement. The coursework had us implement:
- Vertex shader, processing each vertex in a mesh and reading from a heightmap.
- Fragment shader, reading from textures and implementing phong shading.
- Tesselation shader, making the mesh more detailed.
- Geometry shader, rendering 2d sprites on the mesh.

This coursework went fairly well, and I successfully implemented all of them except the geometry shader. Although this part of the module wasn't as groundbreaking as what came before, it was critical knowledge. Shaders and GLSL had initially confused me, so learning them properly was critical to my graphics programming ability. 

## Thoughts
Like the other graphics modules, the Foundations of Modelling and Rendering was a challenge but I learned a lot of very valuable and interesting things. And although I struggled a bit with the coursework, due to a mix of challenging content and external circumstances, learning the fundamentals of rendering proved to be so interesting it sparked my further interest in graphics. Rasterisation in particular, since real-time rendering is most relevent to my desire to get involved with the games industry, and knowing it has changed my understanding of how games work on a technical level I'd not realised before.
