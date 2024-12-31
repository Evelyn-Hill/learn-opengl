## OpenGL is all 3D.

OpenGL keeps everything in 3D space. A big part of OpenGL is transform 3D coordinates to 2D coordinates, and then transform those 2D coordinates to 2D screen space pixels.


## The Graphics Pipeline

Transforms 3D coords to 2D Screen space pixels. It can be divided into several steps where each step requires the output of the previous step as input. These steps are called shaders.


The pipeline is roughly

Vertex Shader -> Shape Assembly -> Geometry Shader -> Rasterization -> Fragment Shader -> Tests and Blending. 


as an input to this pipeline, we pass Vertex Data. Vertex Data is a collection of vertices and a vertex is a collection of data about a 3D coordinate. It is represented using vertex attributes. Vertex attributes can contain any data we'd like. For now, they will contain a position and color.

OpenGL needs to know how to process your vertex data, and it does that using a hint called primitives.
Primitives are given to OpenGL while calling any of the drawing commands.

OpenGL uses *Normalized Device coordinates* meaning that all 3d coordinates are between 0 and 1. Anything outside of this range will not be displayed in the viewport.


## Sending Vertices to the GPU! OMG OMG OMG!!!

The first thing we must do is define some vertex data in a float array.

With the vertex data defined, we'd like to send it to the vertex shader. This is done by creating memory on the GPU that we can store the vertex data in, and configure how OpenGL should interpret the memory and specify how to send the data to the graphics card.

We manage this memory using vertex buffer objects (VBO). They can store a massive amount of vertices in the GPU's memory meaning we can send massive batches of data to the GPU all at once.








