## What Is Rendering

Reference: [Rendering - Wikipedia](https://en.wikipedia.org/wiki/Rendering_(computer_graphics))

In the traditional sense, rendering is the process of turning code into a colorful page.  
Modern rendering usually refers to a creative act that increases an image's realism and richness by adding depth, detail, lighting, and shadow. In embedded systems, rendering can be the process of converting graphical content into images or video that can be displayed on an embedded device screen. This process involves technologies and tools such as lighting, materials, textures, and visual effects, with the goal of making content appear more realistic and vivid. Unlike a GUI library, it is one part of a GUI, specializing in rendering and shading visual effects and requiring extensive computation and drawing.  

The concept of "rendering" is abstract on the embedded side. In pure software, rendering usually means using machine-readable text or code to **"produce a final image for people to see"**, such as a browser rendering HTML/CSS into a web page or a game engine rendering a 3D scene.  
In embedded systems, the word "rendering" is borrowed, but its core meaning becomes **"converting abstract data or state into specific instructions that drive hardware"**. Compared with pure software, this adds adaptation for the display terminal.  
Therefore, when coming from software to embedded systems, rendering can feel abstract because you expect it to mean "drawing", while it actually performs the work of "translation and driving".  

Of course, it can also be understood as drawing basic shapes such as points, circles, and rectangles. However, this drawing spans two layers. Like memory, display has software and hardware layers: software is the GUI drawing library, while hardware drives the screen illumination.  

---
