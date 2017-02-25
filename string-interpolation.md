Allows string literals with embedded expressions in them; a template string uses back ticks instead of double quotes or single quotes. The template string can contain place holders, which use the ${ } syntax.

**Examples:**

Default template string:  
`var x = 1;`  
`var y = 2;`  
``${ x } + ${ y } = ${ x + y}`  // "1 + 2 = 3"`  

Multiline string:  
console.log(`string text line 1

string text line 2`);  
// "string text line 1  
// string text line 2"