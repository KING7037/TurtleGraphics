# TurtleGraphics

This Java-based Turtle Graphics Application is an interactive drawing tool that allows users to control a virtual "turtle" to create geometric designs. Built using Swing for the GUI and extending the LBUGraphics framework, it provides a simple yet powerful way to learn programming concepts through visual feedback.

Core Features
A. Graphical User Interface (GUI)
•	Main Drawing Canvas: The turtle moves and draws on a JPanel.
•	Control Buttons: Includes buttons for common commands (pendown, penup, clear, reset).
•	Command Input Field: Users can type commands (e.g., move 100, left 90).
•	Command History Panel: Displays previously executed commands in a scrollable list.
•	Message Box: Shows feedback and error messages.
•	Menu Bar: Provides file operations (Save Image, Load Image, Exit) and help options.


B. Drawing Functionality
•	Movement & Rotation:
o	forward(distance) – Moves the turtle forward.
o	reverse(distance) – Moves backward.
o	left(angle) / right(angle) – Rotates the turtle.
•	Pen Control:
o	pendown – Enables drawing.
o	penup – Disables drawing.
•	Shapes:
o	square(size) – Draws a square.
o	triangle(size) – Draws an equilateral triangle.
o	triangle(a, b, c) – Draws a custom triangle.
•	Color & Styling:
o	Predefined colors (black, red, green, white).
o	Custom RGB colors (pencolour R G B).
o	Adjustable pen width (penwidth value).


C. File Operations
•	Save/Load Images: Exports drawings as .png files.
•	Save/Load Commands: Stores and retrieves command history in commands.txt.


D. Special Functions
•	about(): Draws the creator's initials ("RAJ") using turtle movements.
•	Nepal(): Attempts to draw a stylized Nepali flag (experimental).
•	Undo/Redo (Potential Enhancement): Currently tracks history but lacks undo functionality.


Technical Implementation
A. Class Structure
•	Extends LBUGraphics (a custom graphics framework).
•	Uses Swing Components (JFrame, JPanel, JButton, JTextArea).
•	Manages command history using ArrayList<String>.
•	Handles file I/O for saving/loading images (ImageIO) and commands (BufferedReader, BufferedWriter).


B. Key Methods
1.	processCommand(String command)
o	Parses and executes user commands using a switch-case structure.
o	Validates inputs (e.g., checks if movement keeps turtle on-screen).
o	Updates the command history and message box.


3.	saveImage() & loadImage()
o	Uses JFileChooser for file selection.
o	Converts the drawing panel into a BufferedImage for saving.


4.	drawSquare(), drawEquilateralTriangle(), drawTriangle()
o	Use geometric calculations to draw shapes with turtle movements.

5.	Error Handling
o	Catches NumberFormatException for invalid numbers.
o	Displays user-friendly error messages via JOptionPane.


Conclusion
This Turtle Graphics Application is a versatile tool for that combines Java Swing, file handling, and geometric algorithms to create an interactive drawing experience. With additional enhancements, it could serve as a powerful educational platform for beginners in computer science.

Command Reference
Command	Parameters	Description
about	none	Shows introductory drawing
penup	none	Lifts the pen (stops drawing)
pendown	none	Lowers the pen (starts drawing)
left	degrees	Turns turtle left by specified angle
right	degrees	Turns turtle right by specified angle
move	distance	Moves turtle forward by specified distance
reverse	distance	Moves turtle backward by specified distance
black/red/green/white	none	Sets pen color
pencolour	R G B	Sets custom pen color (0-255 values)
penwidth	width	Sets pen thickness
square	size	Draws a square with given side length
triangle	size	Draws equilateral triangle
triangle	a b c	Draws triangle with specified sides
clear	none	Clears the drawing
reset	none	Resets turtle position and direction
nepal	none	Draws Nepal flag representation
saveimage	none	Saves drawing as PNG file
loadimage	none	Loads drawing from PNG file
savecommands	none	Saves command history to file
loadcommands	none	Loads commands from file
