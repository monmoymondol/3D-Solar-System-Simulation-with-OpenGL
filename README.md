CHAPTER 1
INTRODUCTION
1.1 COMPUTER GRAPHICS
Computer Graphics is concerned with all aspect of producing pictures or image using computer. The field began humble almost 50 years ago, with the display of few lines on the cathode-ray tube (CRT); now, we can create image using computer that are indistinguishable from photographs from the real objects. We routinely train pilots with simulated airplane, generating graphical display of the virtual environment in the real time. Feature length movies made entirely by computer have been successful, both critically and financially; massive multiplayer game can involve tens of thousands of concurrent participants.
Graphics is created using computers and, more generally, the representation and manipulation of pictorial data by a computer. The development of computer graphics has made computers easier to interact with and better for understanding and interpreting many types of data. Developments in computer graphics have had a profound impact on many types of media and have revolutionized the animation and video game industry. The phrase “Computer Graphics” was coined in 1960 by William Fetter, a graphic designer for Boeing. In today’s world advanced technology, interactive computer graphics has become a powerful tool for the production of realistic features. Today’s we find computer graphics used in various areas that include science, engineering, medicine, business, industry, art, entertainment etc. The main reason for effectiveness of the interactive computer graphics is the speed with which the user can understand the displayed information.
The graphics in OpenGL provides a wide variety of built-in function. The computer graphics remains one of the most exciting and rapidly growing computer fields. It has become a common element in user interface, data visualization, TV commercials, motion picture and many other applications. The current trend of computer graphics is to incorporate more physics principles into 3D graphics algorithm to better simulate the complex interactions between objects and lighting environment.
1.2 OPEN-GL: HISTORY
OpenGL was developed by ‘Silicon Graphics Inc ‘(SGI) on 1992 and is popular in the gaming industry where it competes with the Direct3D in the Microsoft Windows platform. OpenGL is broadly used in CAD (Computer Aided Design), virtual reality, scientific visualization, information visualization, flight simulation and video games development.
OpenGL is a standard specification that defines an API that is multi-language and multi-platform and that enables the codification of applications that output computerized graphics in 2D and 3D. The interface consists in more than 250 different functions, which can be used to draw complex tridimensional scenes with simple primitives. It consists of many functions that help to create a real-world object and a particular existence for an object can be given.
1.3 OPEN-GL INTERFACE:
OpenGL is an application program interface (API) offering various functions to implement primitives, models and images. This offers functions to create and manipulate render lighting, coloring, viewing the models. OpenGL offers different coordinate system and frames. OpenGL offers translation, rotation and scaling of objects. Most of our applications will be designed to access OpenGL directly through functions in three libraries. They are:
1. Main GL: Library has names that begin with the letter gl and are stored in a library usually referred to as GL.
2. OpenGL Utility Library (GLU): This library uses only GL functions but contains code for creating common objects and simplifying viewing.
3. OpenGL Utility Toolkit (GLUT): This provides the minimum functionality that should be accepted in any modern windowing system.
CHARECTERISTICS
 OpenGL is a better documented API.
 OpenGL is also a cleaner API and much easier to learn and program.
 OpenGL has the best demonstrated 3D performance for any API.
CHAPTER 2
REQUIREMENT ANALYSIS
2.1 SYSTEM REQUIREMENTS
i. Hardware Requirements:
 Processor- Intel or AMD (Advanced Micro Devices)
 RAM- 1 GB (minimum)
 Hard Disk- 40MB (minimum)
 Graphics Memory- 128MB
ii. Software Requirements:
 Operating system
 Compiler
 Graphics library
