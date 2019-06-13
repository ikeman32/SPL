**Syntax**
choice, [param]:
[choice1]:
  [code];
[choice2]:
  [code];
[default]://optional
  [code];
choice.

**Example:**
choice, varNumber:
1:
  print, "This is the first choice";
2: 
  print, "This is the second choice";
default:
  print, "This is the default choice";
choice.
