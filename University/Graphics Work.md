TODO

These are a collection of examples from the graphics courseworks I did in my fourth year of uni. These are all done in Vulkan.
Unforunately, due to university rules, I am not allowed to share the actual source code.

1 - The first coursework was mostly just setting up Vulkan and getting it to load a simple premade scene. This involved loading the scene's vertex coordinates, normal coordinates, texture coordinates and textures, and rendering them with the Vulkan API. It also involved making the camera movable and enabling anisotropy to reduce texture blurring. The result was the following: 

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/92a7c12a-a75f-457b-bce4-de7ef081e418)

There was also a task involving visualing data about the scene, specifically visualising the mip level that was being used for each texture at that point. The result was the following:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/c9e8f59d-7faa-4899-8061-bab2794da15a)

2 - The second coursework involved implementing shading and lighting calculations, specifically a Blinn-Phong lighting model, which involed more extensive use of shaders and GLSL. I implemented physically-based lighting such as diffuse and specular light, metallic effects and other proeprties. The result was the following:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/02af894b-cec2-415a-9f23-5ae227263316)

As part of the lighting calculations, we also allowed for the visualisation of their components. For example, here we see the masking term (showing how much certain surfaces are looking at the light) and the Fresnel term (showing which parts of the scene are metallic):

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/3198c484-720a-44b5-ba07-afb95cea1b44)
![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/8d6b79c8-a3c1-461e-a8e4-5930531d0815)

Next we implemented alpha masking, allowing for transparency and translucency in objects such as the foliage:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/dcd52035-b229-4f53-8cc9-1e7eb3112b2a)

Later on we implemented normal mapping, utilising 'tangent space' to greatly increase the detail of the normals of the surfaces and thus their lit appearance:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/aa180074-ebd2-4f02-9d3d-88345af01c03)

Finally, we implemented optimisations to the mesh data to make normal mapping more efficient, by packing the data required into a more compact format when it is sent to the GPU. Specifically, this was packing the TBN (Tangent-Bitangent-Normal) matrix into a quaternion and then unpacking it in the shaders. This produced no difference in the output but reduced the amount of data being sent to the GPU, and thus its latency. This was easily the most challenging part of the coursework as it meant struggling with a lot of data formatting and reformatting between source files, Vulkan data formats I was unfamiliar with, maths libraries for the matrices and quaternions, and trying to debug issues in the shaders where no debugger is available, among other headaches.

3 - The third coursework introduced post-processing and the idea of rendering to an intermediary texture instead of straight to output and doing multiple render passes. After setting this up initially, the first task was to implement tone mapping for high-dynamic range values, which accounts for when colour values go over 1.0 and brings them down to values able to be outputted. We implemented a simple Reinhard tone mapping operator, with this before and after result:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/063db20a-01a3-4d4a-89cc-83e08e647c63)

The next task was to implement bloom. This involved filtering out the glowing parts of the object, rendering them to their own texture and doing post-processing on them before adding them back. This was the result:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/4eb66427-ff34-441e-a634-aa42cc7f6025)

4 - The fourth coursework was about implementing shadows, which was quite a challenge. It first involved rendering the scene from the light's point of view to create a shadow map texture (a texture with only depth information), and then when rendering from the camera's point of view, using that shadow map to determine whether or not a part of the scene was in shadow. This sounds deceptively simple but involved a lot of wrangling with the Vulkan and GLSL functions for doing this as well as transforming and normalising data between different spaces, such as light space and camera space. The task also involved blurring the shadows with a post-processing filter, experimenting with different shadow resolutions and avoiding shadow acne by using frontface culling. The final result was this:

![image](https://github.com/Nebula-Dragon/Portfolio/assets/57454635/5bf69b87-4a42-4cf2-aff6-416e2d77d15f)