2.2 FUNCTIONAL REQUIREMENTS
OpenGL APIs: If we want to have a control on the flow of program and if we want to interact with the window system then we use OpenGL API’S. Vertices are represented in the same manner internally, whether they are specified as two-dimensional or three-dimensional entities, everything that we do are here will be equally valid in three dimensions. Although OpenGL is easy to learn, compared with other APIs, it is nevertheless powerful. It supports the simple three-dimensional programs and also supports the advanced rendering techniques.
GL/glut.h: We use a readily available library called the OpenGL Utility Toolkit (GLUT), which provides the minimum functionality that should be expected in any modern windowing system. The application program uses only GLUT functions and can be recompiled with the GLUT library for other window system. OpenGL makes a heavy use of macros to increase code readability and avoid the use of magic numbers. In most implementation, one of the include lines.
CHAPTER 3
IMPLEMENTATION
3.1 FUNCTIONS IN OPEN-GL
 void glClear(glEnum mode); Clears the buffers namely color buffer and depth buffer. mode refers to GL_COLOR_BUFFER_BIT or DEPTH_BUFFER_BIT.
 void glTranslate[fd](TYPE x, TYPE y, TYPE z); Alters the current matrix by displacement of (x, y, z), TYPE is either GLfloat or GLdouble.
 void glutSwapBuffers(); Swaps the front and back buffers.
 void glMatrixMode(GLenum mode); Specifies which matrix will be affected by subsequent transformations, Mode can be GL_MODELVIEW or GL_PROJECTION.
 void glLoadIdentity( ); Sets the current transformation matrix to identity matrix.
 void glEnable(GLenum feature); Enables an OpenGL feature. Feature can be GL_DEPTH_TEST (enables depth test for hidden surface removal), GL_LIGHTING (enables for lighting calculations), GL_LIGHTi (used to turn on the light for number i), etc.
 void glPushMatrix(); void glPopMatrix(); Pushes to and pops from the matrix stack corresponding to the current matrix mode.
 void glutBitmapCharacter(void *font, int character); Without using any display lists, glutBitmapCharacter renders the character in the named bitmap font. The fonts used are GLUT_BITMAP_TIMES_ ROMAN_24, GLUT_BITMAP_ HELVETICA_18.
 void glRasterPos[234][ifd](GLfloat x, GLfloat y, GLfloat z); This position, called the raster position, is used to position pixel and bitmap write operations.
 void glOrtho(GLdouble left, GLdouble right, GLdouble bottom, GLdouble top, GLdouble near, GLdouble far); Defines an orthographic viewing volume with all the parameters measured from the centre of the projection plane.
 void glutInit(int *argc, char **argv); Initializes GLUT; the arguments from main are passed in and can be used by the application.
 void glutInitDisplayMode(unsigned int mode); Requests a display with the properties in the mode; the value of mode is determined by the logical OR of options including the color model (GLUT_RGB, GLUT_INDEX) and buffering (GLUT_SINGLE, GLUT_DOUBLE).
 void glutCreateWindow(char *title); Creates a window on display; the string title can be used to label the window. The return value provides a reference to the window that can be used when there are multiple windows.
 void glutDisplayFunc(void (*func)(void)) Registers the display function func that is executed when the window needs to be redrawn.
 void glutMouseFunc(void *f(int button, int state, int x, int y) Registers the mouse callback function f. The callback function returns the button (GLUT_LEFT_BUTTON,etc., the state of the button after the event (GLUT_DOWN), and the position of the mouse relative to the top-left corner of the window.
 void glutKeyboardFunc(void *f(char key, int width, int height)) Registers the keyboard callback function f. The callback function returns the ASCII code of the key pressed and the position of the mouse.
 void glClearColor(GLclampf r, GLclampf g, GLclamp b, Glclamp a) Sets the present RGBA clear color used when clearing the color buffer. Variables of type GLclampf are floating point numbers between 0.0 and 1.0.
 void glViewport(int x ,int y, GLsizei width, GLsizei height) Specifies the width*height viewport in pixels whose lower left corner is at (x,y) measured from the origin of the window.
 void glColor3[b I f d ub us ui](TYPE r, TYPE g, TYPE b) Sets the present RGB colors. Valid types are bytes(b), int(i), float(f), double(d), unsigned byte(ub), unsigned short(us), and unsigned int(ui). The maximum and minimum value for floating point types are 1.0 and 0.0 respectively, whereas the maximum and minimum values of the discrete types are those of the type, for eg, 255 and 0 for unsigned bytes.
 void glutInitWindowSize(int width, int height); Specifies the initial height and width of the window in pixels.
 void glutReshapeFunc(void *f(int width, int height)); Registers the reshape callback function f. the callback function returns the height and width of the new window. The reshape callback invokes the display callback.
 void createMenu(void); This function is used to create menus which are used as options in program.
CHAPTER 4
TESTING
4.1 TESTING PROCESS
Testing process started with the testing of individual program units such as functions or objects. These were then integrated into sub-systems and systems, and interactions of these units were tested.
Testing involves verification and validation.
 Validation: “Are we building right product?”
 Verification: “Are we building the product right?”
The ultimate goal of the verification and validation process is to establish confidence that the software system is ‘fit for purpose’. The level of required confidence depends on the system’s purpose, the expectations of the system users and the current marketing environment for the system.
With the verification and validation process, there are two complementary approaches to the system checking and analysis:
Software inspections or peer reviews analyses and check system representations such as the requirements document, design diagrams, and the program source code. Software testing involves running an implementation of the software with test data.
CHAPTER 5
EXPERIMENTAL RESULTS AND ANALYSIS
The project designed has been tested for its working, and is found to be working properly to meet all its requirements.
The designed project has been tested for errors and has been found to be meeting all the requirements of design with which it was started. Thus, the project is declared to be working properly.
Working of the project is explained through snapshots as follows.
5.1 SNAPSHOT
CONCLUSION
After the completion of this project, we came to know how we can implement a project using an Open-source OpenGL tool kit. By implementing a project using Open GL we came to know how to use the functions like menu ‘s, rotation, translation and scaling. With the completion of this project, we have achieved a sense of happiness and we want to thank all those who helped us directly or indirectly to make this idea come true.
REFERENCES
[1]. Edward Angel, Interactive Computer Graphics A Top-Down Approach with OpenGL, 5th Edition, Addison-Wesley, 2008.
[2]. F.S. Hill,Jr, Computer Graphics Using OpenGL. 2nd Edition, Pearson Education, 2001.
[3]. James D Foley, Andries Van Dam, Steven K Feiner, John F Hughes, Computer Graphics –Addison-Wesley 1997.
[4]. Donald Hearn and Pauline Baker, Computer Graphics - OpenGL Version –2nd Edition, Pearson Education, 2003.
SOURCE CODE
