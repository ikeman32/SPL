//Loop a specific amount of times
loop,[var], [condition], [var++]:
  [code];
loop.

Example:
loop, a = 0, a < 10, a++:
  print, a;
loop.

//loop while a condition is true
loop, [condition]:
  [code];
loop.

Example:

loop, a < 10:
  print, a;
  a ++;
loop.
