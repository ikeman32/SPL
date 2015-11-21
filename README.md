# SPL
Simple Programming Language

A language that is structured for a novice with syntax that is more human readable and less complicated for the beginner to learn.

Basic structure for a program Hello World

Create:
Window mainw;
Text text1;
Button button1.
*/
Explanation: The Create commant tells the compiler that you want to create an object while the colon ":" tells the compiler that you want to create several objects.

The semicolon ";" is the list item separator while the period "." tells the comipler that you are done creating objects. Syntax for creating objects is Object name separator. Where the Object is any object that can be created such as a GUI Window. The name is any unique identifiet the developer choses and the separator is either a semicolon or a period.
/*

Hello World program continued.

Define mainw:
Size default;
TitleBar standard;
Title Text, 'Hello World';
StatusBar no.

*/
Basically this tells the compiler that you want to define the parameters of the object named mainw.
/*

Define button1 Text, 'Ok'.

Define text1 Text, 'Hello World!'.

Collect mainw:
text1 Middle, Center;
button1 Under text1.

Events:
button1 Click, Exit.

*/
How it all works.

When a command is invoked the compiler then consults the command library the tells the compiler which Library to go to for instructions to carry out the command. For instance the Create command instructs the Compiler to go the the Object library which then gives all the complex instructions to create the objects specified. So when you tell the compiler to Create a Window named mainw it looks up the Window object and constructs a widow with all the defaults . When you subsiquently Define thw Window named mainw you are telling the compiler to change the atributes from the defaults.

After you create snd define your objects you collect them and arraigne them it the fashion you choose. Then would define any Events that might happen when a user interacts with the program, in this case the click Event for the button.

Complex events not already defined in the compuler's library can be defined by the developer in a set of functions or sub routine called an Instruction which has the following construct:

Instrution name:
Arg1;
Arg2;
Etc.

/*

To keep a program from becoming crowded with developet defined Instructions they can be place in a new library and linked to the main program with the Include command:

Include;
Libray1;
Libray2;
etc.

That is the gist of the concept with the goal of making the coding process easier for beginners without a lot of complex syntax. A more in depth description of the language will be in the wiki.
