# SPL
Simple Programming Language

/- The following is the planned grammar for SPL (Simple Programming Language), it is incomplete and in partial BNF notation as I can't yet seem to get BNF notation wrapped around my head. I plan on using BNF Converter (http://bnfc.digitalgrammars.com/) to compile the front end of the SPL compiler. Rather than clog up the grammar with comments to explain each line I will put a number at the line and that will be the reference to the foot note.-/
--------------------------------------------------------------------------------------------------------------------------------
library includes::= library ; [library_name] . / end [1]

program entry point::= start [program_name] ; declarations statements . / end [2]

declare function::= [function_name] , arguments ; statements . / end [3]

declare an object::= create , object , name ; atribute : expression . / end | create , object , name ; atribute : expression . [4]

declare multiple objects::= create; object ,  name . / end [5]

set attributes for an object::=o.name ; atribute : expression . [6]

if statement::= if , condition ; statements . / end | if , condition ; statement . [7]
if else ::= if, condition ; statements . else ; statements . / end
if eif else ::= if , condition ; statements . eif , condition ; statements . else ; statements . / end

choose statement::= choose , expression ; opt , statements . else ; statements . / end [8]

loop statement::= loop , condition ; statements . / end [9]

assignment::= declaration : expression

exponents::= expression ** expression
multiply::= expression * expression
divide::= expression / expression
modulo::= expression \ expression
add::= expression + expression
subtract::= expression - expression

greater than::= expression > expression
less than::= expression < expression
greater than or equal to::= expression >= expression
less than or equal to::= expression <= expression

increment by one::= expression =>
deincrement by one:: expression =< 
increment by n:: expression =n>
deincrement by n::= expression =n<
absolute value::= --expression--

equals::= "="
not equal::= "!="

data types::= integer double bool hex string

single line comment::= // comments
multi line comment::= /- comments -/
---------------------------------------------------------------------------------------------------------------------------------
Foot Notes:

1. equivilent to the Include statement in other languages like C and C++ but it is meant to be a block of code to include multiple libraries without retyping the include statement over and over.

2. program entry point roughly equivilent to int main() { } in C and C++

3. function declaration but without the use of the key word function. example: myfunction, [optional arguments here]; statements. /end

4. single object declaration. An object can be anything from a variable, a gui object, etc.
	example: create, string, x; value:'This is a string.'.

In the above example we created a string variable and assigned its only atribute called value with the text, 'This is a string.' and simply ended it with a period. If there were multiple atributes to assign then the block format ending with /end is required.

5. multiple object declarartions is used to declare more than one object without assigning any atributes.
	example: 
create; 
string, x.
integer, num.
messagebox, msg.
/end

6. setting atributes for previously created objects can be done by the following example which will make use of the previous example.
	example:
o.x; value:'This is a string.'.
o.num; value:5.
o.msg; prompt:'This is a message box.', button: Ok.

7. a single if statement with only one statement after the condition can end with a period. Multiple statements must end in block format /end.
	example:
if, a = 5; f.[function_name];.

if, a = 5;
f.myfunction.//calls a function named myfunctions
show, o.msg.
/end

8. this is roughly equivilent to the switch case statement in C and C++.
	example:
choose, o.items;
item 1, print:'price is: ' o.price1.
item 2, print:'price is: ' o.price2.
/end

9. there is only one planned looping statement but in theory can be used in many different ways.
	example 1:
loop, times:5;//will loop 6 times starting at zero, equivilent to for loop.
print:'This is a loop.'.
/end
	example 2:
loop, if, o.a != 5; //assume a = to 10
o.a =<
/end
	example 3:
loop, times:5 - 1; //will loop 5 times starting at 0.
o.a =<
/end

	example 4:
loop, times:(5 -1) + 1; // will loop 5 times starting at 1.
o.a =<
/end


