## Creating a window

The first step before creating graphics is creating an OpenGL context and
a window to draw that context in. OpenGL purposefully abstracts itself from The
window and context creation process because it is platform dependent.


## GLFW
is a library that allows us to create an openGL context and window on any
platform.



## Explaining the code.

Theres some big concepts to get here that are really importnat. 

Firstly - The purpose of everyrything.

GLFW -> To create the OpenGL context and window for us. An Abstrction.
GLAD -> Manages OpenGL function pointers. We need to init this before we call any openGL functions. 
OpenGL -> The actual library that GLFW calls upon to do its window making and such.

### The steps

1: Initialize GLFW and give it data such as the version to use and if it is forward compatable.
2: Create a GLFW window.
3: Make the GLFW context the newly created window.
4: Initialize GLAD using gladLoadGLLoader (now we can call openGL functions)
5: set the glViewport with glViewport()
6: while (glfwWindowShouldNotClose) do all your rendering, input, etc.
7: terminate GLFW.

