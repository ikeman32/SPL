These concepts are a work in progress and may require a change in grammar.

**IF Statment**
// single if block
if, condition:
  code;
if.

//if, else block
if, condition:
  code;
else:
  code;
if.

// multiple if blocks with optional else
if, condition:
  code;
condition:
  code;
condtion:
  code;
else:
  code;
if.

**CHOICE Statement**

choice, arg:
[choice1]:
  code;
[choice2]:
  code;
default:
  code;
choice.

**Loops**
// basicly a for loop
loop, var, condition, var ++:
  code;
loop.

// basically a while loop
loop, while, condition:
  code.
loop.

**GUI**
SPL to have a built in gui library

//declare a gui object 
gui.[object], [object name];

//example declare a window
gui.window, mainWindow;

//set gui object properties
mainWindow, properties:
size: x, y;
buttons: [default]//sets all three usual buttons
         [close]//only the close button
         [min]//minimize and close button
mainWindow.
