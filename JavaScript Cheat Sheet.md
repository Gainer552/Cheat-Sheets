# 𝗦𝗵𝗲𝗯𝗮𝗻𝗴

- `// Not required in JavaScript (used in Node.js optionally):`
- `#!/usr/bin/env node` - Declares a Node.js script when run from CLI.

# 𝗘𝗺𝗯𝗲𝗱𝗱𝗲𝗱 𝗖𝗼𝗱𝗲 𝗕𝗹𝗼𝗰𝗸

- `/*`
- `Multi-line comment block.`
- `Used for documentation or disabling code.`
- `*/`

# 𝗘𝘀𝘀𝗲𝗻𝘁𝗶𝗮𝗹 𝗝𝗮𝘃𝗮𝗦𝗰𝗿𝗶𝗽𝘁 𝗕𝘂𝗶𝗹𝘁-𝗶𝗻 𝗢𝗯𝗷𝗲𝗰𝘁𝘀

### Global & Utility

- `console` - Logging/debugging (`log`, `error`, `warn`).
- `Math` - Math operations (`random`, `floor`, `ceil`).
- `Date` - Date/time handling.
- `JSON` - Parse/stringify data.

### DOM

- `document` - Access HTML document.
- `window` - Browser global object.

# 𝗗𝗮𝘁𝗮 𝗧𝘆𝗽𝗲𝘀

- `String (Str)` - `"Hello"`
- `Number (Num)` - `10`, `3.14`
- `BigInt` - `123n`
- `Boolean (Bool)` - `true/false`
- `Undefined` - Declared but not assigned.
- `Null` - Intentional empty value.
- `Symbol` - Unique identifier.

### Complex Types

- `Object {}` - Key-value structured data, mutable, reference-based.
- `Array []` - Ordered list, index-based, dynamic.
- `Function () {}` - Reusable block of logic, first-class object.

# 𝗥𝗲𝘀𝗲𝗿𝘃𝗲𝗱 𝗪𝗼𝗿𝗱𝘀/𝗞𝗲𝘆𝘄𝗼𝗿𝗱𝘀

- `break`, `case`, `catch`, `class`, `const`, `continue`, `debugger`
- `default`, `delete`, `do`, `else`, `export`, `extends`, `finally`
- `for`, `function`, `if`, `import`, `in`, `instanceof`, `let`, `new`
- `return`, `super`, `switch`, `this`, `throw`, `try`, `typeof`
- `var`, `void`, `while`, `with`, `yield`, `async`, `await`

# 𝗢𝗽𝗲𝗿𝗮𝘁𝗼𝗿𝘀

### Logical Operators

- `//` - Comment.
- `+` - Addition / concatenation.
- `- * / % **` - Arithmetic.
- `== === != !==` - Comparison.
- `> < >= <=` - Relational.
- `&&` - AND.
- `||` - OR.
- `!` - NOT.
- `??` - Nullish coalescing.
- `?.` - Optional chaining.

# 𝗦𝗰𝗼𝗽𝗲

- `Global` - Accessible everywhere.
- `Function` - Scoped to function.
- `Block` - Scoped to `{}` (`let/const`).

# 𝗤𝘂𝗼𝘁𝗶𝗻𝗴

- `''` - Literal string.
- `""` - Allows interpolation.
- `` `template ${value}` `` - Template literals with interpolation.

# 𝗔𝗿𝗿𝗮𝘆 𝗠𝗲𝘁𝗵𝗼𝗱𝘀

- `push()` - Add to end.
- `pop()` - Remove from end.
- `shift()` - Remove from start.
- `unshift()` - Add to start.
- `map()` - Transform array.
- `filter()` - Filter elements.
- `reduce()` - Reduce to single value.
- `find()` - Find first match.

# 𝗖𝗼𝗻𝘁𝗿𝗼𝗹 𝗙𝗹𝗼𝘄

- `if / else` - Conditional logic.
- `switch` - Multi-branch condition.
- `for` - Loop.
- `while` - Loop.
- `do...while` - Loop.

# 𝗚𝗿𝗼𝘂𝗽𝗶𝗻𝗴

- `{}` - Block scope.
- `()` - Function execution.
- `[]` - Array literal.

# 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀

## 𝗚𝗲𝗻𝗲𝗿𝗮𝗹 𝗧𝘆𝗽𝗲𝘀

### 𝗩𝗮𝗿𝗶𝗮𝗯𝗹𝗲 (𝗩𝗮𝗿)

- `let x = 10;`
- `const y = 20;`

### 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻 (𝗙𝘂𝗻𝗰)

- `function greet() {`
- `    console.log("Hello world!");`
- `}`

## 𝗖𝗼𝗻𝗱𝗶𝘁𝗶𝗼𝗻𝗮𝗹 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁𝘀

### 𝗜𝗳 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁

- `let num = 5;`
- `if (num > 3) {`
- `    console.log("Greater than 3");`
- `}`

### 𝗜𝗳/𝗘𝗹𝘀𝗲 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁

- `if (num > 10) {`
- `    console.log("Big");`
- `} else {`
- `    console.log("Small");`
- `}`

## 𝗟𝗼𝗼𝗽𝘀

### 𝗙𝗼𝗿 𝗟𝗼𝗼𝗽

- `for (let i = 0; i < 5; i++) {`
- `    console.log(i);`
- `}`

### 𝗪𝗵𝗶𝗹𝗲 𝗟𝗼𝗼𝗽

- `let i = 0;`
- `while (i < 5) {`
- `    console.log(i);`
- `    i++;`
- `}`

## 𝗔𝗿𝗿𝗮𝘆𝘀

- `const arr = [1, 2, 3];`
- `arr.forEach(n => console.log(n));`

## 𝗢𝗯𝗷𝗲𝗰𝘁

- `const obj = {`
- `    name: "John",`
- `    age: 30`
- `};`
- `console.log(obj.name);`

## 𝗔𝘀𝘆𝗻𝗰

- `async function getData() {`
- `    const res = await fetch("https://api.example.com");`
- `    const data = await res.json();`
- `    console.log(data);`
- `}`