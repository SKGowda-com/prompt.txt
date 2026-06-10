# prompt.txt
Write a complete C program that implements an interactive 2D ASCII graphics editor in the terminal. The program should maintain a canvas of 40 rows by 80 columns of characters and support the following features:
Shapes to draw:
Line — using Bresenham's line algorithm; horizontal segments use _, all other segments use *
Rectangle — outline only; top/bottom edges use _, left/right edges use *, corners always use *
Triangle — outline only, drawn by connecting three vertices with lines
Circle — outline only using the midpoint circle algorithm; top/bottom arcs use _, side arcs use *
Program behavior:
Display a numbered menu loop: Add Line, Add Rectangle, Add Triangle, Add Circle, Delete Object, Display Picture, List Objects, Clear All, Exit
Each shape is stored in an object list (max 50) with a unique integer ID and all its parameters
When adding a shape, prompt the user for the necessary coordinates/dimensions via scanf
After every add or delete, call a redrawAll() function that clears the canvas and redraws every object from scratch
Delete by ID: show the current object list, prompt for an ID, remove it and redraw
Display the canvas surrounded by a +---+ border using printf/putchar
List objects in a formatted table showing ID, type name, and parameters
Use a single generic Object struct with a type int, an id int, and a p[6] int array whose meaning varies by shape type
Use only standard C libraries (stdio.h, stdlib.h, string.h, math.h). No dynamic memory allocation — use fixed-size global arrays throughout.
