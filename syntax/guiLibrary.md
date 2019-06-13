//Syntax
gui.Object, [ObjectName];

Example:
//Create a window with all the defaults
gui.window, main;

//Set object properties at creation

gui.Object, [ObjectName]:
  propertyName: [value] ;
[ObjectName].

Example:

gui.window, main:
  size: 480, 640;
main.

//Set object properties after creation

gui.Object, [ObjectName];

[ObjectName]:
  property: [value];
[ObjectName].

Example:

gui.window, main;

main:
  size: 480, 640;
main.

Objects:

window
textBox
checkBox
radioButton
button
inputBox
messageBox
listBox
imageBox
groupBox
selectBox
