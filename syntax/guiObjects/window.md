Desription of the window Object and its properties

Window:
//Syntax

gui.window, [NameOfWindow];

Properties:

size: [x, y];//set the width and height of the window
parent: [true|false];//set to boolean value to determin if the window is a parent window default true.
title: [stringValue];//set the string value of the window title bar.
status: [true|false];//set the visibility of the status bar to true or false, default false.
vScroll: [true|false];
hScroll: [true|false];
clients: [Object List];//List of all gui objects attached to the window body, containers, textBox, etc.
