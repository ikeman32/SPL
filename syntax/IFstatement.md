**Syntax**
//Single if block
if, [condition]:
  [code];
if.

Example:
if, a + b == c:
  print, "Condition is true";
if.

//if else block
if, [condition]:
  [code];
else:
  [code];
if.

Example:
if, a + b == c:
  print, "Condition is true";
else:
  print, "Condition is false";
if.

//Multiple if conditions with optional else block
if, [condition]:
  [code];
[condition]:
  [code];
[condition]:
  [code];
else:
  [code];
if.

Example:
if, a + b == c:
  print, "Condition is true";
a + b == d:
  print, "Condition is true";
a + b = e:
  print, "Condition is true";
else:
  print, "Condition is false";
