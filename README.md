# MAD2ENDSEM

Certainly! I will provide a detailed explanation and solution for each question from both the **practice** and **graded** sections in your document. Since the document is extensive, I will break it down week by week. Here's how I will proceed:

1. Solve and explain all the **graded questions** for Week 1.
2. Solve and explain all the **practice questions** for Week 1.
3. Repeat this process for all subsequent weeks.

If the response exceeds the character limit, I'll continue in subsequent replies. Let’s begin with **Week 1 Graded Questions**:  

---

### **Week 1 Graded Questions**

#### Q1: Which of the following keywords can be used to declare a variable with global scope?
- **Options**: `let`, `var`, `const`, `All of the above`
- **Answer**: **D. All of the above**
- **Explanation**: In JavaScript, global scope is achieved when a variable is declared outside of any function. `let`, `var`, and `const` can all be used for this purpose. However, their behavior differs slightly:
  - `var` creates a global variable if declared outside a function or in the `window` scope.
  - `let` and `const` create block-scoped variables but are still global if declared outside any block.

---

#### Q2: Which of the following statements is true regarding JavaScript language?
- **Options**:  
  - JavaScript is a statically typed language.  
  - JavaScript is a dynamically typed language.  
  - JavaScript is a weakly typed language.  
  - JavaScript is a strongly typed language.  
- **Answer**: **B and C**
- **Explanation**:  
  - JavaScript is a **dynamically typed language** because variable types are determined at runtime, not during compilation.  
  - It is also a **weakly typed language** because it allows implicit type conversions, which may lead to unexpected results.

---

#### Q3: Which of the following statements is correct regarding JavaScript?
- **Options**:  
  - A: It is a forgiving language like HTML.  
  - B: It inserts a semicolon after each statement automatically.  
  - C: Blocks and functions both use `{}` for body contents.  
  - D: Blocks use `{}`, but functions use indentation for body contents.  
- **Answer**: **A, B, and C**
- **Explanation**:  
  - JavaScript is considered "forgiving" due to features like coercion and auto-semicolon insertion.  
  - Both functions and blocks use `{}` to define their body, unlike Python, which relies on indentation.

---

#### Q4: Predict the last value shown on the console for the given program involving `setInterval` and `setTimeout`.
- **Options**:  
  - 4  
  - 8  
  - 5  
  - 10  
- **Answer**: **B. 8**
- **Explanation**:  
  - The `setInterval` function doubles the value of `x` every second and stops after 5 seconds using `clearInterval`. The sequence logged is `2, 4, 6, 8`. The last value logged is `8`.

---

#### Q5: Output of the following code snippet:
```javascript
const x = { name: 'Rohit' };
x.name = 'Mohit';
console.log(x.name);
```
- **Options**:  
  - A: It will throw a TypeError.  
  - B: Rohit  
  - C: Mohit  
  - D: undefined  
- **Answer**: **C. Mohit**
- **Explanation**:  
  - The `const` keyword makes the reference to the object constant, but the properties of the object can still be modified. Here, `x.name` is updated to `'Mohit'`.

---

#### Q6: Predict the output of a program using an arrow function.
- **Options**:  
  - A: undefined  
  - B: Rohit  
  - C: Mohit  
  - D: null  
- **Answer**: **B. Rohit**
- **Explanation**:  
  - Arrow functions don’t have their own `this`. Instead, they inherit it from the surrounding scope. As a result, the `name` property of the `obj` remains `'Rohit'`.

---

#### Q7: Analyze the output of a program using both arrow and normal functions.
- **Options**:  
  - A: Rohit  
  - B: Mohit  
  - C: undefined  
  - D: Syntax Error  
- **Answer**: **A. Rohit**
- **Explanation**:  
  - Arrow functions inherit the `this` value from the parent scope. Since `arrowFunction` is defined inside `normalFunction`, it uses `this` from the `obj`, which resolves to `'Rohit'`.

---

#### Q8: Determine the correct output of a program using `setTimeout` and `console.log`.
- **Options**:  
  - A. Logs are interleaved (asynchronous).  
  - B, C, D: Variations of log order.  
- **Answer**: **D**
- **Explanation**:  
  - Synchronous `console.log` calls execute before asynchronous `setTimeout` logs.

---

#### Q9: Background color of an element with `setTimeout`.
- **Options**: Red, Black, Yellow, None of the above.  
- **Answer**: **C. Yellow**
- **Explanation**:  
  - The `setTimeout` callback changes the background color to `'yellow'` after a delay, overriding the initial `'red'`.

---

#### Q10: Analyze output from a JavaScript program using `split`, `pop`, and `setInterval`.
- **Options**: Various characters from a string.  
- **Answer**: **C. n**  
- **Explanation**:  
  - After 4 seconds, the character `'n'` is popped and logged, as the loop processes the string `'orange'`.



---

### **Week 1 Graded Questions**

---

#### **Q1: Which of the following keywords can be used to declare a variable with global scope?**
- **Options**:  
  1. `let`  
  2. `var`  
  3. `const`  
  4. All of the above  

- **Answer**: **4. All of the above**

---

#### **Detailed Explanation**:

In JavaScript, the scope of a variable determines where it can be accessed in a program. The three key ways to declare variables (`let`, `var`, and `const`) behave differently when used in global or block scope.

1. **`var`:**  
   Variables declared using `var` are globally scoped if they are not declared inside a function. Example:
   ```javascript
   var globalVar = "I am global!";
   console.log(window.globalVar); // Output: "I am global!"
   ```
   However, `var` has function scope, meaning if it’s declared inside a function, it cannot be accessed outside.

2. **`let`:**  
   Variables declared with `let` are **block scoped**. However, if declared outside any block, they behave as global variables:
   ```javascript
   let globalLet = "I am also global!";
   console.log(globalLet); // Output: "I am also global!"
   ```

3. **`const`:**  
   Similar to `let`, variables declared with `const` are block-scoped but can have global behavior when declared outside any block:
   ```javascript
   const globalConst = "I am constant!";
   console.log(globalConst); // Output: "I am constant!"
   ```

### **Key Differences Between These Declarations:**

| Feature           | `var`                  | `let`                  | `const`                |
|--------------------|------------------------|------------------------|------------------------|
| Scope             | Function or Global     | Block or Global        | Block or Global        |
| Reassignment      | Allowed               | Allowed               | Not allowed           |
| Hoisting          | Yes, but undefined     | Yes, in Temporal Dead Zone | Yes, in Temporal Dead Zone |

**Global Scope**: All three (`var`, `let`, and `const`) create global variables if declared outside a block. Hence, the correct answer is **"All of the above"**.

---

#### **Q2: Which of the following statements is true regarding JavaScript language?**
- **Options**:  
  1. JavaScript is a statically typed language.  
  2. JavaScript is a dynamically typed language.  
  3. JavaScript is a weakly typed language.  
  4. JavaScript is a strongly typed language.  

- **Answer**: **2 and 3**

---

#### **Detailed Explanation**:

1. **Statically vs Dynamically Typed**:  
   - A **statically typed language** requires variable types to be explicitly declared (e.g., Java, C++).  
   - In **dynamically typed languages** like JavaScript, variable types are inferred at runtime:
     ```javascript
     let x = 10; // x is a number
     x = "Hello"; // x becomes a string
     ```

2. **Strongly vs Weakly Typed**:  
   - A **strongly typed language** enforces strict type rules (e.g., Python, Java).  
   - A **weakly typed language**, like JavaScript, allows implicit type coercion:
     ```javascript
     console.log("10" - 5); // Output: 5 (string coerced to number)
     console.log("10" + 5); // Output: "105" (number coerced to string)
     ```

This behavior is what makes JavaScript **dynamically typed** and **weakly typed**.

---

#### **Q3: Which of the following statements is correct regarding JavaScript?**
- **Options**:  
  1. It is a forgiving language like HTML.  
  2. It inserts a semicolon after each statement automatically.  
  3. Blocks and functions both use `{}` for body contents.  
  4. Blocks use `{}`, but functions use indentation for body contents.  

- **Answer**: **1, 2, and 3**

---

#### **Detailed Explanation**:

1. **Forgiving Language**:  
   JavaScript is considered forgiving because it performs:
   - **Implicit coercion** (e.g., converting data types to avoid errors).
   - **Error suppression** for certain issues (e.g., missing semicolons).

2. **Automatic Semicolon Insertion (ASI)**:  
   JavaScript automatically inserts semicolons in some cases. However, ASI can cause issues:
   ```javascript
   return 
   { key: "value" }
   // This returns undefined due to ASI
   ```

3. **Blocks and Functions Use `{}`**:  
   Unlike Python (which uses indentation for scoping), JavaScript relies on `{}`:
   ```javascript
   if (true) { console.log("This is a block!"); }
   function myFunc() { console.log("This is a function!"); }
   ```

4. **Functions Do Not Use Indentation**:  
   This statement is incorrect as JavaScript doesn’t use indentation for function scope.

---

#### **Q4: Predict the last value shown on the console for the given program involving `setInterval` and `setTimeout`.**
- **Options**:  
  - 4  
  - 8  
  - 5  
  - 10  

- **Answer**: **8**

---

#### **Detailed Explanation**:

The program uses both `setInterval` and `setTimeout`. Here’s how they work:
1. **`setInterval`**: Repeats execution of a function at regular intervals.
2. **`setTimeout`**: Executes a function once after a delay.

**Program Execution**:
- A `setInterval` doubles `x` every second (`x = 2, 4, 6, 8`).
- After 5 seconds, `setTimeout` clears the interval.

Thus, the final value logged is **8**.

---

#### **Q5: What will be the output of the following code?**
```javascript
const x = { name: 'Rohit' };
x.name = 'Mohit';
console.log(x.name);
```
- **Options**:  
  - Throws TypeError  
  - Rohit  
  - Mohit  
  - undefined  

- **Answer**: **Mohit**

---

#### **Detailed Explanation**:

1. **`const` with Objects**:  
   Declaring an object with `const` makes the reference immutable, but object properties can still be changed:
   ```javascript
   const obj = { a: 10 };
   obj.a = 20; // Allowed
   obj = { b: 30 }; // Error: Assignment to constant variable
   ```

2. In this case, `x.name` is updated to `'Mohit'` successfully.

---

### **Week 1 Graded Questions**

---

#### **Q1: Which of the following keywords can be used to declare a variable with global scope?**
- **Options**:  
  1. `let`  
  2. `var`  
  3. `const`  
  4. All of the above  

- **Answer**: **4. All of the above**

---

#### **Detailed Explanation**:

In JavaScript, the scope of a variable determines where it can be accessed in a program. The three key ways to declare variables (`let`, `var`, and `const`) behave differently when used in global or block scope.

1. **`var`:**  
   Variables declared using `var` are globally scoped if they are not declared inside a function. Example:
   ```javascript
   var globalVar = "I am global!";
   console.log(window.globalVar); // Output: "I am global!"
   ```
   However, `var` has function scope, meaning if it’s declared inside a function, it cannot be accessed outside.

2. **`let`:**  
   Variables declared with `let` are **block scoped**. However, if declared outside any block, they behave as global variables:
   ```javascript
   let globalLet = "I am also global!";
   console.log(globalLet); // Output: "I am also global!"
   ```

3. **`const`:**  
   Similar to `let`, variables declared with `const` are block-scoped but can have global behavior when declared outside any block:
   ```javascript
   const globalConst = "I am constant!";
   console.log(globalConst); // Output: "I am constant!"
   ```

### **Key Differences Between These Declarations:**

| Feature           | `var`                  | `let`                  | `const`                |
|--------------------|------------------------|------------------------|------------------------|
| Scope             | Function or Global     | Block or Global        | Block or Global        |
| Reassignment      | Allowed               | Allowed               | Not allowed           |
| Hoisting          | Yes, but undefined     | Yes, in Temporal Dead Zone | Yes, in Temporal Dead Zone |

**Global Scope**: All three (`var`, `let`, and `const`) create global variables if declared outside a block. Hence, the correct answer is **"All of the above"**.

---

#### **Q2: Which of the following statements is true regarding JavaScript language?**
- **Options**:  
  1. JavaScript is a statically typed language.  
  2. JavaScript is a dynamically typed language.  
  3. JavaScript is a weakly typed language.  
  4. JavaScript is a strongly typed language.  

- **Answer**: **2 and 3**

---

#### **Detailed Explanation**:

1. **Statically vs Dynamically Typed**:  
   - A **statically typed language** requires variable types to be explicitly declared (e.g., Java, C++).  
   - In **dynamically typed languages** like JavaScript, variable types are inferred at runtime:
     ```javascript
     let x = 10; // x is a number
     x = "Hello"; // x becomes a string
     ```

2. **Strongly vs Weakly Typed**:  
   - A **strongly typed language** enforces strict type rules (e.g., Python, Java).  
   - A **weakly typed language**, like JavaScript, allows implicit type coercion:
     ```javascript
     console.log("10" - 5); // Output: 5 (string coerced to number)
     console.log("10" + 5); // Output: "105" (number coerced to string)
     ```

This behavior is what makes JavaScript **dynamically typed** and **weakly typed**.

---

#### **Q3: Which of the following statements is correct regarding JavaScript?**
- **Options**:  
  1. It is a forgiving language like HTML.  
  2. It inserts a semicolon after each statement automatically.  
  3. Blocks and functions both use `{}` for body contents.  
  4. Blocks use `{}`, but functions use indentation for body contents.  

- **Answer**: **1, 2, and 3**

---

#### **Detailed Explanation**:

1. **Forgiving Language**:  
   JavaScript is considered forgiving because it performs:
   - **Implicit coercion** (e.g., converting data types to avoid errors).
   - **Error suppression** for certain issues (e.g., missing semicolons).

2. **Automatic Semicolon Insertion (ASI)**:  
   JavaScript automatically inserts semicolons in some cases. However, ASI can cause issues:
   ```javascript
   return 
   { key: "value" }
   // This returns undefined due to ASI
   ```

3. **Blocks and Functions Use `{}`**:  
   Unlike Python (which uses indentation for scoping), JavaScript relies on `{}`:
   ```javascript
   if (true) { console.log("This is a block!"); }
   function myFunc() { console.log("This is a function!"); }
   ```

4. **Functions Do Not Use Indentation**:  
   This statement is incorrect as JavaScript doesn’t use indentation for function scope.

---

#### **Q4: Predict the last value shown on the console for the given program involving `setInterval` and `setTimeout`.**
- **Options**:  
  - 4  
  - 8  
  - 5  
  - 10  

- **Answer**: **8**

---

#### **Detailed Explanation**:

The program uses both `setInterval` and `setTimeout`. Here’s how they work:
1. **`setInterval`**: Repeats execution of a function at regular intervals.
2. **`setTimeout`**: Executes a function once after a delay.

**Program Execution**:
- A `setInterval` doubles `x` every second (`x = 2, 4, 6, 8`).
- After 5 seconds, `setTimeout` clears the interval.

Thus, the final value logged is **8**.

---

#### **Q5: What will be the output of the following code?**
```javascript
const x = { name: 'Rohit' };
x.name = 'Mohit';
console.log(x.name);
```
- **Options**:  
  - Throws TypeError  
  - Rohit  
  - Mohit  
  - undefined  

- **Answer**: **Mohit**

---

#### **Detailed Explanation**:

1. **`const` with Objects**:  
   Declaring an object with `const` makes the reference immutable, but object properties can still be changed:
   ```javascript
   const obj = { a: 10 };
   obj.a = 20; // Allowed
   obj = { b: 30 }; // Error: Assignment to constant variable
   ```

2. In this case, `x.name` is updated to `'Mohit'` successfully.

---

#### **Q10: Predict the last value shown in the console.**

- **Code Breakdown**:
  ```javascript
  startNamePrinter = (name) => {
    x = name.split('').reverse(); // Splits the string into characters and reverses the array.
    handler = setInterval(() => {
      y = x.pop(); // Pops the last element of the array and logs it.
      console.log(y);
    }, 1000);

    setTimeout(() => {
      clearInterval(handler); // Stops the interval after all characters are printed.
    }, (name.length + 1) * 1000); // Waits for 1 second per character + 1 extra second.
  };

  startNamePrinter('orange');
  ```

- **Explanation**:
  1. The string `'orange'` is split into an array: `['o', 'r', 'a', 'n', 'g', 'e']`.
  2. The array is reversed: `['e', 'g', 'n', 'a', 'r', 'o']`.
  3. Every second, the `setInterval` pops and logs a character:
     - At `1s`: `'e'`
     - At `2s`: `'g'`
     - At `3s`: `'n'`
     - At `4s`: `'a'`
     - At `5s`: `'r'`
     - At `6s`: `'o'`
  4. The interval stops after `(6 + 1) * 1000 = 7 seconds`.
  5. The last value logged is `'n'` (4 seconds in).

- **Answer**: **2. `'n'`**

---

### **Week 1 Practice Questions**

---

#### **Q1: Write a function that takes an array of numbers and returns their sum.**
- **Input Example**: `[1, 2, 3, 4, 5]`
- **Output**: `15`

---

#### **Solution**:

```javascript
function sumArray(numbers) {
  return numbers.reduce((sum, num) => sum + num, 0);
}

// Example
const array = [1, 2, 3, 4, 5];
console.log(sumArray(array)); // Output: 15
```

---

#### **Explanation**:
1. **`reduce` Function**:
   - The `reduce` method applies a function to each element of the array, accumulating a single value.
   - Here, the initial value of the accumulator (`sum`) is `0`.

---

#### **Q2: Write a function to check if a given string is a palindrome.**
- **Input Example**: `"racecar"`
- **Output**: `true`

---

#### **Solution**:

```javascript
function isPalindrome(str) {
  const reversed = str.split('').reverse().join('');
  return str === reversed;
}

// Example
console.log(isPalindrome("racecar")); // Output: true
console.log(isPalindrome("hello")); // Output: false
```

---

#### **Explanation**:
1. The string is split into an array of characters.
2. The array is reversed and joined back into a string.
3. The original string is compared with the reversed string.

---

#### **Q3: Implement a function to find the largest number in an array.**
- **Input Example**: `[3, 5, 7, 2, 8]`
- **Output**: `8`

---

#### **Solution**:

```javascript
function findLargestNumber(numbers) {
  return Math.max(...numbers);
}

// Example
const nums = [3, 5, 7, 2, 8];
console.log(findLargestNumber(nums)); // Output: 8
```

---

#### **Explanation**:
1. **`Math.max` Function**:
   - `Math.max` returns the largest value from a list of numbers.
   - The spread operator (`...`) expands the array into individual arguments.

---

#### **Q4: Create a function to count the occurrences of each character in a string.**
- **Input Example**: `"hello"`
- **Output**: `{ h: 1, e: 1, l: 2, o: 1 }`

---

#### **Solution**:

```javascript
function countOccurrences(str) {
  const counts = {};
  for (let char of str) {
    counts[char] = counts[char] ? counts[char] + 1 : 1;
  }
  return counts;
}

// Example
console.log(countOccurrences("hello")); // Output: { h: 1, e: 1, l: 2, o: 1 }
```

---

#### **Explanation**:
1. A `for` loop iterates over each character in the string.
2. The `counts` object tracks occurrences, incrementing the count if the character exists or initializing it to `1` if it doesn’t.

---

#### **Q5: Write a function to reverse the words in a sentence.**
- **Input Example**: `"Hello world"`
- **Output**: `"world Hello"`

---

#### **Solution**:

```javascript
function reverseWords(sentence) {
  return sentence.split(' ').reverse().join(' ');
}

// Example
console.log(reverseWords("Hello world")); // Output: "world Hello"
```

---

#### **Explanation**:
1. The sentence is split into an array of words using the space delimiter (`' '`).
2. The array is reversed and then joined back into a sentence.

---

Let’s proceed with the remaining **Week 1 Practice Questions** and their detailed explanations.

---

#### **Q6: Write a function to flatten a nested array.**
- **Input Example**: `[1, [2, 3], [4, [5]]]`  
- **Output**: `[1, 2, 3, 4, 5]`

---

#### **Solution**:

```javascript
function flattenArray(arr) {
  return arr.flat(Infinity);
}

// Example
console.log(flattenArray([1, [2, 3], [4, [5]]])); // Output: [1, 2, 3, 4, 5]
```

---

#### **Explanation**:
1. **`Array.prototype.flat()`**:
   - The `flat()` method flattens a nested array up to the specified depth.
   - Using `Infinity` as the depth parameter flattens the array completely.

**Alternative Solution (Recursive)**:
```javascript
function flattenArrayRecursive(arr) {
  return arr.reduce((flat, toFlatten) => {
    return flat.concat(Array.isArray(toFlatten) ? flattenArrayRecursive(toFlatten) : toFlatten);
  }, []);
}
```

---

#### **Q7: Implement a function to remove duplicates from an array.**
- **Input Example**: `[1, 2, 2, 3, 4, 4]`
- **Output**: `[1, 2, 3, 4]`

---

#### **Solution**:

```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

// Example
console.log(removeDuplicates([1, 2, 2, 3, 4, 4])); // Output: [1, 2, 3, 4]
```

---

#### **Explanation**:
1. **`Set` Object**:
   - A `Set` is a collection of unique values.
   - Converting an array to a `Set` removes duplicates. Spreading the `Set` back into an array gives the desired result.

**Alternative Solution**:
```javascript
function removeDuplicatesAlt(arr) {
  const unique = [];
  for (let item of arr) {
    if (!unique.includes(item)) unique.push(item);
  }
  return unique;
}
```

---

#### **Q8: Write a function to capitalize the first letter of each word in a sentence.**
- **Input Example**: `"hello world"`
- **Output**: `"Hello World"`

---

#### **Solution**:

```javascript
function capitalizeWords(sentence) {
  return sentence
    .split(' ')
    .map(word => word.charAt(0).toUpperCase() + word.slice(1))
    .join(' ');
}

// Example
console.log(capitalizeWords("hello world")); // Output: "Hello World"
```

---

#### **Explanation**:
1. **Steps**:
   - Split the sentence into words using `' '`.
   - Capitalize the first letter of each word using `charAt(0).toUpperCase()`.
   - Reconstruct the sentence using `join(' ')`.

---

#### **Q9: Create a function to check if two strings are anagrams.**
- **Input Example**: `"listen"` and `"silent"`
- **Output**: `true`

---

#### **Solution**:

```javascript
function areAnagrams(str1, str2) {
  const format = str => str.toLowerCase().split('').sort().join('');
  return format(str1) === format(str2);
}

// Example
console.log(areAnagrams("listen", "silent")); // Output: true
console.log(areAnagrams("hello", "world")); // Output: false
```

---

#### **Explanation**:
1. **Steps**:
   - Convert both strings to lowercase to ensure case insensitivity.
   - Sort the characters of each string and compare them. Anagrams will have identical sorted forms.

---

#### **Q10: Write a function to generate the Fibonacci sequence up to `n` terms.**
- **Input Example**: `5`
- **Output**: `[0, 1, 1, 2, 3]`

---

#### **Solution**:

```javascript
function generateFibonacci(n) {
  if (n <= 0) return [];
  if (n === 1) return [0];
  const fib = [0, 1];
  for (let i = 2; i < n; i++) {
    fib.push(fib[i - 1] + fib[i - 2]);
  }
  return fib;
}

// Example
console.log(generateFibonacci(5)); // Output: [0, 1, 1, 2, 3]
```

---

#### **Explanation**:
1. **Logic**:
   - Start the sequence with `[0, 1]`.
   - Add the sum of the last two terms to the array until `n` terms are generated.

---

### **Week 2 Graded Questions**

Now, let’s proceed to **Week 2 Graded Questions**.

---

#### **Q1: Which of the following shows the correct output of the given program?**
**Code**:
```javascript
let a = [75, 55, 22, 5];
console.log(a.sort());
```
- **Options**:  
  1. Error  
  2. `[5, 22, 55, 75]`  
  3. `[22, 5, 55, 75]`  
  4. `[5, 75, 22, 55]`

- **Answer**: **3. `[22, 5, 55, 75]`**

---

#### **Detailed Explanation**:

1. **Default Behavior of `sort()`**:
   - By default, the `sort()` method sorts elements as strings.
   - Elements are converted to strings and compared lexicographically (dictionary order):
     ```javascript
     console.log(["22", "5"].sort()); // Output: ["22", "5"]
     ```

2. **Numerical Sorting**:
   - For numerical sorting, a comparison function is needed:
     ```javascript
     a.sort((x, y) => x - y); // Output: [5, 22, 55, 75]
     ```

3. **Behavior in the Given Code**:
   - Without a comparison function, the array is sorted lexicographically: `[22, 5, 55, 75]`.

---

#### **Q2: What will be the output of this code?**
**Code**:
```javascript
let a = { name: 'Abhi', age: 22 };
let b = [];
for (let i = 0; i < 3; i++) {
  b.push(a);
}
b[1].name = 'Akshay';
console.log(b[0].name);
```
- **Options**:  
  1. Abhi  
  2. Akshay  
  3. Undefined  
  4. ReferenceError

- **Answer**: **2. Akshay**

---

#### **Detailed Explanation**:

1. **Reference Behavior in Objects**:
   - In JavaScript, objects are assigned by reference.
   - Modifying the `name` property of one object affects all references to that object.

2. **Execution**:
   - `b` contains three references to the same object `a`.
   - When `b[1].name` is changed to `'Akshay'`, it also updates `b[0].name`.

---
Let’s proceed with the remaining **Week 1 Practice Questions** and their detailed explanations.

---

#### **Q6: Write a function to flatten a nested array.**
- **Input Example**: `[1, [2, 3], [4, [5]]]`  
- **Output**: `[1, 2, 3, 4, 5]`

---

#### **Solution**:

```javascript
function flattenArray(arr) {
  return arr.flat(Infinity);
}

// Example
console.log(flattenArray([1, [2, 3], [4, [5]]])); // Output: [1, 2, 3, 4, 5]
```

---

#### **Explanation**:
1. **`Array.prototype.flat()`**:
   - The `flat()` method flattens a nested array up to the specified depth.
   - Using `Infinity` as the depth parameter flattens the array completely.

**Alternative Solution (Recursive)**:
```javascript
function flattenArrayRecursive(arr) {
  return arr.reduce((flat, toFlatten) => {
    return flat.concat(Array.isArray(toFlatten) ? flattenArrayRecursive(toFlatten) : toFlatten);
  }, []);
}
```

---

#### **Q7: Implement a function to remove duplicates from an array.**
- **Input Example**: `[1, 2, 2, 3, 4, 4]`
- **Output**: `[1, 2, 3, 4]`

---

#### **Solution**:

```javascript
function removeDuplicates(arr) {
  return [...new Set(arr)];
}

// Example
console.log(removeDuplicates([1, 2, 2, 3, 4, 4])); // Output: [1, 2, 3, 4]
```

---

#### **Explanation**:
1. **`Set` Object**:
   - A `Set` is a collection of unique values.
   - Converting an array to a `Set` removes duplicates. Spreading the `Set` back into an array gives the desired result.

**Alternative Solution**:
```javascript
function removeDuplicatesAlt(arr) {
  const unique = [];
  for (let item of arr) {
    if (!unique.includes(item)) unique.push(item);
  }
  return unique;
}
```

---

#### **Q8: Write a function to capitalize the first letter of each word in a sentence.**
- **Input Example**: `"hello world"`
- **Output**: `"Hello World"`

---

#### **Solution**:

```javascript
function capitalizeWords(sentence) {
  return sentence
    .split(' ')
    .map(word => word.charAt(0).toUpperCase() + word.slice(1))
    .join(' ');
}

// Example
console.log(capitalizeWords("hello world")); // Output: "Hello World"
```

---

#### **Explanation**:
1. **Steps**:
   - Split the sentence into words using `' '`.
   - Capitalize the first letter of each word using `charAt(0).toUpperCase()`.
   - Reconstruct the sentence using `join(' ')`.

---

#### **Q9: Create a function to check if two strings are anagrams.**
- **Input Example**: `"listen"` and `"silent"`
- **Output**: `true`

---

#### **Solution**:

```javascript
function areAnagrams(str1, str2) {
  const format = str => str.toLowerCase().split('').sort().join('');
  return format(str1) === format(str2);
}

// Example
console.log(areAnagrams("listen", "silent")); // Output: true
console.log(areAnagrams("hello", "world")); // Output: false
```

---

#### **Explanation**:
1. **Steps**:
   - Convert both strings to lowercase to ensure case insensitivity.
   - Sort the characters of each string and compare them. Anagrams will have identical sorted forms.

---

#### **Q10: Write a function to generate the Fibonacci sequence up to `n` terms.**
- **Input Example**: `5`
- **Output**: `[0, 1, 1, 2, 3]`

---

#### **Solution**:

```javascript
function generateFibonacci(n) {
  if (n <= 0) return [];
  if (n === 1) return [0];
  const fib = [0, 1];
  for (let i = 2; i < n; i++) {
    fib.push(fib[i - 1] + fib[i - 2]);
  }
  return fib;
}

// Example
console.log(generateFibonacci(5)); // Output: [0, 1, 1, 2, 3]
```

---

#### **Explanation**:
1. **Logic**:
   - Start the sequence with `[0, 1]`.
   - Add the sum of the last two terms to the array until `n` terms are generated.

---

### **Week 2 Graded Questions**

Now, let’s proceed to **Week 2 Graded Questions**.

---

#### **Q1: Which of the following shows the correct output of the given program?**
**Code**:
```javascript
let a = [75, 55, 22, 5];
console.log(a.sort());
```
- **Options**:  
  1. Error  
  2. `[5, 22, 55, 75]`  
  3. `[22, 5, 55, 75]`  
  4. `[5, 75, 22, 55]`

- **Answer**: **3. `[22, 5, 55, 75]`**

---

#### **Detailed Explanation**:

1. **Default Behavior of `sort()`**:
   - By default, the `sort()` method sorts elements as strings.
   - Elements are converted to strings and compared lexicographically (dictionary order):
     ```javascript
     console.log(["22", "5"].sort()); // Output: ["22", "5"]
     ```

2. **Numerical Sorting**:
   - For numerical sorting, a comparison function is needed:
     ```javascript
     a.sort((x, y) => x - y); // Output: [5, 22, 55, 75]
     ```

3. **Behavior in the Given Code**:
   - Without a comparison function, the array is sorted lexicographically: `[22, 5, 55, 75]`.

---

#### **Q2: What will be the output of this code?**
**Code**:
```javascript
let a = { name: 'Abhi', age: 22 };
let b = [];
for (let i = 0; i < 3; i++) {
  b.push(a);
}
b[1].name = 'Akshay';
console.log(b[0].name);
```
- **Options**:  
  1. Abhi  
  2. Akshay  
  3. Undefined  
  4. ReferenceError

- **Answer**: **2. Akshay**

---

#### **Detailed Explanation**:

1. **Reference Behavior in Objects**:
   - In JavaScript, objects are assigned by reference.
   - Modifying the `name` property of one object affects all references to that object.

2. **Execution**:
   - `b` contains three references to the same object `a`.
   - When `b[1].name` is changed to `'Akshay'`, it also updates `b[0].name`.

---
Let’s proceed with the remaining **Week 2 Graded Questions**.

---

#### **Q8: Analyze the output of the given Vue.js application.**
**Code**:
**HTML**:
```html
<div id="app">
  <div id="div1" style="background-color: red"></div>
</div>
<script src="script.js"></script>
```
**JavaScript (`script.js`)**:
```javascript
var height = 0;
var width = 0;
var divStyle = document.getElementById('div1').style;
let res = setInterval(() => {
  height += 50;
  width += 50;
  divStyle.height = height + 'px';
  divStyle.width = width + 'px';
  console.log(height);
}, 1000);

setTimeout(() => {
  clearInterval(res);
}, 10050);
```
**Question**: What will be the height of the `div` element with ID `div1` after 20 seconds?  
- **Options**:  
  1. `500px`  
  2. `1000px`  
  3. `0px`  
  4. `None of the above`

- **Answer**: **1. 500px**

---

#### **Detailed Explanation**:

1. **Logic of `setInterval`**:
   - The `setInterval` callback increases the height and width of the `div` element by `50px` every second.

2. **Logic of `setTimeout`**:
   - After `10050ms` (approximately 10 seconds), the `setTimeout` clears the interval, stopping further height/width increases.

3. **Execution**:
   - The interval runs 10 times before being cleared (`10050ms / 1000ms per iteration = 10`).
   - Height increases by \(50px \times 10 = 500px\).

4. **Final State After 20 Seconds**:
   - Even though the program runs for 20 seconds, the interval has already been cleared after 10 seconds.
   - The height remains **`500px`**.

---

#### **Q9: Analyze the following code with modules.**
**Files**:  
**`index.html`**:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <script src="module1.js" type="module"></script>
</head>
<body>
  <div id="div1" style="border: 2px solid black"></div>
</body>
</html>
```

**`module1.js`**:
```javascript
import { divStyle1, divStyle2 } from './module2.js';

divStyle1.width = '50px';
const diviStyle = document.getElementById('div1').style;
diviStyle.backgroundColor = divStyle1.color;
diviStyle.height = divStyle2.height;
diviStyle.width = divStyle1.width;
```

**`module2.js`**:
```javascript
export const divStyle1 = {
  color: 'red',
  height: '100px',
  width: '100px',
};

export const divStyle2 = {
  color: 'green',
  height: '50px',
};
```

**Question**: What will be the background color, height, and width of the HTML element with ID `div1` when rendered in a browser?  
- **Options**:  
  1. `Red, 100px, 100px`  
  2. `Red, 50px, 50px`  
  3. `Green, 50px, 100px`  
  4. `Green, 50px, 50px`

- **Answer**: **2. Red, 50px, 50px**

---

#### **Detailed Explanation**:

1. **Module Imports**:
   - `divStyle1` and `divStyle2` are imported from `module2.js`.

2. **Property Overrides**:
   - In `module1.js`, `divStyle1.width` is updated to `'50px'`.

3. **Final Style of `div1`**:
   - `backgroundColor`: Comes from `divStyle1.color`, which is `'red'`.  
   - `height`: Comes from `divStyle2.height`, which is `'50px'`.  
   - `width`: Comes from the updated `divStyle1.width`, which is `'50px'`.

---

#### **Q10: Predict the output of the program involving object iteration.**
**Code**:
```javascript
const api = { A: 'Application', P: 'Programming', I: 'Interface' };
function standsFor(x) {
  for (let [k, v] of Object.entries(api)) {
    if (k !== x) {
      return v;
    }
  }
}
console.log(standsFor('A'));
```
- **Options**:  
  1. `Application`  
  2. `Programming`  
  3. `Interface`  
  4. `A`

- **Answer**: **2. Programming**

---

#### **Detailed Explanation**:

1. **Logic of `Object.entries`**:
   - `Object.entries()` converts an object into an array of `[key, value]` pairs:
     ```javascript
     [['A', 'Application'], ['P', 'Programming'], ['I', 'Interface']]
     ```

2. **Execution**:
   - The loop iterates through the entries.
   - When `k !== 'A'`:
     - For the first entry (`['A', 'Application']`), `k === 'A'`, so it skips.
     - For the second entry (`['P', 'Programming']`), `k !== 'A'`, so it returns `'Programming'`.

3. **Output**:
   - The first value with a key not equal to `'A'` is `'Programming'`.

---
Let’s proceed with the remaining **Week 2 Graded Questions**.

---

#### **Q8: Analyze the output of the given Vue.js application.**
**Code**:
**HTML**:
```html
<div id="app">
  <div id="div1" style="background-color: red"></div>
</div>
<script src="script.js"></script>
```
**JavaScript (`script.js`)**:
```javascript
var height = 0;
var width = 0;
var divStyle = document.getElementById('div1').style;
let res = setInterval(() => {
  height += 50;
  width += 50;
  divStyle.height = height + 'px';
  divStyle.width = width + 'px';
  console.log(height);
}, 1000);

setTimeout(() => {
  clearInterval(res);
}, 10050);
```
**Question**: What will be the height of the `div` element with ID `div1` after 20 seconds?  
- **Options**:  
  1. `500px`  
  2. `1000px`  
  3. `0px`  
  4. `None of the above`

- **Answer**: **1. 500px**

---

#### **Detailed Explanation**:

1. **Logic of `setInterval`**:
   - The `setInterval` callback increases the height and width of the `div` element by `50px` every second.

2. **Logic of `setTimeout`**:
   - After `10050ms` (approximately 10 seconds), the `setTimeout` clears the interval, stopping further height/width increases.

3. **Execution**:
   - The interval runs 10 times before being cleared (`10050ms / 1000ms per iteration = 10`).
   - Height increases by \(50px \times 10 = 500px\).

4. **Final State After 20 Seconds**:
   - Even though the program runs for 20 seconds, the interval has already been cleared after 10 seconds.
   - The height remains **`500px`**.

---

#### **Q9: Analyze the following code with modules.**
**Files**:  
**`index.html`**:
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <script src="module1.js" type="module"></script>
</head>
<body>
  <div id="div1" style="border: 2px solid black"></div>
</body>
</html>
```

**`module1.js`**:
```javascript
import { divStyle1, divStyle2 } from './module2.js';

divStyle1.width = '50px';
const diviStyle = document.getElementById('div1').style;
diviStyle.backgroundColor = divStyle1.color;
diviStyle.height = divStyle2.height;
diviStyle.width = divStyle1.width;
```

**`module2.js`**:
```javascript
export const divStyle1 = {
  color: 'red',
  height: '100px',
  width: '100px',
};

export const divStyle2 = {
  color: 'green',
  height: '50px',
};
```

**Question**: What will be the background color, height, and width of the HTML element with ID `div1` when rendered in a browser?  
- **Options**:  
  1. `Red, 100px, 100px`  
  2. `Red, 50px, 50px`  
  3. `Green, 50px, 100px`  
  4. `Green, 50px, 50px`

- **Answer**: **2. Red, 50px, 50px**

---

#### **Detailed Explanation**:

1. **Module Imports**:
   - `divStyle1` and `divStyle2` are imported from `module2.js`.

2. **Property Overrides**:
   - In `module1.js`, `divStyle1.width` is updated to `'50px'`.

3. **Final Style of `div1`**:
   - `backgroundColor`: Comes from `divStyle1.color`, which is `'red'`.  
   - `height`: Comes from `divStyle2.height`, which is `'50px'`.  
   - `width`: Comes from the updated `divStyle1.width`, which is `'50px'`.

---

#### **Q10: Predict the output of the program involving object iteration.**
**Code**:
```javascript
const api = { A: 'Application', P: 'Programming', I: 'Interface' };
function standsFor(x) {
  for (let [k, v] of Object.entries(api)) {
    if (k !== x) {
      return v;
    }
  }
}
console.log(standsFor('A'));
```
- **Options**:  
  1. `Application`  
  2. `Programming`  
  3. `Interface`  
  4. `A`

- **Answer**: **2. Programming**

---

#### **Detailed Explanation**:

1. **Logic of `Object.entries`**:
   - `Object.entries()` converts an object into an array of `[key, value]` pairs:
     ```javascript
     [['A', 'Application'], ['P', 'Programming'], ['I', 'Interface']]
     ```

2. **Execution**:
   - The loop iterates through the entries.
   - When `k !== 'A'`:
     - For the first entry (`['A', 'Application']`), `k === 'A'`, so it skips.
     - For the second entry (`['P', 'Programming']`), `k !== 'A'`, so it returns `'Programming'`.

3. **Output**:
   - The first value with a key not equal to `'A'` is `'Programming'`.

---

Continuing with the remaining **Week 2 Practice Questions**:

---

#### **Q8: Write a function to calculate the sum of all numbers in a matrix.**
- **Input Example**:  
  ```
  [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
  ]
  ```
- **Output**: `45`

---

#### **Solution**:

```javascript
function sumMatrix(matrix) {
  return matrix.reduce((total, row) => {
    return total + row.reduce((rowSum, num) => rowSum + num, 0);
  }, 0);
}

// Example
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
console.log(sumMatrix(matrix)); // Output: 45
```

---

#### **Explanation**:
1. **Two `reduce` Calls**:
   - The outer `reduce` iterates over each row in the matrix.
   - The inner `reduce` sums up the elements within a single row.

2. **Total Calculation**:
   - For the given matrix:
     ```
     [1, 2, 3] → 6
     [4, 5, 6] → 15
     [7, 8, 9] → 24
     Total = 6 + 15 + 24 = 45
     ```

---

#### **Q9: Write a function to count the vowels in a string.**
- **Input Example**: `"hello world"`  
- **Output**: `3`

---

#### **Solution**:

```javascript
function countVowels(str) {
  const vowels = 'aeiouAEIOU';
  return str.split('').filter(char => vowels.includes(char)).length;
}

// Example
console.log(countVowels("hello world")); // Output: 3
```

---

#### **Explanation**:
1. **Steps**:
   - Split the string into individual characters.
   - Use `filter()` to retain only characters present in the `vowels` string.
   - Return the length of the filtered array.

2. **Count in the Example**:
   - `"hello world"` contains vowels: `e, o, o`.

---

#### **Q10: Write a function to find the intersection of two arrays.**
- **Input Example**: `[1, 2, 3]` and `[2, 3, 4]`  
- **Output**: `[2, 3]`

---

#### **Solution**:

```javascript
function intersectArrays(arr1, arr2) {
  return arr1.filter(num => arr2.includes(num));
}

// Example
console.log(intersectArrays([1, 2, 3], [2, 3, 4])); // Output: [2, 3]
```

---

#### **Explanation**:
1. **`filter` and `includes`**:
   - The `filter()` method iterates over `arr1` and checks if each element exists in `arr2` using `includes()`.

2. **Result**:
   - Only the common elements, `2` and `3`, are included in the output.

---

#### **Q11: Write a function to generate a random hexadecimal color code.**
- **Output Example**: `#3e2f1b`

---

#### **Solution**:

```javascript
function generateHexColor() {
  return '#' + Math.floor(Math.random() * 16777215).toString(16).padStart(6, '0');
}

// Example
console.log(generateHexColor()); // Output: Random Hex Code (e.g., "#3e2f1b")
```

---

#### **Explanation**:
1. **Hexadecimal Color Codes**:
   - Hex codes represent colors using 6 hexadecimal digits, ranging from `#000000` (black) to `#ffffff` (white).

2. **Steps**:
   - Generate a random number between `0` and `16777215` (decimal equivalent of `#ffffff`).
   - Convert it to a hexadecimal string with `toString(16)`.
   - Ensure the code is 6 characters long using `padStart()`.

---

#### **Q12: Write a function to count the occurrences of words in a string.**
- **Input Example**: `"hello world hello"`  
- **Output**: `{ hello: 2, world: 1 }`

---

#### **Solution**:

```javascript
function countWords(str) {
  const words = str.split(' ');
  const wordCounts = {};
  for (let word of words) {
    wordCounts[word] = wordCounts[word] ? wordCounts[word] + 1 : 1;
  }
  return wordCounts;
}

// Example
console.log(countWords("hello world hello")); // Output: { hello: 2, world: 1 }
```

---

#### **Explanation**:
1. **Steps**:
   - Split the string into an array of words using `' '` as the delimiter.
   - Iterate over the array and maintain a count for each word in the `wordCounts` object.

2. **Result**:
   - For the example, the word `"hello"` appears `2` times, and `"world"` appears `1` time.

---

#### **Q13: Write a function to rotate an array to the right by `k` steps.**
- **Input Example**: `[1, 2, 3, 4, 5]`, `k = 2`  
- **Output**: `[4, 5, 1, 2, 3]`

---

#### **Solution**:

```javascript
function rotateArray(arr, k) {
  k = k % arr.length;
  return [...arr.slice(-k), ...arr.slice(0, -k)];
}

// Example
console.log(rotateArray([1, 2, 3, 4, 5], 2)); // Output: [4, 5, 1, 2, 3]
```

---

#### **Explanation**:
1. **Steps**:
   - Use `slice()` to split the array into two parts:
     - The last `k` elements: `arr.slice(-k)`
     - The remaining elements: `arr.slice(0, -k)`
   - Concatenate the two parts in reverse order.

2. **Optimization**:
   - Use `k % arr.length` to handle cases where `k` is larger than the array length.

---

Continuing with the remaining **Week 2 Practice Questions**:

---

#### **Q8: Write a function to calculate the sum of all numbers in a matrix.**
- **Input Example**:  
  ```
  [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
  ]
  ```
- **Output**: `45`

---

#### **Solution**:

```javascript
function sumMatrix(matrix) {
  return matrix.reduce((total, row) => {
    return total + row.reduce((rowSum, num) => rowSum + num, 0);
  }, 0);
}

// Example
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
console.log(sumMatrix(matrix)); // Output: 45
```

---

#### **Explanation**:
1. **Two `reduce` Calls**:
   - The outer `reduce` iterates over each row in the matrix.
   - The inner `reduce` sums up the elements within a single row.

2. **Total Calculation**:
   - For the given matrix:
     ```
     [1, 2, 3] → 6
     [4, 5, 6] → 15
     [7, 8, 9] → 24
     Total = 6 + 15 + 24 = 45
     ```

---

#### **Q9: Write a function to count the vowels in a string.**
- **Input Example**: `"hello world"`  
- **Output**: `3`

---

#### **Solution**:

```javascript
function countVowels(str) {
  const vowels = 'aeiouAEIOU';
  return str.split('').filter(char => vowels.includes(char)).length;
}

// Example
console.log(countVowels("hello world")); // Output: 3
```

---

#### **Explanation**:
1. **Steps**:
   - Split the string into individual characters.
   - Use `filter()` to retain only characters present in the `vowels` string.
   - Return the length of the filtered array.

2. **Count in the Example**:
   - `"hello world"` contains vowels: `e, o, o`.

---

#### **Q10: Write a function to find the intersection of two arrays.**
- **Input Example**: `[1, 2, 3]` and `[2, 3, 4]`  
- **Output**: `[2, 3]`

---

#### **Solution**:

```javascript
function intersectArrays(arr1, arr2) {
  return arr1.filter(num => arr2.includes(num));
}

// Example
console.log(intersectArrays([1, 2, 3], [2, 3, 4])); // Output: [2, 3]
```

---

#### **Explanation**:
1. **`filter` and `includes`**:
   - The `filter()` method iterates over `arr1` and checks if each element exists in `arr2` using `includes()`.

2. **Result**:
   - Only the common elements, `2` and `3`, are included in the output.

---

#### **Q11: Write a function to generate a random hexadecimal color code.**
- **Output Example**: `#3e2f1b`

---

#### **Solution**:

```javascript
function generateHexColor() {
  return '#' + Math.floor(Math.random() * 16777215).toString(16).padStart(6, '0');
}

// Example
console.log(generateHexColor()); // Output: Random Hex Code (e.g., "#3e2f1b")
```

---

#### **Explanation**:
1. **Hexadecimal Color Codes**:
   - Hex codes represent colors using 6 hexadecimal digits, ranging from `#000000` (black) to `#ffffff` (white).

2. **Steps**:
   - Generate a random number between `0` and `16777215` (decimal equivalent of `#ffffff`).
   - Convert it to a hexadecimal string with `toString(16)`.
   - Ensure the code is 6 characters long using `padStart()`.

---

#### **Q12: Write a function to count the occurrences of words in a string.**
- **Input Example**: `"hello world hello"`  
- **Output**: `{ hello: 2, world: 1 }`

---

#### **Solution**:

```javascript
function countWords(str) {
  const words = str.split(' ');
  const wordCounts = {};
  for (let word of words) {
    wordCounts[word] = wordCounts[word] ? wordCounts[word] + 1 : 1;
  }
  return wordCounts;
}

// Example
console.log(countWords("hello world hello")); // Output: { hello: 2, world: 1 }
```

---

#### **Explanation**:
1. **Steps**:
   - Split the string into an array of words using `' '` as the delimiter.
   - Iterate over the array and maintain a count for each word in the `wordCounts` object.

2. **Result**:
   - For the example, the word `"hello"` appears `2` times, and `"world"` appears `1` time.

---

#### **Q13: Write a function to rotate an array to the right by `k` steps.**
- **Input Example**: `[1, 2, 3, 4, 5]`, `k = 2`  
- **Output**: `[4, 5, 1, 2, 3]`

---

#### **Solution**:

```javascript
function rotateArray(arr, k) {
  k = k % arr.length;
  return [...arr.slice(-k), ...arr.slice(0, -k)];
}

// Example
console.log(rotateArray([1, 2, 3, 4, 5], 2)); // Output: [4, 5, 1, 2, 3]
```

---

#### **Explanation**:
1. **Steps**:
   - Use `slice()` to split the array into two parts:
     - The last `k` elements: `arr.slice(-k)`
     - The remaining elements: `arr.slice(0, -k)`
   - Concatenate the two parts in reverse order.

2. **Optimization**:
   - Use `k % arr.length` to handle cases where `k` is larger than the array length.

---
Let’s continue with **Week 3 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 3 Practice Questions**

---

#### **Q1: Write an `async` function that fetches data from a simulated API and logs the result.**
- **Simulated API**:  
  ```javascript
  function fetchFromAPI() {
    return new Promise((resolve) => {
      setTimeout(() => resolve("API Response"), 2000);
    });
  }
  ```
- **Output Example**:  
  - `Fetching data...`  
  - `API Response`

---

#### **Solution**:

```javascript
async function fetchData() {
  console.log("Fetching data...");
  const data = await fetchFromAPI();
  console.log(data);
}

// Simulated API
function fetchFromAPI() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("API Response"), 2000);
  });
}

// Example
fetchData();
```

---

#### **Explanation**:
1. **Simulated API**:
   - The `fetchFromAPI` function returns a promise that resolves after 2 seconds with the message `"API Response"`.

2. **Async Function**:
   - `await` pauses the execution of `fetchData` until the promise returned by `fetchFromAPI` resolves.

3. **Execution Order**:
   - Logs `"Fetching data..."` immediately.
   - After 2 seconds, logs `"API Response"`.

---

#### **Q2: Write a function to execute multiple promises concurrently and log their results.**
- **Input Example**:
  ```javascript
  const p1 = Promise.resolve(1);
  const p2 = Promise.resolve(2);
  const p3 = Promise.resolve(3);
  ```
- **Output**: `[1, 2, 3]`

---

#### **Solution**:

```javascript
async function executePromises(promises) {
  const results = await Promise.all(promises);
  console.log(results);
}

// Example
const p1 = Promise.resolve(1);
const p2 = Promise.resolve(2);
const p3 = Promise.resolve(3);

executePromises([p1, p2, p3]);
```

---

#### **Explanation**:
1. **`Promise.all`**:
   - Executes all promises in parallel and waits for all to resolve.
   - Returns an array of resolved values.

2. **Execution**:
   - In the example, `[1, 2, 3]` is logged as all promises resolve immediately.

---

#### **Q3: Write an `async` function to simulate a countdown timer.**
- **Input Example**: `5`  
- **Output**:  
  ```
  5
  4
  3
  2
  1
  Time's up!
  ```

---

#### **Solution**:

```javascript
async function countdown(seconds) {
  for (let i = seconds; i > 0; i--) {
    console.log(i);
    await new Promise((resolve) => setTimeout(resolve, 1000));
  }
  console.log("Time's up!");
}

// Example
countdown(5);
```

---

#### **Explanation**:
1. **Async Timer**:
   - The `setTimeout` inside a promise simulates a delay of 1 second for each countdown step.

2. **Execution**:
   - The function logs the countdown numbers, pausing 1 second between each log.

---

#### **Q4: Write an `async` function to fetch data from multiple simulated APIs and log their results.**
- **Simulated APIs**:
  ```javascript
  function api1() {
    return new Promise((resolve) => setTimeout(() => resolve("API 1 Response"), 1000));
  }
  function api2() {
    return new Promise((resolve) => setTimeout(() => resolve("API 2 Response"), 2000));
  }
  ```
- **Output**:  
  - `API 1 Response`  
  - `API 2 Response`

---

#### **Solution**:

```javascript
async function fetchMultipleAPIs() {
  const [result1, result2] = await Promise.all([api1(), api2()]);
  console.log(result1);
  console.log(result2);
}

// Simulated APIs
function api1() {
  return new Promise((resolve) => setTimeout(() => resolve("API 1 Response"), 1000));
}

function api2() {
  return new Promise((resolve) => setTimeout(() => resolve("API 2 Response"), 2000));
}

// Example
fetchMultipleAPIs();
```

---

#### **Explanation**:
1. **Simultaneous Requests**:
   - `Promise.all` executes both API requests in parallel, reducing the total wait time.

2. **Execution**:
   - Logs `"API 1 Response"` after 1 second and `"API 2 Response"` after 2 seconds.

---

#### **Q5: Write an `async` function that retries a failing promise up to 3 times.**
- **Simulated API**:
  ```javascript
  let attempt = 0;
  function unreliableAPI() {
    return new Promise((resolve, reject) => {
      attempt++;
      if (attempt < 3) reject("Failure");
      else resolve("Success");
    });
  }
  ```
- **Output Example**:  
  - `Attempt 1: Failure`  
  - `Attempt 2: Failure`  
  - `Attempt 3: Success`

---

#### **Solution**:

```javascript
async function retryPromise(promiseFunc, retries) {
  for (let i = 1; i <= retries; i++) {
    try {
      const result = await promiseFunc();
      console.log(`Attempt ${i}: ${result}`);
      return;
    } catch (error) {
      console.log(`Attempt ${i}: ${error}`);
    }
  }
  console.log("All attempts failed");
}

// Simulated API
let attempt = 0;
function unreliableAPI() {
  return new Promise((resolve, reject) => {
    attempt++;
    if (attempt < 3) reject("Failure");
    else resolve("Success");
  });
}

// Example
retryPromise(unreliableAPI, 3);
```

---

#### **Explanation**:
1. **Retry Logic**:
   - A `for` loop executes the promise up to the specified retry count.
   - If the promise succeeds (`resolve`), the function exits.
   - If it fails (`reject`), the loop continues to the next attempt.

2. **Execution**:
   - The first two attempts fail, and the third attempt succeeds.

---

#### **Q6: Write an `async` function to implement a delay.**
- **Input Example**: `delay(2000)`  
- **Output**: Logs `Delayed for 2 seconds` after 2 seconds.

---

#### **Solution**:

```javascript
async function delay(ms) {
  await new Promise((resolve) => setTimeout(resolve, ms));
  console.log(`Delayed for ${ms / 1000} seconds`);
}

// Example
delay(2000);
```

---

#### **Explanation**:
1. **Delay Simulation**:
   - The `setTimeout` inside a promise ensures a delay for the specified milliseconds (`ms`).

2. **Execution**:
   - Logs the message after the delay.

---
Let’s proceed with **Week 4 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 4 Graded Questions**

---

#### **Q1: Predict the output of the following JavaScript code.**
**Code**:
```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function () {
  console.log(`Hello, my name is ${this.name}`);
};

const person1 = new Person("John");
person1.sayHello();
```
- **Options**:  
  1. `Hello, my name is John`  
  2. `Hello, my name is undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Hello, my name is John**

---

#### **Detailed Explanation**:

1. **Prototype Chain**:
   - The `sayHello` method is added to the `Person` prototype. All instances of `Person` inherit this method.

2. **Instance Creation**:
   - `person1` is created using the `Person` constructor. The `name` property is set to `"John"`.

3. **Execution**:
   - When `person1.sayHello()` is called, it accesses the `sayHello` method from the prototype and logs `"Hello, my name is John"`.

---

#### **Q2: What will be the output of the following code?**
**Code**:
```javascript
const obj = {
  name: "Alice",
  greet: function () {
    const sayHi = () => {
      console.log(`Hi, ${this.name}`);
    };
    sayHi();
  },
};

obj.greet();
```
- **Options**:  
  1. `Hi, Alice`  
  2. `Hi, undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Hi, Alice**

---

#### **Detailed Explanation**:

1. **Arrow Functions and `this`**:
   - Arrow functions do not have their own `this`. Instead, they inherit `this` from their surrounding lexical context.

2. **Execution**:
   - The `greet` method is invoked on `obj`, so `this` refers to `obj`.
   - Inside `sayHi`, `this.name` evaluates to `"Alice"`, and `"Hi, Alice"` is logged.

---

#### **Q3: Predict the output of this code involving `call`.**
**Code**:
```javascript
function greet(greeting) {
  console.log(`${greeting}, my name is ${this.name}`);
}

const user = { name: "Bob" };
greet.call(user, "Hello");
```
- **Options**:  
  1. `Hello, my name is Bob`  
  2. `Hello, my name is undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Hello, my name is Bob**

---

#### **Detailed Explanation**:

1. **`call` Method**:
   - The `call` method invokes a function with a specified `this` value and arguments.

2. **Execution**:
   - `this` is explicitly set to the `user` object, so `this.name` evaluates to `"Bob"`.
   - The greeting `"Hello, my name is Bob"` is logged.

---

#### **Q4: Predict the output of the following code using closures.**
**Code**:
```javascript
function createCounter() {
  let count = 0;
  return function () {
    count++;
    console.log(count);
  };
}

const counter = createCounter();
counter();
counter();
counter();
```
- **Options**:  
  1. `1 1 1`  
  2. `1 2 3`  
  3. `Error`  
  4. `0 1 2`

- **Answer**: **2. 1 2 3**

---

#### **Detailed Explanation**:

1. **Closure**:
   - A closure is a function that remembers variables from its enclosing scope, even after the outer function has returned.

2. **Execution**:
   - Each time `counter()` is called, the inner function increments and logs the `count` variable from the closure.

---

#### **Q5: Predict the output of the following code involving `bind`.**
**Code**:
```javascript
const obj = {
  name: "Charlie",
  greet: function () {
    console.log(`Hi, ${this.name}`);
  },
};

const greetFunc = obj.greet.bind(obj);
greetFunc();
```
- **Options**:  
  1. `Hi, Charlie`  
  2. `Hi, undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Hi, Charlie**

---

#### **Detailed Explanation**:

1. **`bind` Method**:
   - The `bind` method creates a new function with `this` explicitly set to the provided object (`obj` in this case).

2. **Execution**:
   - `greetFunc()` logs `"Hi, Charlie"`, as `this.name` refers to `"Charlie"` in the bound context.

---

#### **Q6: What will be the output of this code?**
**Code**:
```javascript
function outer() {
  let a = 10;
  return function inner() {
    console.log(a);
  };
}

const innerFunc = outer();
innerFunc();
```
- **Options**:  
  1. `10`  
  2. `undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. 10**

---

#### **Detailed Explanation**:

1. **Closure**:
   - The `inner` function forms a closure over the `outer` function's variables.
   - Even after `outer` returns, the `inner` function retains access to `a`.

2. **Execution**:
   - `innerFunc()` logs the value of `a` (`10`).

---

#### **Q7: Predict the output of this code involving the spread operator.**
**Code**:
```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const merged = { ...obj1, ...obj2 };
console.log(merged);
```
- **Options**:  
  1. `{ a: 1, b: 2, c: 4 }`  
  2. `{ a: 1, b: 3, c: 4 }`  
  3. `{ b: 3, c: 4 }`  
  4. `{ a: 1, c: 4 }`

- **Answer**: **2. { a: 1, b: 3, c: 4 }**

---

#### **Detailed Explanation**:

1. **Spread Operator**:
   - The spread operator (`...`) copies the properties of objects into a new object.

2. **Property Overwriting**:
   - Properties in `obj2` overwrite those in `obj1` if they share the same key (`b` in this case).

---

#### **Q8: What will be the output of the following code?**
**Code**:
```javascript
const arr = [1, 2, 3, 4];
const [a, , b] = arr;
console.log(a, b);
```
- **Options**:  
  1. `1 2`  
  2. `1 3`  
  3. `Error`  
  4. `undefined undefined`

- **Answer**: **2. 1 3**

---

#### **Detailed Explanation**:

1. **Array Destructuring**:
   - The `[a, , b]` pattern skips the second element (`2`) and assigns `1` to `a` and `3` to `b`.

2. **Output**:
   - Logs `1 3`.

---
Let’s proceed with **Week 4 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 4 Practice Questions**

---

#### **Q1: Write a function to merge two objects, giving priority to the second object’s properties.**
- **Input Example**:  
  ```javascript
  const obj1 = { a: 1, b: 2 };
  const obj2 = { b: 3, c: 4 };
  ```
- **Output**: `{ a: 1, b: 3, c: 4 }`

---

#### **Solution**:

```javascript
function mergeObjects(obj1, obj2) {
  return { ...obj1, ...obj2 };
}

// Example
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
console.log(mergeObjects(obj1, obj2)); // Output: { a: 1, b: 3, c: 4 }
```

---

#### **Explanation**:
1. **Spread Operator (`...`)**:
   - The spread operator copies all properties from one object to another.
   - When objects share keys, the properties of the latter object overwrite the former.

2. **Result**:
   - `obj2`’s `b: 3` overwrites `obj1`’s `b: 2`, while `c: 4` is added.

---

#### **Q2: Write a function to extract unique elements from an array.**
- **Input Example**: `[1, 2, 2, 3, 4, 4]`  
- **Output**: `[1, 2, 3, 4]`

---

#### **Solution**:

```javascript
function uniqueElements(arr) {
  return [...new Set(arr)];
}

// Example
console.log(uniqueElements([1, 2, 2, 3, 4, 4])); // Output: [1, 2, 3, 4]
```

---

#### **Explanation**:
1. **`Set` Object**:
   - A `Set` stores only unique values.
   - Converting an array to a `Set` removes duplicates.

2. **Spread Operator**:
   - Converts the `Set` back to an array for the output.

---

#### **Q3: Write a function to flatten a nested object.**
- **Input Example**:
  ```javascript
  const obj = {
    a: 1,
    b: { c: 2, d: { e: 3 } }
  };
  ```
- **Output**:
  ```javascript
  { "a": 1, "b.c": 2, "b.d.e": 3 }
  ```

---

#### **Solution**:

```javascript
function flattenObject(obj, parent = '', result = {}) {
  for (let key in obj) {
    const propName = parent ? `${parent}.${key}` : key;
    if (typeof obj[key] === 'object' && !Array.isArray(obj[key])) {
      flattenObject(obj[key], propName, result);
    } else {
      result[propName] = obj[key];
    }
  }
  return result;
}

// Example
const obj = { a: 1, b: { c: 2, d: { e: 3 } } };
console.log(flattenObject(obj));
// Output: { "a": 1, "b.c": 2, "b.d.e": 3 }
```

---

#### **Explanation**:
1. **Recursive Approach**:
   - Iterates through the object.
   - Concatenates parent keys with nested keys using `.`.

2. **Base Case**:
   - Adds non-object values directly to the `result`.

---

#### **Q4: Write a function to group an array of objects by a property.**
- **Input Example**:
  ```javascript
  const data = [
    { category: 'fruit', name: 'apple' },
    { category: 'fruit', name: 'banana' },
    { category: 'vegetable', name: 'carrot' }
  ];
  ```
- **Output**:
  ```javascript
  {
    fruit: [
      { category: 'fruit', name: 'apple' },
      { category: 'fruit', name: 'banana' }
    ],
    vegetable: [
      { category: 'vegetable', name: 'carrot' }
    ]
  }
  ```

---

#### **Solution**:

```javascript
function groupBy(arr, property) {
  return arr.reduce((result, item) => {
    const key = item[property];
    if (!result[key]) result[key] = [];
    result[key].push(item);
    return result;
  }, {});
}

// Example
const data = [
  { category: 'fruit', name: 'apple' },
  { category: 'fruit', name: 'banana' },
  { category: 'vegetable', name: 'carrot' }
];
console.log(groupBy(data, 'category'));
// Output:
// {
//   fruit: [
//     { category: 'fruit', name: 'apple' },
//     { category: 'fruit', name: 'banana' }
//   ],
//   vegetable: [
//     { category: 'vegetable', name: 'carrot' }
//   ]
// }
```

---

#### **Explanation**:
1. **`reduce` Function**:
   - Iterates through the array.
   - Groups objects into arrays based on the specified property.

2. **Result**:
   - Objects with the same category are grouped together.

---

#### **Q5: Write a function to deep clone an object.**
- **Input Example**:
  ```javascript
  const obj = { a: 1, b: { c: 2 } };
  const clone = deepClone(obj);
  clone.b.c = 3;
  console.log(obj.b.c); // Output: 2
  ```
- **Output**: The original object remains unchanged.

---

#### **Solution**:

```javascript
function deepClone(obj) {
  if (obj === null || typeof obj !== 'object') {
    return obj;
  }
  if (Array.isArray(obj)) {
    return obj.map(deepClone);
  }
  const result = {};
  for (let key in obj) {
    result[key] = deepClone(obj[key]);
  }
  return result;
}

// Example
const obj = { a: 1, b: { c: 2 } };
const clone = deepClone(obj);
clone.b.c = 3;
console.log(obj.b.c); // Output: 2
```

---

#### **Explanation**:
1. **Recursive Cloning**:
   - For arrays or objects, recursively clone each property or element.

2. **Base Case**:
   - For non-object values, return the value directly.

---

#### **Q6: Write a function to debounce another function.**
- **Input Example**:
  ```javascript
  function log() {
    console.log("Function executed");
  }
  const debouncedLog = debounce(log, 2000);
  debouncedLog();
  debouncedLog();
  debouncedLog();
  ```
- **Output**: Logs `"Function executed"` only once after 2 seconds.

---

#### **Solution**:

```javascript
function debounce(func, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => func(...args), delay);
  };
}

// Example
function log() {
  console.log("Function executed");
}
const debouncedLog = debounce(log, 2000);
debouncedLog();
debouncedLog();
debouncedLog();
```

---

#### **Explanation**:
1. **Debouncing**:
   - Ensures the function (`log`) is executed only after the specified delay (`2000ms`) has passed since the last call.

2. **Execution**:
   - Multiple calls within 2 seconds reset the timer, so the function executes only once.

---

Let’s proceed with **Week 4 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 4 Practice Questions**

---

#### **Q1: Write a function to merge two objects, giving priority to the second object’s properties.**
- **Input Example**:  
  ```javascript
  const obj1 = { a: 1, b: 2 };
  const obj2 = { b: 3, c: 4 };
  ```
- **Output**: `{ a: 1, b: 3, c: 4 }`

---

#### **Solution**:

```javascript
function mergeObjects(obj1, obj2) {
  return { ...obj1, ...obj2 };
}

// Example
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
console.log(mergeObjects(obj1, obj2)); // Output: { a: 1, b: 3, c: 4 }
```

---

#### **Explanation**:
1. **Spread Operator (`...`)**:
   - The spread operator copies all properties from one object to another.
   - When objects share keys, the properties of the latter object overwrite the former.

2. **Result**:
   - `obj2`’s `b: 3` overwrites `obj1`’s `b: 2`, while `c: 4` is added.

---

#### **Q2: Write a function to extract unique elements from an array.**
- **Input Example**: `[1, 2, 2, 3, 4, 4]`  
- **Output**: `[1, 2, 3, 4]`

---

#### **Solution**:

```javascript
function uniqueElements(arr) {
  return [...new Set(arr)];
}

// Example
console.log(uniqueElements([1, 2, 2, 3, 4, 4])); // Output: [1, 2, 3, 4]
```

---

#### **Explanation**:
1. **`Set` Object**:
   - A `Set` stores only unique values.
   - Converting an array to a `Set` removes duplicates.

2. **Spread Operator**:
   - Converts the `Set` back to an array for the output.

---

#### **Q3: Write a function to flatten a nested object.**
- **Input Example**:
  ```javascript
  const obj = {
    a: 1,
    b: { c: 2, d: { e: 3 } }
  };
  ```
- **Output**:
  ```javascript
  { "a": 1, "b.c": 2, "b.d.e": 3 }
  ```

---

#### **Solution**:

```javascript
function flattenObject(obj, parent = '', result = {}) {
  for (let key in obj) {
    const propName = parent ? `${parent}.${key}` : key;
    if (typeof obj[key] === 'object' && !Array.isArray(obj[key])) {
      flattenObject(obj[key], propName, result);
    } else {
      result[propName] = obj[key];
    }
  }
  return result;
}

// Example
const obj = { a: 1, b: { c: 2, d: { e: 3 } } };
console.log(flattenObject(obj));
// Output: { "a": 1, "b.c": 2, "b.d.e": 3 }
```

---

#### **Explanation**:
1. **Recursive Approach**:
   - Iterates through the object.
   - Concatenates parent keys with nested keys using `.`.

2. **Base Case**:
   - Adds non-object values directly to the `result`.

---

#### **Q4: Write a function to group an array of objects by a property.**
- **Input Example**:
  ```javascript
  const data = [
    { category: 'fruit', name: 'apple' },
    { category: 'fruit', name: 'banana' },
    { category: 'vegetable', name: 'carrot' }
  ];
  ```
- **Output**:
  ```javascript
  {
    fruit: [
      { category: 'fruit', name: 'apple' },
      { category: 'fruit', name: 'banana' }
    ],
    vegetable: [
      { category: 'vegetable', name: 'carrot' }
    ]
  }
  ```

---

#### **Solution**:

```javascript
function groupBy(arr, property) {
  return arr.reduce((result, item) => {
    const key = item[property];
    if (!result[key]) result[key] = [];
    result[key].push(item);
    return result;
  }, {});
}

// Example
const data = [
  { category: 'fruit', name: 'apple' },
  { category: 'fruit', name: 'banana' },
  { category: 'vegetable', name: 'carrot' }
];
console.log(groupBy(data, 'category'));
// Output:
// {
//   fruit: [
//     { category: 'fruit', name: 'apple' },
//     { category: 'fruit', name: 'banana' }
//   ],
//   vegetable: [
//     { category: 'vegetable', name: 'carrot' }
//   ]
// }
```

---

#### **Explanation**:
1. **`reduce` Function**:
   - Iterates through the array.
   - Groups objects into arrays based on the specified property.

2. **Result**:
   - Objects with the same category are grouped together.

---

#### **Q5: Write a function to deep clone an object.**
- **Input Example**:
  ```javascript
  const obj = { a: 1, b: { c: 2 } };
  const clone = deepClone(obj);
  clone.b.c = 3;
  console.log(obj.b.c); // Output: 2
  ```
- **Output**: The original object remains unchanged.

---

#### **Solution**:

```javascript
function deepClone(obj) {
  if (obj === null || typeof obj !== 'object') {
    return obj;
  }
  if (Array.isArray(obj)) {
    return obj.map(deepClone);
  }
  const result = {};
  for (let key in obj) {
    result[key] = deepClone(obj[key]);
  }
  return result;
}

// Example
const obj = { a: 1, b: { c: 2 } };
const clone = deepClone(obj);
clone.b.c = 3;
console.log(obj.b.c); // Output: 2
```

---

#### **Explanation**:
1. **Recursive Cloning**:
   - For arrays or objects, recursively clone each property or element.

2. **Base Case**:
   - For non-object values, return the value directly.

---

#### **Q6: Write a function to debounce another function.**
- **Input Example**:
  ```javascript
  function log() {
    console.log("Function executed");
  }
  const debouncedLog = debounce(log, 2000);
  debouncedLog();
  debouncedLog();
  debouncedLog();
  ```
- **Output**: Logs `"Function executed"` only once after 2 seconds.

---

#### **Solution**:

```javascript
function debounce(func, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => func(...args), delay);
  };
}

// Example
function log() {
  console.log("Function executed");
}
const debouncedLog = debounce(log, 2000);
debouncedLog();
debouncedLog();
debouncedLog();
```

---

#### **Explanation**:
1. **Debouncing**:
   - Ensures the function (`log`) is executed only after the specified delay (`2000ms`) has passed since the last call.

2. **Execution**:
   - Multiple calls within 2 seconds reset the timer, so the function executes only once.

---

Let’s proceed with **Week 5 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 5 Practice Questions**

---

#### **Q1: Write a function to store and retrieve an object in `localStorage`.**
- **Input Example**:
  ```javascript
  const user = { name: "John", age: 30 };
  saveToLocalStorage("user", user);
  const retrievedUser = getFromLocalStorage("user");
  console.log(retrievedUser); // Output: { name: "John", age: 30 }
  ```

---

#### **Solution**:

```javascript
function saveToLocalStorage(key, value) {
  localStorage.setItem(key, JSON.stringify(value));
}

function getFromLocalStorage(key) {
  const data = localStorage.getItem(key);
  return data ? JSON.parse(data) : null;
}

// Example
const user = { name: "John", age: 30 };
saveToLocalStorage("user", user);
const retrievedUser = getFromLocalStorage("user");
console.log(retrievedUser); // Output: { name: "John", age: 30 }
```

---

#### **Explanation**:
1. **`localStorage`**:
   - Stores only strings, so objects must be serialized using `JSON.stringify`.

2. **`JSON.parse`**:
   - Converts the retrieved string back into an object.

3. **Execution**:
   - The user object is saved as a string and then retrieved and parsed into its original format.

---

#### **Q2: Write a function to implement a simple cookie manager.**
- **Input Example**:
  ```javascript
  setCookie("username", "Alice", 7);
  console.log(getCookie("username")); // Output: Alice
  ```

---

#### **Solution**:

```javascript
function setCookie(name, value, days) {
  const expires = new Date(Date.now() + days * 864e5).toUTCString();
  document.cookie = `${name}=${value}; expires=${expires}; path=/`;
}

function getCookie(name) {
  const cookies = document.cookie.split("; ");
  const cookie = cookies.find((c) => c.startsWith(`${name}=`));
  return cookie ? cookie.split("=")[1] : null;
}

// Example
setCookie("username", "Alice", 7);
console.log(getCookie("username")); // Output: Alice
```

---

#### **Explanation**:
1. **Setting Cookies**:
   - The `setCookie` function formats the cookie string with a name, value, expiration date, and path.

2. **Retrieving Cookies**:
   - The `getCookie` function parses `document.cookie`, which contains all cookies as a single string.

---

#### **Q3: Write a function to check if a key exists in `sessionStorage`.**
- **Input Example**:
  ```javascript
  sessionStorage.setItem("user", "Alice");
  console.log(hasKeyInSessionStorage("user")); // Output: true
  console.log(hasKeyInSessionStorage("age")); // Output: false
  ```

---

#### **Solution**:

```javascript
function hasKeyInSessionStorage(key) {
  return sessionStorage.getItem(key) !== null;
}

// Example
sessionStorage.setItem("user", "Alice");
console.log(hasKeyInSessionStorage("user")); // Output: true
console.log(hasKeyInSessionStorage("age")); // Output: false
```

---

#### **Explanation**:
1. **`getItem` Method**:
   - Returns `null` if the key does not exist in `sessionStorage`.

2. **Execution**:
   - The function checks for `null` to determine if the key exists.

---

#### **Q4: Write a function to remove all items from `localStorage`.**
- **Input Example**:
  ```javascript
  localStorage.setItem("key1", "value1");
  localStorage.setItem("key2", "value2");
  clearLocalStorage();
  console.log(localStorage.getItem("key1")); // Output: null
  console.log(localStorage.getItem("key2")); // Output: null
  ```

---

#### **Solution**:

```javascript
function clearLocalStorage() {
  localStorage.clear();
}

// Example
localStorage.setItem("key1", "value1");
localStorage.setItem("key2", "value2");
clearLocalStorage();
console.log(localStorage.getItem("key1")); // Output: null
console.log(localStorage.getItem("key2")); // Output: null
```

---

#### **Explanation**:
1. **`clear` Method**:
   - Removes all key-value pairs from `localStorage`.

2. **Execution**:
   - After calling `clear`, `localStorage` is empty.

---

#### **Q5: Write a function to count the total number of keys in `localStorage`.**
- **Input Example**:
  ```javascript
  localStorage.setItem("key1", "value1");
  localStorage.setItem("key2", "value2");
  console.log(countLocalStorageKeys()); // Output: 2
  ```

---

#### **Solution**:

```javascript
function countLocalStorageKeys() {
  return localStorage.length;
}

// Example
localStorage.setItem("key1", "value1");
localStorage.setItem("key2", "value2");
console.log(countLocalStorageKeys()); // Output: 2
```

---

#### **Explanation**:
1. **`length` Property**:
   - Returns the number of key-value pairs stored in `localStorage`.

2. **Execution**:
   - The function simply returns the value of `localStorage.length`.

---

#### **Q6: Write a function to list all keys in `sessionStorage`.**
- **Input Example**:
  ```javascript
  sessionStorage.setItem("key1", "value1");
  sessionStorage.setItem("key2", "value2");
  console.log(listSessionStorageKeys()); // Output: ["key1", "key2"]
  ```

---

#### **Solution**:

```javascript
function listSessionStorageKeys() {
  const keys = [];
  for (let i = 0; i < sessionStorage.length; i++) {
    keys.push(sessionStorage.key(i));
  }
  return keys;
}

// Example
sessionStorage.setItem("key1", "value1");
sessionStorage.setItem("key2", "value2");
console.log(listSessionStorageKeys()); // Output: ["key1", "key2"]
```

---

#### **Explanation**:
1. **`key` Method**:
   - `sessionStorage.key(i)` retrieves the key at index `i`.

2. **Looping**:
   - Iterates over the keys using `sessionStorage.length`.

---

#### **Q7: Write a function to implement a retry mechanism for a failing API call.**
- **Input Example**:
  ```javascript
  let attempt = 0;
  function unreliableAPI() {
    return new Promise((resolve, reject) => {
      attempt++;
      if (attempt < 3) reject("Failure");
      else resolve("Success");
    });
  }

  retry(unreliableAPI, 3).then(console.log).catch(console.error);
  ```
- **Output Example**:
  - `Attempt 1: Failure`  
  - `Attempt 2: Failure`  
  - `Attempt 3: Success`

---

#### **Solution**:

```javascript
async function retry(apiFunc, retries) {
  for (let i = 1; i <= retries; i++) {
    try {
      const result = await apiFunc();
      console.log(`Attempt ${i}: ${result}`);
      return result;
    } catch (error) {
      console.log(`Attempt ${i}: ${error}`);
      if (i === retries) throw error;
    }
  }
}

// Example
let attempt = 0;
function unreliableAPI() {
  return new Promise((resolve, reject) => {
    attempt++;
    if (attempt < 3) reject("Failure");
    else resolve("Success");
  });
}

retry(unreliableAPI, 3).then(console.log).catch(console.error);
```

---

#### **Explanation**:
1. **Retry Logic**:
   - Attempts the API call up to the specified retry limit.

2. **Execution**:
   - Logs failures and retries until the call succeeds or retries are exhausted.

---
Let’s proceed with **Week 5 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 5 Practice Questions**

---

#### **Q1: Write a function to store and retrieve an object in `localStorage`.**
- **Input Example**:
  ```javascript
  const user = { name: "John", age: 30 };
  saveToLocalStorage("user", user);
  const retrievedUser = getFromLocalStorage("user");
  console.log(retrievedUser); // Output: { name: "John", age: 30 }
  ```

---

#### **Solution**:

```javascript
function saveToLocalStorage(key, value) {
  localStorage.setItem(key, JSON.stringify(value));
}

function getFromLocalStorage(key) {
  const data = localStorage.getItem(key);
  return data ? JSON.parse(data) : null;
}

// Example
const user = { name: "John", age: 30 };
saveToLocalStorage("user", user);
const retrievedUser = getFromLocalStorage("user");
console.log(retrievedUser); // Output: { name: "John", age: 30 }
```

---

#### **Explanation**:
1. **`localStorage`**:
   - Stores only strings, so objects must be serialized using `JSON.stringify`.

2. **`JSON.parse`**:
   - Converts the retrieved string back into an object.

3. **Execution**:
   - The user object is saved as a string and then retrieved and parsed into its original format.

---

#### **Q2: Write a function to implement a simple cookie manager.**
- **Input Example**:
  ```javascript
  setCookie("username", "Alice", 7);
  console.log(getCookie("username")); // Output: Alice
  ```

---

#### **Solution**:

```javascript
function setCookie(name, value, days) {
  const expires = new Date(Date.now() + days * 864e5).toUTCString();
  document.cookie = `${name}=${value}; expires=${expires}; path=/`;
}

function getCookie(name) {
  const cookies = document.cookie.split("; ");
  const cookie = cookies.find((c) => c.startsWith(`${name}=`));
  return cookie ? cookie.split("=")[1] : null;
}

// Example
setCookie("username", "Alice", 7);
console.log(getCookie("username")); // Output: Alice
```

---

#### **Explanation**:
1. **Setting Cookies**:
   - The `setCookie` function formats the cookie string with a name, value, expiration date, and path.

2. **Retrieving Cookies**:
   - The `getCookie` function parses `document.cookie`, which contains all cookies as a single string.

---

#### **Q3: Write a function to check if a key exists in `sessionStorage`.**
- **Input Example**:
  ```javascript
  sessionStorage.setItem("user", "Alice");
  console.log(hasKeyInSessionStorage("user")); // Output: true
  console.log(hasKeyInSessionStorage("age")); // Output: false
  ```

---

#### **Solution**:

```javascript
function hasKeyInSessionStorage(key) {
  return sessionStorage.getItem(key) !== null;
}

// Example
sessionStorage.setItem("user", "Alice");
console.log(hasKeyInSessionStorage("user")); // Output: true
console.log(hasKeyInSessionStorage("age")); // Output: false
```

---

#### **Explanation**:
1. **`getItem` Method**:
   - Returns `null` if the key does not exist in `sessionStorage`.

2. **Execution**:
   - The function checks for `null` to determine if the key exists.

---

#### **Q4: Write a function to remove all items from `localStorage`.**
- **Input Example**:
  ```javascript
  localStorage.setItem("key1", "value1");
  localStorage.setItem("key2", "value2");
  clearLocalStorage();
  console.log(localStorage.getItem("key1")); // Output: null
  console.log(localStorage.getItem("key2")); // Output: null
  ```

---

#### **Solution**:

```javascript
function clearLocalStorage() {
  localStorage.clear();
}

// Example
localStorage.setItem("key1", "value1");
localStorage.setItem("key2", "value2");
clearLocalStorage();
console.log(localStorage.getItem("key1")); // Output: null
console.log(localStorage.getItem("key2")); // Output: null
```

---

#### **Explanation**:
1. **`clear` Method**:
   - Removes all key-value pairs from `localStorage`.

2. **Execution**:
   - After calling `clear`, `localStorage` is empty.

---

#### **Q5: Write a function to count the total number of keys in `localStorage`.**
- **Input Example**:
  ```javascript
  localStorage.setItem("key1", "value1");
  localStorage.setItem("key2", "value2");
  console.log(countLocalStorageKeys()); // Output: 2
  ```

---

#### **Solution**:

```javascript
function countLocalStorageKeys() {
  return localStorage.length;
}

// Example
localStorage.setItem("key1", "value1");
localStorage.setItem("key2", "value2");
console.log(countLocalStorageKeys()); // Output: 2
```

---

#### **Explanation**:
1. **`length` Property**:
   - Returns the number of key-value pairs stored in `localStorage`.

2. **Execution**:
   - The function simply returns the value of `localStorage.length`.

---

#### **Q6: Write a function to list all keys in `sessionStorage`.**
- **Input Example**:
  ```javascript
  sessionStorage.setItem("key1", "value1");
  sessionStorage.setItem("key2", "value2");
  console.log(listSessionStorageKeys()); // Output: ["key1", "key2"]
  ```

---

#### **Solution**:

```javascript
function listSessionStorageKeys() {
  const keys = [];
  for (let i = 0; i < sessionStorage.length; i++) {
    keys.push(sessionStorage.key(i));
  }
  return keys;
}

// Example
sessionStorage.setItem("key1", "value1");
sessionStorage.setItem("key2", "value2");
console.log(listSessionStorageKeys()); // Output: ["key1", "key2"]
```

---

#### **Explanation**:
1. **`key` Method**:
   - `sessionStorage.key(i)` retrieves the key at index `i`.

2. **Looping**:
   - Iterates over the keys using `sessionStorage.length`.

---

#### **Q7: Write a function to implement a retry mechanism for a failing API call.**
- **Input Example**:
  ```javascript
  let attempt = 0;
  function unreliableAPI() {
    return new Promise((resolve, reject) => {
      attempt++;
      if (attempt < 3) reject("Failure");
      else resolve("Success");
    });
  }

  retry(unreliableAPI, 3).then(console.log).catch(console.error);
  ```
- **Output Example**:
  - `Attempt 1: Failure`  
  - `Attempt 2: Failure`  
  - `Attempt 3: Success`

---

#### **Solution**:

```javascript
async function retry(apiFunc, retries) {
  for (let i = 1; i <= retries; i++) {
    try {
      const result = await apiFunc();
      console.log(`Attempt ${i}: ${result}`);
      return result;
    } catch (error) {
      console.log(`Attempt ${i}: ${error}`);
      if (i === retries) throw error;
    }
  }
}

// Example
let attempt = 0;
function unreliableAPI() {
  return new Promise((resolve, reject) => {
    attempt++;
    if (attempt < 3) reject("Failure");
    else resolve("Success");
  });
}

retry(unreliableAPI, 3).then(console.log).catch(console.error);
```

---

#### **Explanation**:
1. **Retry Logic**:
   - Attempts the API call up to the specified retry limit.

2. **Execution**:
   - Logs failures and retries until the call succeeds or retries are exhausted.

---
Let’s proceed with **Week 6 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 6 Practice Questions**

---

#### **Q1: Write a script to create a file and write data to it using `fs` in Node.js.**
- **Input Example**:  
  - Filename: `example.txt`  
  - Data: `"Node.js is awesome!"`  
- **Expected Output**: The file `example.txt` is created with the content `"Node.js is awesome!"`.

---

#### **Solution**:

```javascript
const fs = require('fs');

function writeToFile(filename, data) {
  fs.writeFileSync(filename, data);
  console.log(`File ${filename} created with data: "${data}"`);
}

// Example
writeToFile('example.txt', 'Node.js is awesome!');
```

---

#### **Explanation**:
1. **`fs.writeFileSync`**:
   - Synchronously writes data to a file. If the file does not exist, it creates one.

2. **Execution**:
   - Creates `example.txt` with the specified content.
   - Logs a confirmation message.

---

#### **Q2: Write a script to read the content of a file using `fs`.**
- **Input Example**:  
  - Filename: `example.txt`  
- **Expected Output**: Logs the file content, e.g., `"Node.js is awesome!"`.

---

#### **Solution**:

```javascript
const fs = require('fs');

function readFromFile(filename) {
  if (fs.existsSync(filename)) {
    const content = fs.readFileSync(filename, 'utf8');
    console.log(`File content: "${content}"`);
  } else {
    console.log(`File "${filename}" does not exist.`);
  }
}

// Example
readFromFile('example.txt');
```

---

#### **Explanation**:
1. **`fs.readFileSync`**:
   - Reads the content of the file synchronously.
   - The second argument (`'utf8'`) specifies the encoding for reading the file.

2. **File Existence Check**:
   - Uses `fs.existsSync` to ensure the file exists before attempting to read it.

---

#### **Q3: Write a script to delete a file using `fs`.**
- **Input Example**:  
  - Filename: `example.txt`  
- **Expected Output**: The file is deleted, and a confirmation message is logged.

---

#### **Solution**:

```javascript
const fs = require('fs');

function deleteFile(filename) {
  if (fs.existsSync(filename)) {
    fs.unlinkSync(filename);
    console.log(`File "${filename}" deleted.`);
  } else {
    console.log(`File "${filename}" does not exist.`);
  }
}

// Example
deleteFile('example.txt');
```

---

#### **Explanation**:
1. **`fs.unlinkSync`**:
   - Deletes the specified file synchronously.

2. **File Existence Check**:
   - Ensures the file exists before attempting to delete it.

---

#### **Q4: Write a script to create a directory using `fs`.**
- **Input Example**:  
  - Directory Name: `exampleDir`  
- **Expected Output**: The directory `exampleDir` is created.

---

#### **Solution**:

```javascript
const fs = require('fs');

function createDirectory(dirname) {
  if (!fs.existsSync(dirname)) {
    fs.mkdirSync(dirname);
    console.log(`Directory "${dirname}" created.`);
  } else {
    console.log(`Directory "${dirname}" already exists.`);
  }
}

// Example
createDirectory('exampleDir');
```

---

#### **Explanation**:
1. **`fs.mkdirSync`**:
   - Creates a new directory synchronously.

2. **Execution**:
   - Checks if the directory already exists before creating it.

---

#### **Q5: Write a script to list all files in a directory using `fs`.**
- **Input Example**:  
  - Directory Name: `exampleDir`  
- **Expected Output**: Logs the names of all files in the directory.

---

#### **Solution**:

```javascript
const fs = require('fs');

function listFilesInDirectory(dirname) {
  if (fs.existsSync(dirname)) {
    const files = fs.readdirSync(dirname);
    console.log(`Files in "${dirname}":`, files);
  } else {
    console.log(`Directory "${dirname}" does not exist.`);
  }
}

// Example
listFilesInDirectory('exampleDir');
```

---

#### **Explanation**:
1. **`fs.readdirSync`**:
   - Reads the contents of a directory synchronously and returns an array of filenames.

2. **Execution**:
   - Ensures the directory exists before attempting to list its contents.

---

#### **Q6: Write a script to read the command-line arguments passed to a Node.js script.**
- **Input Example**:  
  - Command: `node script.js arg1 arg2`  
- **Expected Output**: Logs the arguments: `["arg1", "arg2"]`.

---

#### **Solution**:

```javascript
function readCommandLineArgs() {
  const args = process.argv.slice(2);
  console.log("Command-line arguments:", args);
}

// Example
readCommandLineArgs();
```

---

#### **Explanation**:
1. **`process.argv`**:
   - Contains an array of command-line arguments.
   - The first two elements are:
     - Path to the Node.js executable.
     - Path to the script file.

2. **Slicing**:
   - `slice(2)` skips the first two elements to retrieve only user-provided arguments.

---

#### **Q7: Write a script to get the absolute path of a file using `path`.**
- **Input Example**:  
  - Filename: `example.txt`  
- **Expected Output**: Logs the absolute path to `example.txt`.

---

#### **Solution**:

```javascript
const path = require('path');

function getAbsolutePath(filename) {
  const absolutePath = path.resolve(filename);
  console.log(`Absolute path of "${filename}":`, absolutePath);
}

// Example
getAbsolutePath('example.txt');
```

---

#### **Explanation**:
1. **`path.resolve`**:
   - Resolves a file path into an absolute path based on the current working directory.

2. **Execution**:
   - Logs the absolute path of the specified file.

---

#### **Q8: Write a script to get the total free memory on the system using `os`.**
- **Expected Output**: Logs the free memory in bytes.

---

#### **Solution**:

```javascript
const os = require('os');

function getFreeMemory() {
  const freeMemory = os.freemem();
  console.log(`Free memory: ${freeMemory} bytes`);
}

// Example
getFreeMemory();
```

---

#### **Explanation**:
1. **`os.freemem`**:
   - Returns the amount of free system memory in bytes.

2. **Execution**:
   - Logs the available memory on the system.

---
Let’s proceed with **Week 6 Practice Questions**, providing detailed solutions and explanations.

---
Let’s move on to **Week 7 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 7 Graded Questions**

---

#### **Q1: What will the following `setTimeout` code output?**
**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside Timeout");
}, 0);

console.log("End");
```
- **Options**:  
  1. `Start`, `End`, `Inside Timeout`  
  2. `Start`, `Inside Timeout`, `End`  
  3. `Inside Timeout`, `Start`, `End`  
  4. `Start`, `End`

- **Answer**: **1. Start, End, Inside Timeout**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - JavaScript is single-threaded and processes tasks in an event loop.
   - The `setTimeout` callback is placed in the **task queue** and executed only after the **main execution stack** is empty.

2. **Execution Order**:
   - `"Start"` is logged immediately.
   - `"End"` is logged after `"Start"` since `setTimeout` doesn’t block execution.
   - `"Inside Timeout"` is logged last when the callback executes from the task queue.

---

#### **Q2: Predict the output of this promise-based code.**
**Code**:
```javascript
console.log("Start");

const promise = new Promise((resolve) => {
  console.log("Inside Promise");
  resolve("Resolved");
});

promise.then((result) => {
  console.log(result);
});

console.log("End");
```
- **Options**:  
  1. `Start`, `Inside Promise`, `End`, `Resolved`  
  2. `Start`, `Inside Promise`, `Resolved`, `End`  
  3. `Start`, `Resolved`, `Inside Promise`, `End`  
  4. `Inside Promise`, `Start`, `End`, `Resolved`

- **Answer**: **1. Start, Inside Promise, End, Resolved**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - The `console.log` inside the `Promise` constructor runs immediately, logging `"Inside Promise"`.
   - The `then` callback is queued in the **microtask queue** and runs after the main execution stack is cleared.

2. **Execution Order**:
   - `"Start"` logs first.
   - `"Inside Promise"` logs immediately.
   - `"End"` logs after the promise constructor completes.
   - `"Resolved"` logs last, as it is part of the microtask queue.

---

#### **Q3: What will be the output of this code using `async`/`await`?**
**Code**:
```javascript
async function example() {
  console.log("Start");
  const result = await Promise.resolve("Resolved");
  console.log(result);
  console.log("End");
}

example();
console.log("Outside");
```
- **Options**:  
  1. `Start`, `Resolved`, `End`, `Outside`  
  2. `Start`, `Outside`, `Resolved`, `End`  
  3. `Start`, `End`, `Resolved`, `Outside`  
  4. `Outside`, `Start`, `Resolved`, `End`

- **Answer**: **2. Start, Outside, Resolved, End**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - `"Start"` is logged immediately when `example` runs.
   - The `await` pauses execution of `example`, queuing the `then` callback.
   - `"Outside"` logs next, as it is part of the main thread.
   - `"Resolved"` and `"End"` log after the promise resolves.

---

#### **Q4: What will this `setInterval` code log?**
**Code**:
```javascript
let count = 0;
const interval = setInterval(() => {
  console.log(count);
  count++;
  if (count === 3) clearInterval(interval);
}, 1000);
```
- **Options**:  
  1. `0`, `1`, `2`  
  2. `0`, `1`, `2`, `3`  
  3. `0`, `1`  
  4. `0`, `1`, `2`, `3`, `4`

- **Answer**: **1. 0, 1, 2**

---

#### **Detailed Explanation**:

1. **`setInterval`**:
   - Executes the callback every 1000ms.

2. **Execution**:
   - Logs `count` (`0`, `1`, `2`) each second.
   - Stops when `count` reaches `3` using `clearInterval`.

---

#### **Q5: What will this code output?**
**Code**:
```javascript
function fetchData() {
  return new Promise((resolve, reject) => {
    setTimeout(() => reject("Error"), 1000);
  });
}

fetchData()
  .then((data) => console.log(data))
  .catch((error) => console.log(error));
```
- **Options**:  
  1. `Error`  
  2. `Error`, `undefined`  
  3. `undefined`  
  4. `No output`

- **Answer**: **1. Error**

---

#### **Detailed Explanation**:

1. **Promise Rejection**:
   - The `fetchData` promise rejects with `"Error"` after 1 second.

2. **Execution**:
   - The `.catch` block handles the rejection and logs `"Error"`.

---

#### **Q6: What is logged in this closure-based counter?**
**Code**:
```javascript
function counter() {
  let count = 0;
  return function () {
    count++;
    console.log(count);
  };
}

const increment = counter();
increment();
increment();
increment();
```
- **Options**:  
  1. `1`, `2`, `3`  
  2. `0`, `1`, `2`  
  3. `Error`  
  4. `undefined`

- **Answer**: **1. 1, 2, 3**

---

#### **Detailed Explanation**:

1. **Closure**:
   - The inner function retains access to `count` in the outer function's scope.

2. **Execution**:
   - Each call to `increment` increases `count` by `1` and logs its value.

---

#### **Q7: What will be logged in this destructuring example?**
**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
const { a, ...rest } = obj;
console.log(a);
console.log(rest);
```
- **Options**:  
  1. `1`, `{ b: 2, c: 3 }`  
  2. `undefined`, `{ a: 1, b: 2, c: 3 }`  
  3. `1`, `{}`  
  4. `Error`

- **Answer**: **1. 1, { b: 2, c: 3 }**

---

#### **Detailed Explanation**:

1. **Object Destructuring**:
   - Extracts `a` from `obj` and groups the remaining properties into `rest`.

2. **Execution**:
   - Logs `1` for `a` and `{ b: 2, c: 3 }` for `rest`.

---

#### **Q8: Predict the output of this array destructuring example.**
**Code**:
```javascript
const arr = [1, 2, 3, 4];
const [first, , third] = arr;
console.log(first, third);
```
- **Options**:  
  1. `1 3`  
  2. `2 3`  
  3. `undefined undefined`  
  4. `Error`

- **Answer**: **1. 1 3**

---

#### **Detailed Explanation**:

1. **Array Destructuring**:
   - Skips the second element by leaving an empty position.

2. **Execution**:
   - Assigns `1` to `first` and `3` to `third`.

---
Let’s continue with **Week 7 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 7 Practice Questions**

---

#### **Q1: Write a function that implements a delay using `Promise` and `setTimeout`.**
- **Input Example**:  
  ```javascript
  delay(2000).then(() => console.log("Executed after 2 seconds"));
  ```
- **Expected Output**: Logs `"Executed after 2 seconds"` after 2 seconds.

---

#### **Solution**:

```javascript
function delay(ms) {
  return new Promise((resolve) => setTimeout(resolve, ms));
}

// Example
delay(2000).then(() => console.log("Executed after 2 seconds"));
```

---

#### **Explanation**:
1. **`Promise` with `setTimeout`**:
   - The `setTimeout` function resolves the promise after the specified delay (`ms`).

2. **Execution**:
   - The `then` callback executes once the promise is resolved, logging the message after the delay.

---

#### **Q2: Write a function to execute multiple promises sequentially.**
- **Input Example**:  
  ```javascript
  const tasks = [
    () => Promise.resolve("Task 1 completed"),
    () => Promise.resolve("Task 2 completed"),
    () => Promise.resolve("Task 3 completed"),
  ];
  executeSequentially(tasks).then(() => console.log("All tasks completed"));
  ```
- **Expected Output**:  
  - Logs:  
    ```
    Task 1 completed
    Task 2 completed
    Task 3 completed
    All tasks completed
    ```

---

#### **Solution**:

```javascript
async function executeSequentially(tasks) {
  for (const task of tasks) {
    const result = await task();
    console.log(result);
  }
  console.log("All tasks completed");
}

// Example
const tasks = [
  () => Promise.resolve("Task 1 completed"),
  () => Promise.resolve("Task 2 completed"),
  () => Promise.resolve("Task 3 completed"),
];
executeSequentially(tasks);
```

---

#### **Explanation**:
1. **Sequential Execution**:
   - The `for` loop ensures tasks are awaited one at a time.

2. **Execution**:
   - Each task is executed in sequence, logging its result.

---

#### **Q3: Write a function to execute multiple promises in parallel and log their results.**
- **Input Example**:  
  ```javascript
  const promises = [
    Promise.resolve("Promise 1 resolved"),
    Promise.resolve("Promise 2 resolved"),
    Promise.resolve("Promise 3 resolved"),
  ];
  executeInParallel(promises).then(() => console.log("All promises resolved"));
  ```
- **Expected Output**:  
  - Logs:  
    ```
    Promise 1 resolved
    Promise 2 resolved
    Promise 3 resolved
    All promises resolved
    ```

---

#### **Solution**:

```javascript
async function executeInParallel(promises) {
  const results = await Promise.all(promises);
  results.forEach((result) => console.log(result));
  console.log("All promises resolved");
}

// Example
const promises = [
  Promise.resolve("Promise 1 resolved"),
  Promise.resolve("Promise 2 resolved"),
  Promise.resolve("Promise 3 resolved"),
];
executeInParallel(promises);
```

---

#### **Explanation**:
1. **Parallel Execution**:
   - `Promise.all` executes all promises concurrently.

2. **Execution**:
   - Logs results only after all promises have resolved.

---

#### **Q4: Write a function to retry a promise-based task up to a specified number of attempts.**
- **Input Example**:  
  ```javascript
  let attempt = 0;
  function unreliableTask() {
    return new Promise((resolve, reject) => {
      attempt++;
      if (attempt < 3) reject("Failed");
      else resolve("Success");
    });
  }
  retryTask(unreliableTask, 3).then(console.log).catch(console.error);
  ```
- **Expected Output**:  
  - Logs:  
    ```
    Attempt 1: Failed
    Attempt 2: Failed
    Attempt 3: Success
    ```

---

#### **Solution**:

```javascript
async function retryTask(task, retries) {
  for (let i = 1; i <= retries; i++) {
    try {
      const result = await task();
      console.log(`Attempt ${i}: ${result}`);
      return result;
    } catch (error) {
      console.log(`Attempt ${i}: ${error}`);
      if (i === retries) throw error;
    }
  }
}

// Example
let attempt = 0;
function unreliableTask() {
  return new Promise((resolve, reject) => {
    attempt++;
    if (attempt < 3) reject("Failed");
    else resolve("Success");
  });
}
retryTask(unreliableTask, 3).then(console.log).catch(console.error);
```

---

#### **Explanation**:
1. **Retry Logic**:
   - Retries the task up to the specified number of attempts.

2. **Execution**:
   - Logs each attempt’s result or error.

---

#### **Q5: Write a function to create a counter using closures.**
- **Input Example**:  
  ```javascript
  const counter = createCounter();
  console.log(counter.increment()); // Output: 1
  console.log(counter.increment()); // Output: 2
  console.log(counter.decrement()); // Output: 1
  ```
- **Expected Output**:  
  ```
  1
  2
  1
  ```

---

#### **Solution**:

```javascript
function createCounter() {
  let count = 0;
  return {
    increment: () => ++count,
    decrement: () => --count,
  };
}

// Example
const counter = createCounter();
console.log(counter.increment()); // Output: 1
console.log(counter.increment()); // Output: 2
console.log(counter.decrement()); // Output: 1
```

---

#### **Explanation**:
1. **Closures**:
   - The inner functions (`increment`, `decrement`) access `count` in the outer scope.

2. **Execution**:
   - The `count` variable is updated and returned with each method call.

---

#### **Q6: Write a function to find the maximum value in an array using `reduce`.**
- **Input Example**:  
  ```javascript
  const numbers = [10, 20, 30, 40];
  console.log(findMax(numbers)); // Output: 40
  ```
- **Expected Output**: `40`

---

#### **Solution**:

```javascript
function findMax(arr) {
  return arr.reduce((max, num) => (num > max ? num : max), -Infinity);
}

// Example
const numbers = [10, 20, 30, 40];
console.log(findMax(numbers)); // Output: 40
```

---

#### **Explanation**:
1. **`reduce`**:
   - Iterates over the array, comparing each element to the current maximum.

2. **Execution**:
   - Updates the maximum value at each iteration.

---

Let’s move on to **Week 8 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 8 Graded Questions**

---

#### **Q1: What will this asynchronous code log to the console?**
**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve("Resolved").then((value) => {
  console.log(value);
});

console.log("End");
```
- **Options**:  
  1. `Start`, `Timeout`, `Resolved`, `End`  
  2. `Start`, `Resolved`, `Timeout`, `End`  
  3. `Start`, `End`, `Resolved`, `Timeout`  
  4. `Start`, `Resolved`, `End`, `Timeout`

- **Answer**: **3. Start, End, Resolved, Timeout**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - JavaScript uses an **event loop** to manage synchronous and asynchronous code execution.
   - Synchronous tasks execute first, followed by **microtasks** (e.g., `Promise.then`), and then **macrotasks** (e.g., `setTimeout`).

2. **Order of Execution**:
   - `"Start"` is logged immediately.
   - `"End"` is logged next as it's also synchronous.
   - The `Promise` callback (`"Resolved"`) executes as a **microtask**.
   - The `setTimeout` callback (`"Timeout"`) executes last as a **macrotask**.

---

#### **Q2: Predict the output of this promise chaining code.**
**Code**:
```javascript
const promise = new Promise((resolve) => {
  resolve("First Resolve");
});

promise
  .then((data) => {
    console.log(data);
    return "Second Resolve";
  })
  .then((data) => {
    console.log(data);
    throw new Error("Something went wrong");
  })
  .catch((error) => {
    console.log(error.message);
  });
```
- **Options**:  
  1. `First Resolve`, `Second Resolve`, `Something went wrong`  
  2. `First Resolve`, `Second Resolve`  
  3. `First Resolve`, `Something went wrong`  
  4. `Error`

- **Answer**: **1. First Resolve, Second Resolve, Something went wrong**

---

#### **Detailed Explanation**:

1. **Promise Chaining**:
   - Each `.then` returns a new promise, allowing chaining of asynchronous operations.

2. **Execution**:
   - The first `.then` logs `"First Resolve"` and returns `"Second Resolve"`.
   - The second `.then` logs `"Second Resolve"` and throws an error.
   - The `.catch` block handles the error, logging `"Something went wrong"`.

---

#### **Q3: What will this async/await code output?**
**Code**:
```javascript
async function fetchData() {
  console.log("Fetching Data...");
  throw new Error("Fetch Failed");
}

fetchData()
  .then(() => console.log("Success"))
  .catch((error) => console.log(error.message));
```
- **Options**:  
  1. `Fetching Data...`, `Success`  
  2. `Fetching Data...`, `Fetch Failed`  
  3. `Error`, `Fetching Data...`  
  4. `Fetch Failed`

- **Answer**: **2. Fetching Data..., Fetch Failed**

---

#### **Detailed Explanation**:

1. **Async Function**:
   - Errors thrown inside an `async` function are automatically wrapped in a rejected promise.

2. **Execution**:
   - `"Fetching Data..."` logs immediately.
   - The promise rejects with `"Fetch Failed"`, and the `.catch` block handles the error.

---

#### **Q4: What will this destructuring code log?**
**Code**:
```javascript
const [first, ...rest] = [10, 20, 30, 40];
console.log(first);
console.log(rest);
```
- **Options**:  
  1. `10`, `[20, 30, 40]`  
  2. `10`, `[30, 40]`  
  3. `20`, `[30, 40]`  
  4. `10`, `[20]`

- **Answer**: **1. 10, [20, 30, 40]**

---

#### **Detailed Explanation**:

1. **Array Destructuring**:
   - The first element (`10`) is assigned to `first`.
   - The rest of the elements (`[20, 30, 40]`) are grouped into `rest` using the spread operator (`...`).

2. **Execution**:
   - Logs `10` for `first` and `[20, 30, 40]` for `rest`.

---

#### **Q5: Predict the output of this closure-based counter.**
**Code**:
```javascript
function createCounter() {
  let count = 0;
  return {
    increment: () => ++count,
    reset: () => (count = 0),
  };
}

const counter = createCounter();
console.log(counter.increment());
console.log(counter.increment());
counter.reset();
console.log(counter.increment());
```
- **Options**:  
  1. `1`, `2`, `1`  
  2. `1`, `1`, `1`  
  3. `1`, `2`, `2`  
  4. `Error`

- **Answer**: **1. 1, 2, 1**

---

#### **Detailed Explanation**:

1. **Closure**:
   - The `increment` and `reset` methods share access to the `count` variable within the outer function.

2. **Execution**:
   - The first `increment` call increases `count` to `1`.
   - The second `increment` call increases `count` to `2`.
   - The `reset` method sets `count` back to `0`.
   - The final `increment` call increases `count` to `1`.

---

#### **Q6: What will this code log?**
**Code**:
```javascript
const promise = new Promise((resolve, reject) => {
  reject("Error occurred");
});

promise
  .then(() => console.log("Resolved"))
  .catch(() => console.log("Caught"))
  .finally(() => console.log("Finally"));
```
- **Options**:  
  1. `Resolved`, `Finally`  
  2. `Caught`, `Finally`  
  3. `Error occurred`  
  4. `Finally`

- **Answer**: **2. Caught, Finally**

---

#### **Detailed Explanation**:

1. **Promise Rejection**:
   - The promise is rejected with `"Error occurred"`.

2. **`.catch`**:
   - Handles the rejection, logging `"Caught"`.

3. **`.finally`**:
   - Executes after the promise settles (either resolved or rejected), logging `"Finally"`.

---

#### **Q7: Predict the output of this `Object.entries` code.**
**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
const entries = Object.entries(obj);
console.log(entries);
```
- **Options**:  
  1. `[["a", 1], ["b", 2], ["c", 3]]`  
  2. `["a", 1, "b", 2, "c", 3]`  
  3. `[["a", "b", "c"], [1, 2, 3]]`  
  4. `Error`

- **Answer**: **1. [["a", 1], ["b", 2], ["c", 3]]**

---

#### **Detailed Explanation**:

1. **`Object.entries`**:
   - Converts an object into an array of key-value pairs.

2. **Execution**:
   - The keys (`a`, `b`, `c`) are paired with their corresponding values (`1`, `2`, `3`), forming an array of arrays.

---
Let’s move on to **Week 8 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 8 Graded Questions**

---

#### **Q1: What will this asynchronous code log to the console?**
**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout");
}, 0);

Promise.resolve("Resolved").then((value) => {
  console.log(value);
});

console.log("End");
```
- **Options**:  
  1. `Start`, `Timeout`, `Resolved`, `End`  
  2. `Start`, `Resolved`, `Timeout`, `End`  
  3. `Start`, `End`, `Resolved`, `Timeout`  
  4. `Start`, `Resolved`, `End`, `Timeout`

- **Answer**: **3. Start, End, Resolved, Timeout**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - JavaScript uses an **event loop** to manage synchronous and asynchronous code execution.
   - Synchronous tasks execute first, followed by **microtasks** (e.g., `Promise.then`), and then **macrotasks** (e.g., `setTimeout`).

2. **Order of Execution**:
   - `"Start"` is logged immediately.
   - `"End"` is logged next as it's also synchronous.
   - The `Promise` callback (`"Resolved"`) executes as a **microtask**.
   - The `setTimeout` callback (`"Timeout"`) executes last as a **macrotask**.

---

#### **Q2: Predict the output of this promise chaining code.**
**Code**:
```javascript
const promise = new Promise((resolve) => {
  resolve("First Resolve");
});

promise
  .then((data) => {
    console.log(data);
    return "Second Resolve";
  })
  .then((data) => {
    console.log(data);
    throw new Error("Something went wrong");
  })
  .catch((error) => {
    console.log(error.message);
  });
```
- **Options**:  
  1. `First Resolve`, `Second Resolve`, `Something went wrong`  
  2. `First Resolve`, `Second Resolve`  
  3. `First Resolve`, `Something went wrong`  
  4. `Error`

- **Answer**: **1. First Resolve, Second Resolve, Something went wrong**

---

#### **Detailed Explanation**:

1. **Promise Chaining**:
   - Each `.then` returns a new promise, allowing chaining of asynchronous operations.

2. **Execution**:
   - The first `.then` logs `"First Resolve"` and returns `"Second Resolve"`.
   - The second `.then` logs `"Second Resolve"` and throws an error.
   - The `.catch` block handles the error, logging `"Something went wrong"`.

---

#### **Q3: What will this async/await code output?**
**Code**:
```javascript
async function fetchData() {
  console.log("Fetching Data...");
  throw new Error("Fetch Failed");
}

fetchData()
  .then(() => console.log("Success"))
  .catch((error) => console.log(error.message));
```
- **Options**:  
  1. `Fetching Data...`, `Success`  
  2. `Fetching Data...`, `Fetch Failed`  
  3. `Error`, `Fetching Data...`  
  4. `Fetch Failed`

- **Answer**: **2. Fetching Data..., Fetch Failed**

---

#### **Detailed Explanation**:

1. **Async Function**:
   - Errors thrown inside an `async` function are automatically wrapped in a rejected promise.

2. **Execution**:
   - `"Fetching Data..."` logs immediately.
   - The promise rejects with `"Fetch Failed"`, and the `.catch` block handles the error.

---

#### **Q4: What will this destructuring code log?**
**Code**:
```javascript
const [first, ...rest] = [10, 20, 30, 40];
console.log(first);
console.log(rest);
```
- **Options**:  
  1. `10`, `[20, 30, 40]`  
  2. `10`, `[30, 40]`  
  3. `20`, `[30, 40]`  
  4. `10`, `[20]`

- **Answer**: **1. 10, [20, 30, 40]**

---

#### **Detailed Explanation**:

1. **Array Destructuring**:
   - The first element (`10`) is assigned to `first`.
   - The rest of the elements (`[20, 30, 40]`) are grouped into `rest` using the spread operator (`...`).

2. **Execution**:
   - Logs `10` for `first` and `[20, 30, 40]` for `rest`.

---

#### **Q5: Predict the output of this closure-based counter.**
**Code**:
```javascript
function createCounter() {
  let count = 0;
  return {
    increment: () => ++count,
    reset: () => (count = 0),
  };
}

const counter = createCounter();
console.log(counter.increment());
console.log(counter.increment());
counter.reset();
console.log(counter.increment());
```
- **Options**:  
  1. `1`, `2`, `1`  
  2. `1`, `1`, `1`  
  3. `1`, `2`, `2`  
  4. `Error`

- **Answer**: **1. 1, 2, 1**

---

#### **Detailed Explanation**:

1. **Closure**:
   - The `increment` and `reset` methods share access to the `count` variable within the outer function.

2. **Execution**:
   - The first `increment` call increases `count` to `1`.
   - The second `increment` call increases `count` to `2`.
   - The `reset` method sets `count` back to `0`.
   - The final `increment` call increases `count` to `1`.

---

#### **Q6: What will this code log?**
**Code**:
```javascript
const promise = new Promise((resolve, reject) => {
  reject("Error occurred");
});

promise
  .then(() => console.log("Resolved"))
  .catch(() => console.log("Caught"))
  .finally(() => console.log("Finally"));
```
- **Options**:  
  1. `Resolved`, `Finally`  
  2. `Caught`, `Finally`  
  3. `Error occurred`  
  4. `Finally`

- **Answer**: **2. Caught, Finally**

---

#### **Detailed Explanation**:

1. **Promise Rejection**:
   - The promise is rejected with `"Error occurred"`.

2. **`.catch`**:
   - Handles the rejection, logging `"Caught"`.

3. **`.finally`**:
   - Executes after the promise settles (either resolved or rejected), logging `"Finally"`.

---

#### **Q7: Predict the output of this `Object.entries` code.**
**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
const entries = Object.entries(obj);
console.log(entries);
```
- **Options**:  
  1. `[["a", 1], ["b", 2], ["c", 3]]`  
  2. `["a", 1, "b", 2, "c", 3]`  
  3. `[["a", "b", "c"], [1, 2, 3]]`  
  4. `Error`

- **Answer**: **1. [["a", 1], ["b", 2], ["c", 3]]**

---

#### **Detailed Explanation**:

1. **`Object.entries`**:
   - Converts an object into an array of key-value pairs.

2. **Execution**:
   - The keys (`a`, `b`, `c`) are paired with their corresponding values (`1`, `2`, `3`), forming an array of arrays.

---

Let’s proceed with **Week 8 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 8 Practice Questions**

---

#### **Q1: Write a function to handle errors in a promise-based API call.**
- **Input Example**:  
  ```javascript
  function unreliableAPI() {
    return new Promise((resolve, reject) => {
      Math.random() > 0.5 ? resolve("Success") : reject("Failure");
    });
  }

  handleAPI(unreliableAPI)
    .then(console.log)
    .catch(console.error);
  ```
- **Expected Output**:  
  - Logs `"Success"` if resolved or `"Failure"` if rejected.

---

#### **Solution**:

```javascript
async function handleAPI(apiFunc) {
  try {
    const result = await apiFunc();
    return result;
  } catch (error) {
    throw error;
  }
}

// Example
function unreliableAPI() {
  return new Promise((resolve, reject) => {
    Math.random() > 0.5 ? resolve("Success") : reject("Failure");
  });
}

handleAPI(unreliableAPI)
  .then(console.log) // Logs "Success"
  .catch(console.error); // Logs "Failure"
```

---

#### **Explanation**:
1. **Async/Await with Try-Catch**:
   - The `try` block handles successful resolutions.
   - The `catch` block handles rejections.

2. **Execution**:
   - Resolves with `"Success"` if `Math.random() > 0.5`.
   - Rejects with `"Failure"` otherwise.

---

#### **Q2: Write a function to merge two arrays of objects based on a common key.**
- **Input Example**:  
  ```javascript
  const array1 = [{ id: 1, name: "Alice" }, { id: 2, name: "Bob" }];
  const array2 = [{ id: 1, age: 25 }, { id: 2, age: 30 }];

  console.log(mergeArrays(array1, array2));
  ```
- **Expected Output**:  
  ```javascript
  [
    { id: 1, name: "Alice", age: 25 },
    { id: 2, name: "Bob", age: 30 },
  ];
  ```

---

#### **Solution**:

```javascript
function mergeArrays(arr1, arr2) {
  const map = new Map();
  arr1.forEach((item) => map.set(item.id, { ...item }));
  arr2.forEach((item) => {
    if (map.has(item.id)) {
      Object.assign(map.get(item.id), item);
    }
  });
  return Array.from(map.values());
}

// Example
const array1 = [{ id: 1, name: "Alice" }, { id: 2, name: "Bob" }];
const array2 = [{ id: 1, age: 25 }, { id: 2, age: 30 }];

console.log(mergeArrays(array1, array2));
```

---

#### **Explanation**:
1. **Using a `Map`**:
   - The `id` is used as the key for merging.
   - Combines objects with the same `id`.

2. **Execution**:
   - Merges objects from `array1` and `array2` based on their `id`.

---

#### **Q3: Write a function to debounce an API call.**
- **Input Example**:  
  ```javascript
  function fetchData() {
    console.log("API called");
  }

  const debouncedFetch = debounce(fetchData, 1000);
  debouncedFetch();
  debouncedFetch();
  debouncedFetch(); // Only this call executes
  ```
- **Expected Output**:  
  - Logs `"API called"` only once after 1 second.

---

#### **Solution**:

```javascript
function debounce(func, delay) {
  let timer;
  return function (...args) {
    clearTimeout(timer);
    timer = setTimeout(() => func(...args), delay);
  };
}

// Example
function fetchData() {
  console.log("API called");
}

const debouncedFetch = debounce(fetchData, 1000);
debouncedFetch();
debouncedFetch();
debouncedFetch(); // Only this call executes
```

---

#### **Explanation**:
1. **Debouncing**:
   - Ensures the function is executed only after the specified delay since the last invocation.

2. **Execution**:
   - Resets the timer on each call, so only the final call executes.

---

#### **Q4: Write a function to throttle an API call.**
- **Input Example**:  
  ```javascript
  function fetchData() {
    console.log("API called");
  }

  const throttledFetch = throttle(fetchData, 1000);
  throttledFetch();
  throttledFetch();
  throttledFetch(); // Only the first call executes
  ```
- **Expected Output**:  
  - Logs `"API called"` only once per second.

---

#### **Solution**:

```javascript
function throttle(func, delay) {
  let isThrottled = false;
  return function (...args) {
    if (!isThrottled) {
      func(...args);
      isThrottled = true;
      setTimeout(() => (isThrottled = false), delay);
    }
  };
}

// Example
function fetchData() {
  console.log("API called");
}

const throttledFetch = throttle(fetchData, 1000);
throttledFetch();
throttledFetch();
throttledFetch(); // Only the first call executes
```

---

#### **Explanation**:
1. **Throttling**:
   - Ensures the function is executed at most once per specified interval (`delay`).

2. **Execution**:
   - Blocks subsequent calls within the interval.

---

#### **Q5: Write a function to check if a string is a valid palindrome, ignoring case and non-alphanumeric characters.**
- **Input Example**:  
  ```javascript
  console.log(isPalindrome("A man, a plan, a canal, Panama")); // Output: true
  console.log(isPalindrome("Hello, World!")); // Output: false
  ```
- **Expected Output**:  
  - `true`  
  - `false`

---

#### **Solution**:

```javascript
function isPalindrome(str) {
  const sanitized = str.toLowerCase().replace(/[^a-z0-9]/g, "");
  return sanitized === sanitized.split("").reverse().join("");
}

// Example
console.log(isPalindrome("A man, a plan, a canal, Panama")); // Output: true
console.log(isPalindrome("Hello, World!")); // Output: false
```

---

#### **Explanation**:
1. **Sanitization**:
   - Converts the string to lowercase and removes non-alphanumeric characters using a regular expression.

2. **Comparison**:
   - Compares the sanitized string with its reversed version.

---

#### **Q6: Write a function to calculate the factorial of a number using recursion.**
- **Input Example**:  
  ```javascript
  console.log(factorial(5)); // Output: 120
  ```
- **Expected Output**: `120`

---

#### **Solution**:

```javascript
function factorial(n) {
  if (n === 0 || n === 1) return 1;
  return n * factorial(n - 1);
}

// Example
console.log(factorial(5)); // Output: 120
```

---

#### **Explanation**:
1. **Recursive Logic**:
   - Base case: `factorial(0)` and `factorial(1)` return `1`.
   - Recursive case: Multiplies `n` by `factorial(n - 1)`.

2. **Execution**:
   - Computes `5 * 4 * 3 * 2 * 1 = 120`.

---
Let’s continue with **Week 9 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 9 Graded Questions**

---

#### **Q1: What will be the output of the following code involving asynchronous behavior?**

**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside Timeout");
}, 0);

Promise.resolve("Resolved").then((value) => {
  console.log(value);
});

console.log("End");
```

- **Options**:  
  1. `Start`, `End`, `Resolved`, `Inside Timeout`  
  2. `Start`, `Resolved`, `End`, `Inside Timeout`  
  3. `Start`, `End`, `Inside Timeout`, `Resolved`  
  4. `Start`, `Resolved`, `Inside Timeout`, `End`

- **Answer**: **1. Start, End, Resolved, Inside Timeout**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - JavaScript runs synchronously first, logging `"Start"` and `"End"`.
   - The `Promise.resolve` is added to the **microtask queue** and runs after the synchronous code completes, logging `"Resolved"`.
   - The `setTimeout` callback with a 0ms delay is added to the **macrotask queue** and executes after all the microtasks, logging `"Inside Timeout"`.

---

#### **Q2: Predict the output of this code using `async`/`await`.**

**Code**:
```javascript
async function fetchData() {
  console.log("Fetching Data...");
  return "Data Fetched";
}

fetchData()
  .then((result) => console.log(result));
```

- **Options**:  
  1. `Fetching Data...`, `Data Fetched`  
  2. `Data Fetched`  
  3. `Fetching Data...`  
  4. `Error`

- **Answer**: **1. Fetching Data..., Data Fetched**

---

#### **Detailed Explanation**:

1. **`async` Function**:
   - The `async` function `fetchData` logs `"Fetching Data..."` and then returns a resolved promise with the value `"Data Fetched"`.

2. **Promise Handling**:
   - The promise is handled with `.then()`, which logs `"Data Fetched"` once the promise resolves.

---

#### **Q3: What will be the output of this code?**

**Code**:
```javascript
const myPromise = new Promise((resolve, reject) => {
  reject("Error occurred");
});

myPromise
  .then((data) => {
    console.log("Resolved:", data);
  })
  .catch((error) => {
    console.log("Caught:", error);
  });
```

- **Options**:  
  1. `Resolved: Error occurred`  
  2. `Caught: Error occurred`  
  3. `Error`  
  4. No output

- **Answer**: **2. Caught: Error occurred**

---

#### **Detailed Explanation**:

1. **Promise Rejection**:
   - The promise is immediately rejected with `"Error occurred"`.
   
2. **`.catch()`**:
   - The `.catch()` block handles the rejection and logs `"Caught: Error occurred"`.

---

#### **Q4: What will be logged in this code using `setInterval`?**

**Code**:
```javascript
let count = 0;
const interval = setInterval(() => {
  console.log(count);
  count++;
  if (count === 3) clearInterval(interval);
}, 1000);
```

- **Options**:  
  1. `0`, `1`, `2`  
  2. `0`, `1`, `2`, `3`  
  3. `0`, `1`  
  4. `0`, `1`, `2`, `3`, `4`

- **Answer**: **1. 0, 1, 2**

---

#### **Detailed Explanation**:

1. **`setInterval`**:
   - Executes the callback every 1000ms (1 second).

2. **`clearInterval`**:
   - Stops the interval after `count` reaches `3`, so only `0`, `1`, and `2` are logged.

---

#### **Q5: What will be the output of the following code?**

**Code**:
```javascript
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Data fetched"), 2000);
  });
}

async function getData() {
  const result = await fetchData();
  console.log(result);
}

getData();
```

- **Options**:  
  1. `Data fetched`  
  2. `undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Data fetched**

---

#### **Detailed Explanation**:

1. **`async/await`**:
   - The `await` keyword waits for the promise returned by `fetchData` to resolve, which occurs after 2 seconds.

2. **Execution**:
   - The resolved value `"Data fetched"` is logged after 2 seconds.

---

#### **Q6: What will be the output of this code involving `Promise.all`?**

**Code**:
```javascript
const promise1 = new Promise((resolve) => setTimeout(() => resolve("Resolved 1"), 1000));
const promise2 = new Promise((resolve) => setTimeout(() => resolve("Resolved 2"), 2000));
const promise3 = new Promise((resolve) => setTimeout(() => resolve("Resolved 3"), 1500));

Promise.all([promise1, promise2, promise3]).then((results) => {
  console.log(results);
});
```

- **Options**:  
  1. `["Resolved 1", "Resolved 2", "Resolved 3"]`  
  2. `["Resolved 1", "Resolved 3", "Resolved 2"]`  
  3. `["Resolved 1", "Resolved 2"]`  
  4. `Error`

- **Answer**: **1. ["Resolved 1", "Resolved 2", "Resolved 3"]**

---

#### **Detailed Explanation**:

1. **`Promise.all`**:
   - Waits for all promises to resolve and returns an array with the resolved values in the order they were passed.

2. **Execution**:
   - The promises resolve in their respective times, but the results are logged in the order they were provided in the array.

---

#### **Q7: What will this code log?**

**Code**:
```javascript
const arr = [1, 2, 3];
arr.push(4);
console.log(arr);
```

- **Options**:  
  1. `[1, 2, 3]`  
  2. `[1, 2, 3, 4]`  
  3. `undefined`  
  4. `Error`

- **Answer**: **2. [1, 2, 3, 4]**

---

#### **Detailed Explanation**:

1. **Array Modification**:
   - The `push` method adds `4` to the end of the array.

2. **Execution**:
   - Logs `[1, 2, 3, 4]`.

---

#### **Q8: What will this code output?**

**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
delete obj.b;
console.log(obj);
```

- **Options**:  
  1. `{ a: 1, b: 2, c: 3 }`  
  2. `{ a: 1, c: 3 }`  
  3. `{ b: 2, c: 3 }`  
  4. `Error`

- **Answer**: **2. { a: 1, c: 3 }**

---

#### **Detailed Explanation**:

1. **`delete` Operator**:
   - The `delete` operator removes the specified property from the object.

2. **Execution**:
   - Removes the `b` property, leaving `{ a: 1, c: 3 }`.

---
Let’s continue with **Week 9 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 9 Graded Questions**

---

#### **Q1: What will be the output of the following code involving asynchronous behavior?**

**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside Timeout");
}, 0);

Promise.resolve("Resolved").then((value) => {
  console.log(value);
});

console.log("End");
```

- **Options**:  
  1. `Start`, `End`, `Resolved`, `Inside Timeout`  
  2. `Start`, `Resolved`, `End`, `Inside Timeout`  
  3. `Start`, `End`, `Inside Timeout`, `Resolved`  
  4. `Start`, `Resolved`, `Inside Timeout`, `End`

- **Answer**: **1. Start, End, Resolved, Inside Timeout**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - JavaScript runs synchronously first, logging `"Start"` and `"End"`.
   - The `Promise.resolve` is added to the **microtask queue** and runs after the synchronous code completes, logging `"Resolved"`.
   - The `setTimeout` callback with a 0ms delay is added to the **macrotask queue** and executes after all the microtasks, logging `"Inside Timeout"`.

---

#### **Q2: Predict the output of this code using `async`/`await`.**

**Code**:
```javascript
async function fetchData() {
  console.log("Fetching Data...");
  return "Data Fetched";
}

fetchData()
  .then((result) => console.log(result));
```

- **Options**:  
  1. `Fetching Data...`, `Data Fetched`  
  2. `Data Fetched`  
  3. `Fetching Data...`  
  4. `Error`

- **Answer**: **1. Fetching Data..., Data Fetched**

---

#### **Detailed Explanation**:

1. **`async` Function**:
   - The `async` function `fetchData` logs `"Fetching Data..."` and then returns a resolved promise with the value `"Data Fetched"`.

2. **Promise Handling**:
   - The promise is handled with `.then()`, which logs `"Data Fetched"` once the promise resolves.

---

#### **Q3: What will be the output of this code?**

**Code**:
```javascript
const myPromise = new Promise((resolve, reject) => {
  reject("Error occurred");
});

myPromise
  .then((data) => {
    console.log("Resolved:", data);
  })
  .catch((error) => {
    console.log("Caught:", error);
  });
```

- **Options**:  
  1. `Resolved: Error occurred`  
  2. `Caught: Error occurred`  
  3. `Error`  
  4. No output

- **Answer**: **2. Caught: Error occurred**

---

#### **Detailed Explanation**:

1. **Promise Rejection**:
   - The promise is immediately rejected with `"Error occurred"`.
   
2. **`.catch()`**:
   - The `.catch()` block handles the rejection and logs `"Caught: Error occurred"`.

---

#### **Q4: What will be logged in this code using `setInterval`?**

**Code**:
```javascript
let count = 0;
const interval = setInterval(() => {
  console.log(count);
  count++;
  if (count === 3) clearInterval(interval);
}, 1000);
```

- **Options**:  
  1. `0`, `1`, `2`  
  2. `0`, `1`, `2`, `3`  
  3. `0`, `1`  
  4. `0`, `1`, `2`, `3`, `4`

- **Answer**: **1. 0, 1, 2**

---

#### **Detailed Explanation**:

1. **`setInterval`**:
   - Executes the callback every 1000ms (1 second).

2. **`clearInterval`**:
   - Stops the interval after `count` reaches `3`, so only `0`, `1`, and `2` are logged.

---

#### **Q5: What will be the output of the following code?**

**Code**:
```javascript
function fetchData() {
  return new Promise((resolve) => {
    setTimeout(() => resolve("Data fetched"), 2000);
  });
}

async function getData() {
  const result = await fetchData();
  console.log(result);
}

getData();
```

- **Options**:  
  1. `Data fetched`  
  2. `undefined`  
  3. `Error`  
  4. No output

- **Answer**: **1. Data fetched**

---

#### **Detailed Explanation**:

1. **`async/await`**:
   - The `await` keyword waits for the promise returned by `fetchData` to resolve, which occurs after 2 seconds.

2. **Execution**:
   - The resolved value `"Data fetched"` is logged after 2 seconds.

---

#### **Q6: What will be the output of this code involving `Promise.all`?**

**Code**:
```javascript
const promise1 = new Promise((resolve) => setTimeout(() => resolve("Resolved 1"), 1000));
const promise2 = new Promise((resolve) => setTimeout(() => resolve("Resolved 2"), 2000));
const promise3 = new Promise((resolve) => setTimeout(() => resolve("Resolved 3"), 1500));

Promise.all([promise1, promise2, promise3]).then((results) => {
  console.log(results);
});
```

- **Options**:  
  1. `["Resolved 1", "Resolved 2", "Resolved 3"]`  
  2. `["Resolved 1", "Resolved 3", "Resolved 2"]`  
  3. `["Resolved 1", "Resolved 2"]`  
  4. `Error`

- **Answer**: **1. ["Resolved 1", "Resolved 2", "Resolved 3"]**

---

#### **Detailed Explanation**:

1. **`Promise.all`**:
   - Waits for all promises to resolve and returns an array with the resolved values in the order they were passed.

2. **Execution**:
   - The promises resolve in their respective times, but the results are logged in the order they were provided in the array.

---

#### **Q7: What will this code log?**

**Code**:
```javascript
const arr = [1, 2, 3];
arr.push(4);
console.log(arr);
```

- **Options**:  
  1. `[1, 2, 3]`  
  2. `[1, 2, 3, 4]`  
  3. `undefined`  
  4. `Error`

- **Answer**: **2. [1, 2, 3, 4]**

---

#### **Detailed Explanation**:

1. **Array Modification**:
   - The `push` method adds `4` to the end of the array.

2. **Execution**:
   - Logs `[1, 2, 3, 4]`.

---

#### **Q8: What will this code output?**

**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
delete obj.b;
console.log(obj);
```

- **Options**:  
  1. `{ a: 1, b: 2, c: 3 }`  
  2. `{ a: 1, c: 3 }`  
  3. `{ b: 2, c: 3 }`  
  4. `Error`

- **Answer**: **2. { a: 1, c: 3 }**

---

#### **Detailed Explanation**:

1. **`delete` Operator**:
   - The `delete` operator removes the specified property from the object.

2. **Execution**:
   - Removes the `b` property, leaving `{ a: 1, c: 3 }`.

---

Let’s continue with **Week 10 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 10 Graded Questions**

---

#### **Q1: What will the following code output?**
**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Timeout 1");
}, 0);

Promise.resolve("Resolved 1").then((value) => {
  console.log(value);
});

setTimeout(() => {
  console.log("Timeout 2");
}, 0);

Promise.resolve("Resolved 2").then((value) => {
  console.log(value);
});

console.log("End");
```

- **Options**:  
  1. `Start`, `End`, `Resolved 1`, `Resolved 2`, `Timeout 1`, `Timeout 2`  
  2. `Start`, `End`, `Timeout 1`, `Timeout 2`, `Resolved 1`, `Resolved 2`  
  3. `Start`, `Resolved 1`, `Resolved 2`, `End`, `Timeout 1`, `Timeout 2`  
  4. `Start`, `Timeout 1`, `Timeout 2`, `Resolved 1`, `Resolved 2`, `End`

- **Answer**: **1. Start, End, Resolved 1, Resolved 2, Timeout 1, Timeout 2**

---

#### **Detailed Explanation**:

1. **Synchronous Execution**:
   - `"Start"` and `"End"` are logged immediately because they are synchronous.

2. **Promises**:
   - The promise handlers are added to the **microtask queue** and are executed after the synchronous code but before the `setTimeout` callbacks.

3. **`setTimeout`**:
   - The `setTimeout` callbacks are added to the **macrotask queue** and execute after the microtasks.

4. **Execution Order**:
   - `"Start"` is logged.
   - `"End"` is logged.
   - `"Resolved 1"` and `"Resolved 2"` are logged (promise resolution happens before the `setTimeout`).
   - `"Timeout 1"` and `"Timeout 2"` are logged.

---

#### **Q2: What will this code output?**
**Code**:
```javascript
function foo() {
  console.log("foo");
}

function bar() {
  console.log("bar");
  foo();
}

bar();
```

- **Options**:  
  1. `foo`, `bar`  
  2. `bar`, `foo`  
  3. `foo`  
  4. `bar`, `foo`, `bar`

- **Answer**: **2. bar, foo**

---

#### **Detailed Explanation**:

1. **Execution Flow**:
   - The `bar()` function is called first, which logs `"bar"`.
   - Inside `bar()`, the `foo()` function is called, which logs `"foo"`.

2. **Execution Order**:
   - `"bar"` is logged first from `bar()`.
   - `"foo"` is logged next from `foo()` called inside `bar()`.

---

#### **Q3: What will the following code output?**
**Code**:
```javascript
const obj = { a: 1, b: 2 };

Object.freeze(obj);
obj.a = 3;
console.log(obj.a);
```

- **Options**:  
  1. `3`  
  2. `1`  
  3. `undefined`  
  4. `Error`

- **Answer**: **2. 1**

---

#### **Detailed Explanation**:

1. **`Object.freeze()`**:
   - The `Object.freeze()` method prevents the modification of an object's properties.

2. **Execution**:
   - After calling `Object.freeze()`, trying to modify `obj.a` has no effect, and it remains `1`.

---

#### **Q4: What will the following code output?**
**Code**:
```javascript
const arr = [1, 2, 3];
const arr2 = arr;

arr2.push(4);
console.log(arr);
```

- **Options**:  
  1. `[1, 2, 3, 4]`  
  2. `[1, 2, 3]`  
  3. `[4]`  
  4. `Error`

- **Answer**: **1. [1, 2, 3, 4]**

---

#### **Detailed Explanation**:

1. **Array Assignment**:
   - The assignment `const arr2 = arr` doesn't create a new array but rather makes `arr2` reference the same array as `arr`.

2. **Modification**:
   - Modifying `arr2` (via `push`) also affects `arr` since both variables refer to the same array in memory.

3. **Execution**:
   - After `arr2.push(4)`, both `arr` and `arr2` contain `[1, 2, 3, 4]`.

---

#### **Q5: What will the following code output?**
**Code**:
```javascript
const arr = [1, 2, 3];
arr.length = 2;
console.log(arr);
```

- **Options**:  
  1. `[1, 2]`  
  2. `[1, 2, 3]`  
  3. `[]`  
  4. `Error`

- **Answer**: **1. [1, 2]**

---

#### **Detailed Explanation**:

1. **Modifying `length`**:
   - Changing the `length` property of an array truncates the array to the specified length.

2. **Execution**:
   - Setting `arr.length = 2` removes the last element of the array, so it becomes `[1, 2]`.

---

#### **Q6: What will this code output?**
**Code**:
```javascript
console.log(1 + "1");
console.log("1" - 1);
console.log("1" * 1);
console.log(1 / "1");
```

- **Options**:  
  1. `"11"`, `0`, `1`, `1`  
  2. `"11"`, `NaN`, `1`, `1`  
  3. `NaN`, `NaN`, `NaN`, `NaN`  
  4. `"11"`, `NaN`, `"1"`, `1`

- **Answer**: **1. "11", 0, 1, 1**

---

#### **Detailed Explanation**:

1. **String Concatenation** (`1 + "1"`):
   - JavaScript converts the number `1` to a string and concatenates, resulting in `"11"`.

2. **Subtraction** (`"1" - 1`):
   - JavaScript converts the string `"1"` to a number and performs subtraction, resulting in `0`.

3. **Multiplication** (`"1" * 1`):
   - JavaScript converts the string `"1"` to a number and performs multiplication, resulting in `1`.

4. **Division** (`1 / "1"`):
   - JavaScript converts the string `"1"` to a number and performs division, resulting in `1`.

---

#### **Q7: What will this code output?**
**Code**:
```javascript
console.log(2 + 2 + "2");
console.log("2" + 2 + 2);
```

- **Options**:  
  1. `"22"`, `"222"`  
  2. `"22"`, `222`  
  3. `"22"`, `"222"`  
  4. `NaN`, `"222"`

- **Answer**: **1. "22", "222"**

---

#### **Detailed Explanation**:

1. **Expression Evaluation**:
   - In the first example, `2 + 2` is evaluated first to give `4`, and then the string `"2"` is concatenated, resulting in `"22"`.
   - In the second example, `"2"` is a string, so the first `+` operation concatenates, and the result `"22"` is followed by another `+ 2`, resulting in `"222"`.

---

#### **Q8: What will this code output?**
**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
const { a, ...rest } = obj;
console.log(a);
console.log(rest);
```

- **Options**:  
  1. `1`, `{ b: 2, c: 3 }`  
  2. `1`, `{ a: 1, b: 2, c: 3 }`  
  3. `{ a: 1 }`, `{ b: 2, c: 3 }`  
  4. `undefined`, `{ b: 2, c: 3 }`

- **Answer**: **1. 1, { b: 2, c: 3 }**

---

#### **Detailed Explanation**:

1. **Object Destructuring**:
   - The object is destructured with `a` being extracted and `rest` gathering the remaining properties.

2. **Execution**:
   - Logs `1` for `a` and `{ b: 2, c: 3 }` for the `rest` object.

---
Let’s continue with **Week 11 Graded Questions**, providing detailed solutions and explanations.

---

### **Week 11 Graded Questions**

---

#### **Q1: What will be the output of the following code using `setTimeout`?**
**Code**:
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside Timeout");
}, 0);

console.log("End");
```
- **Options**:  
  1. `Start`, `End`, `Inside Timeout`  
  2. `Start`, `Inside Timeout`, `End`  
  3. `Inside Timeout`, `Start`, `End`  
  4. `Start`, `End`

- **Answer**: **1. Start, End, Inside Timeout**

---

#### **Detailed Explanation**:

1. **Synchronous Code**:
   - `"Start"` and `"End"` are logged first because they are synchronous and executed immediately.

2. **`setTimeout`**:
   - The callback in `setTimeout` is scheduled to run after 0 milliseconds, but it still has to wait for the synchronous code to finish first. It will be added to the **macrotask queue**.

3. **Execution Order**:
   - After `"Start"` and `"End"` are logged, the callback from `setTimeout` executes, logging `"Inside Timeout"`.

---

#### **Q2: What will be the output of the following code using `Promise`?**
**Code**:
```javascript
console.log("Start");

Promise.resolve("Resolved").then((value) => {
  console.log(value);
});

console.log("End");
```
- **Options**:  
  1. `Start`, `End`, `Resolved`  
  2. `Start`, `Resolved`, `End`  
  3. `Resolved`, `Start`, `End`  
  4. `Start`, `End`

- **Answer**: **1. Start, End, Resolved**

---

#### **Detailed Explanation**:

1. **Synchronous Code**:
   - `"Start"` and `"End"` are logged immediately because they are synchronous.

2. **`Promise.resolve()`**:
   - The promise is resolved immediately, but the `.then()` handler is added to the **microtask queue**, which gets executed after the synchronous code finishes.

3. **Execution Order**:
   - `"Start"` and `"End"` are logged first.
   - The promise is resolved and `"Resolved"` is logged last, after the synchronous code.

---

#### **Q3: What will be the output of the following code involving `async/await`?**
**Code**:
```javascript
async function fetchData() {
  console.log("Fetching Data...");
  return "Data Fetched";
}

fetchData().then((result) => console.log(result));
```
- **Options**:  
  1. `Fetching Data...`, `Data Fetched`  
  2. `Data Fetched`  
  3. `Fetching Data...`  
  4. `Error`

- **Answer**: **1. Fetching Data..., Data Fetched**

---

#### **Detailed Explanation**:

1. **`async/await`**:
   - The `async` function `fetchData` logs `"Fetching Data..."` immediately and then returns a resolved promise with `"Data Fetched"`.
   - The `.then()` method handles the resolved promise and logs `"Data Fetched"`.

2. **Execution Order**:
   - `"Fetching Data..."` is logged first.
   - `"Data Fetched"` is logged after the promise resolves.

---

#### **Q4: What will be the output of the following code using `Object.assign`?**
**Code**:
```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };

const mergedObj = Object.assign({}, obj1, obj2);
console.log(mergedObj);
```
- **Options**:  
  1. `{ a: 1, b: 3, c: 4 }`  
  2. `{ a: 1, b: 2, c: 4 }`  
  3. `{ b: 3, c: 4 }`  
  4. `{ a: 1, b: 2, c: 4 }`

- **Answer**: **1. { a: 1, b: 3, c: 4 }**

---

#### **Detailed Explanation**:

1. **`Object.assign()`**:
   - The `Object.assign()` method copies the properties from one or more source objects to a target object. If properties overlap, the values from later objects will overwrite earlier ones.

2. **Execution**:
   - `obj1` and `obj2` are merged into a new object. The value of `b` from `obj2` overwrites the value of `b` from `obj1`, resulting in `{ a: 1, b: 3, c: 4 }`.

---

#### **Q5: What will be the output of the following code?**
**Code**:
```javascript
const arr = [1, 2, 3];
arr.length = 2;
console.log(arr);
```
- **Options**:  
  1. `[1, 2]`  
  2. `[1, 2, 3]`  
  3. `[]`  
  4. `Error`

- **Answer**: **1. [1, 2]**

---

#### **Detailed Explanation**:

1. **Changing `length`**:
   - The `length` property of an array controls the number of elements in the array. Setting the `length` property to `2` removes elements beyond the second index.

2. **Execution**:
   - The array becomes `[1, 2]` after truncating the last element.

---

#### **Q6: What will be the output of this code involving `this`?**
**Code**:
```javascript
const person = {
  name: "John",
  greet: function() {
    console.log("Hello, " + this.name);
  }
};

person.greet();
```
- **Options**:  
  1. `Hello, John`  
  2. `Hello, undefined`  
  3. `Error`  
  4. `No output`

- **Answer**: **1. Hello, John**

---

#### **Detailed Explanation**:

1. **`this` Context**:
   - In the method `greet()`, `this` refers to the `person` object. Therefore, `this.name` accesses the `name` property of `person`.

2. **Execution**:
   - Logs `"Hello, John"` because `this.name` is `"John"`.

---

#### **Q7: What will the following code output?**
**Code**:
```javascript
const arr = [1, 2, 3];
const arr2 = arr;
arr2[0] = 5;
console.log(arr);
```
- **Options**:  
  1. `[5, 2, 3]`  
  2. `[1, 2, 3]`  
  3. `[5]`  
  4. `Error`

- **Answer**: **1. [5, 2, 3]**

---

#### **Detailed Explanation**:

1. **Array Reference**:
   - In JavaScript, arrays are objects, and when you assign one array to another (`arr2 = arr`), both variables point to the same array in memory.
   - Modifying `arr2` also modifies `arr` because they reference the same array.

2. **Execution**:
   - The modification `arr2[0] = 5` changes the first element of both `arr` and `arr2`, resulting in `[5, 2, 3]`.

---

#### **Q8: What will be the output of the following code?**
**Code**:
```javascript
const obj = { a: 1, b: 2, c: 3 };
const { a, ...rest } = obj;
console.log(a);
console.log(rest);
```
- **Options**:  
  1. `1`, `{ b: 2, c: 3 }`  
  2. `1`, `{ a: 1, b: 2, c: 3 }`  
  3. `{ a: 1 }`, `{ b: 2, c: 3 }`  
  4. `undefined`, `{ b: 2, c: 3 }`

- **Answer**: **1. 1, { b: 2, c: 3 }**

---

#### **Detailed Explanation**:

1. **Object Destructuring**:
   - The `{ a, ...rest } = obj` syntax extracts the `a` property and gathers the remaining properties into `rest`.

2. **Execution**:
   - Logs `1` for `a` and `{ b: 2, c: 3 }` for `rest`.

---

Let's proceed with **Week 11 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 11 Practice Questions**

---

#### **Q1: Write a function to find the intersection of two arrays.**
- **Input Example**:  
  ```javascript
  const array1 = [1, 2, 3, 4];
  const array2 = [3, 4, 5, 6];
  console.log(findIntersection(array1, array2)); // Output: [3, 4]
  ```
- **Expected Output**:  
  - `[3, 4]`

---

#### **Solution**:

```javascript
function findIntersection(arr1, arr2) {
  return arr1.filter(value => arr2.includes(value));
}

// Example
const array1 = [1, 2, 3, 4];
const array2 = [3, 4, 5, 6];
console.log(findIntersection(array1, array2)); // Output: [3, 4]
```

---

#### **Explanation**:
1. **Using `filter` and `includes`**:
   - The `filter` method iterates through `arr1` and checks if each element is also present in `arr2` using `includes`.
   
2. **Execution**:
   - Returns an array of common elements, `[3, 4]`.

---

#### **Q2: Write a function to find the union of two arrays (all elements without duplicates).**
- **Input Example**:  
  ```javascript
  const array1 = [1, 2, 3];
  const array2 = [3, 4, 5];
  console.log(findUnion(array1, array2)); // Output: [1, 2, 3, 4, 5]
  ```
- **Expected Output**:  
  - `[1, 2, 3, 4, 5]`

---

#### **Solution**:

```javascript
function findUnion(arr1, arr2) {
  return [...new Set([...arr1, ...arr2])];
}

// Example
const array1 = [1, 2, 3];
const array2 = [3, 4, 5];
console.log(findUnion(array1, array2)); // Output: [1, 2, 3, 4, 5]
```

---

#### **Explanation**:
1. **Using `Set`**:
   - `Set` removes duplicates, so combining `arr1` and `arr2` into a set gives the union without duplicates.

2. **Execution**:
   - The arrays `[1, 2, 3]` and `[3, 4, 5]` are merged and duplicates are removed, resulting in `[1, 2, 3, 4, 5]`.

---

#### **Q3: Write a function to get the keys of an object that have `null` values.**
- **Input Example**:  
  ```javascript
  const obj = { a: 1, b: null, c: 3, d: null };
  console.log(getNullKeys(obj)); // Output: ['b', 'd']
  ```
- **Expected Output**:  
  - `['b', 'd']`

---

#### **Solution**:

```javascript
function getNullKeys(obj) {
  return Object.keys(obj).filter(key => obj[key] === null);
}

// Example
const obj = { a: 1, b: null, c: 3, d: null };
console.log(getNullKeys(obj)); // Output: ['b', 'd']
```

---

#### **Explanation**:
1. **Using `Object.keys` and `filter`**:
   - `Object.keys()` gets all keys of the object.
   - `filter` is used to select the keys where the corresponding value is `null`.

2. **Execution**:
   - Returns the keys `['b', 'd']` because they have `null` values.

---

#### **Q4: Write a function to find the longest word in a string.**
- **Input Example**:  
  ```javascript
  const sentence = "The quick brown fox jumped over the lazy dog";
  console.log(findLongestWord(sentence)); // Output: "jumped"
  ```
- **Expected Output**:  
  - `"jumped"`

---

#### **Solution**:

```javascript
function findLongestWord(sentence) {
  const words = sentence.split(" ");
  return words.reduce((longest, current) => current.length > longest.length ? current : longest, "");
}

// Example
const sentence = "The quick brown fox jumped over the lazy dog";
console.log(findLongestWord(sentence)); // Output: "jumped"
```

---

#### **Explanation**:
1. **Using `split` and `reduce`**:
   - `split(" ")` splits the sentence into words.
   - `reduce` compares the lengths of the words and keeps the longest one.

2. **Execution**:
   - The longest word `"jumped"` is returned.

---

#### **Q5: Write a function to check if an object has a specific property.**
- **Input Example**:  
  ```javascript
  const obj = { a: 1, b: 2, c: 3 };
  console.log(hasProperty(obj, 'b')); // Output: true
  console.log(hasProperty(obj, 'd')); // Output: false
  ```
- **Expected Output**:  
  - `true` or `false` based on the existence of the property.

---

#### **Solution**:

```javascript
function hasProperty(obj, prop) {
  return obj.hasOwnProperty(prop);
}

// Example
const obj = { a: 1, b: 2, c: 3 };
console.log(hasProperty(obj, 'b')); // Output: true
console.log(hasProperty(obj, 'd')); // Output: false
```

---

#### **Explanation**:
1. **Using `hasOwnProperty`**:
   - The `hasOwnProperty` method checks if the object has the given property as its own (not inherited).

2. **Execution**:
   - Returns `true` for `b` and `false` for `d`.

---

#### **Q6: Write a function to count how many times a character appears in a string.**
- **Input Example**:  
  ```javascript
  const str = "hello world";
  console.log(countCharacter(str, 'o')); // Output: 2
  ```
- **Expected Output**:  
  - `2`

---

#### **Solution**:

```javascript
function countCharacter(str, char) {
  return str.split(char).length - 1;
}

// Example
const str = "hello world";
console.log(countCharacter(str, 'o')); // Output: 2
```

---

#### **Explanation**:
1. **String Split**:
   - The `split(char)` method splits the string by the specified character and returns an array.
   - The length of the resulting array minus 1 gives the count of occurrences of the character.

2. **Execution**:
   - The character `'o'` appears twice in the string `"hello world"`.

---

#### **Q7: Write a function to convert a string to an array of words.**
- **Input Example**:  
  ```javascript
  const sentence = "Hello world from JavaScript";
  console.log(convertToArray(sentence)); // Output: ["Hello", "world", "from", "JavaScript"]
  ```
- **Expected Output**:  
  - `["Hello", "world", "from", "JavaScript"]`

---

#### **Solution**:

```javascript
function convertToArray(str) {
  return str.split(" ");
}

// Example
const sentence = "Hello world from JavaScript";
console.log(convertToArray(sentence)); // Output: ["Hello", "world", "from", "JavaScript"]
```

---

#### **Explanation**:
1. **Using `split(" ")`**:
   - The `split(" ")` method splits the string into an array of words based on spaces.

2. **Execution**:
   - The sentence `"Hello world from JavaScript"` is converted into an array of words.

---

#### **Q8: Write a function to find the second largest number in an array.**
- **Input Example**:  
  ```javascript
  const numbers = [10, 20, 30, 40, 50];
  console.log(secondLargest(numbers)); // Output: 40
  ```
- **Expected Output**:  
  - `40`

---

#### **Solution**:

```javascript
function secondLargest(arr) {
  const sorted = [...arr].sort((a, b) => b - a);
  return sorted[1];
}

// Example
const numbers = [10, 20, 30, 40, 50];
console.log(secondLargest(numbers)); // Output: 40
```

---

#### **Explanation**:
1. **Sorting in Descending Order**:
   - The array is sorted in descending order using `sort((a, b) => b - a)`.

2. **Execution**:
   - The second largest number is the second element in the sorted array.

---

This concludes **Week 11 Practice Questions**. Let me know if you'd like further clarification on any topics or if you want to continue with more questions!
---
Let's proceed with **Week 11 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 11 Practice Questions**

---

#### **Q1: Write a function to find the intersection of two arrays.**
- **Input Example**:  
  ```javascript
  const array1 = [1, 2, 3, 4];
  const array2 = [3, 4, 5, 6];
  console.log(findIntersection(array1, array2)); // Output: [3, 4]
  ```
- **Expected Output**:  
  - `[3, 4]`

---

#### **Solution**:

```javascript
function findIntersection(arr1, arr2) {
  return arr1.filter(value => arr2.includes(value));
}

// Example
const array1 = [1, 2, 3, 4];
const array2 = [3, 4, 5, 6];
console.log(findIntersection(array1, array2)); // Output: [3, 4]
```

---

#### **Explanation**:
1. **Using `filter` and `includes`**:
   - The `filter` method iterates through `arr1` and checks if each element is also present in `arr2` using `includes`.
   
2. **Execution**:
   - Returns an array of common elements, `[3, 4]`.

---

#### **Q2: Write a function to find the union of two arrays (all elements without duplicates).**
- **Input Example**:  
  ```javascript
  const array1 = [1, 2, 3];
  const array2 = [3, 4, 5];
  console.log(findUnion(array1, array2)); // Output: [1, 2, 3, 4, 5]
  ```
- **Expected Output**:  
  - `[1, 2, 3, 4, 5]`

---

#### **Solution**:

```javascript
function findUnion(arr1, arr2) {
  return [...new Set([...arr1, ...arr2])];
}

// Example
const array1 = [1, 2, 3];
const array2 = [3, 4, 5];
console.log(findUnion(array1, array2)); // Output: [1, 2, 3, 4, 5]
```

---

#### **Explanation**:
1. **Using `Set`**:
   - `Set` removes duplicates, so combining `arr1` and `arr2` into a set gives the union without duplicates.

2. **Execution**:
   - The arrays `[1, 2, 3]` and `[3, 4, 5]` are merged and duplicates are removed, resulting in `[1, 2, 3, 4, 5]`.

---

#### **Q3: Write a function to get the keys of an object that have `null` values.**
- **Input Example**:  
  ```javascript
  const obj = { a: 1, b: null, c: 3, d: null };
  console.log(getNullKeys(obj)); // Output: ['b', 'd']
  ```
- **Expected Output**:  
  - `['b', 'd']`

---

#### **Solution**:

```javascript
function getNullKeys(obj) {
  return Object.keys(obj).filter(key => obj[key] === null);
}

// Example
const obj = { a: 1, b: null, c: 3, d: null };
console.log(getNullKeys(obj)); // Output: ['b', 'd']
```

---

#### **Explanation**:
1. **Using `Object.keys` and `filter`**:
   - `Object.keys()` gets all keys of the object.
   - `filter` is used to select the keys where the corresponding value is `null`.

2. **Execution**:
   - Returns the keys `['b', 'd']` because they have `null` values.

---

#### **Q4: Write a function to find the longest word in a string.**
- **Input Example**:  
  ```javascript
  const sentence = "The quick brown fox jumped over the lazy dog";
  console.log(findLongestWord(sentence)); // Output: "jumped"
  ```
- **Expected Output**:  
  - `"jumped"`

---

#### **Solution**:

```javascript
function findLongestWord(sentence) {
  const words = sentence.split(" ");
  return words.reduce((longest, current) => current.length > longest.length ? current : longest, "");
}

// Example
const sentence = "The quick brown fox jumped over the lazy dog";
console.log(findLongestWord(sentence)); // Output: "jumped"
```

---

#### **Explanation**:
1. **Using `split` and `reduce`**:
   - `split(" ")` splits the sentence into words.
   - `reduce` compares the lengths of the words and keeps the longest one.

2. **Execution**:
   - The longest word `"jumped"` is returned.

---

#### **Q5: Write a function to check if an object has a specific property.**
- **Input Example**:  
  ```javascript
  const obj = { a: 1, b: 2, c: 3 };
  console.log(hasProperty(obj, 'b')); // Output: true
  console.log(hasProperty(obj, 'd')); // Output: false
  ```
- **Expected Output**:  
  - `true` or `false` based on the existence of the property.

---

#### **Solution**:

```javascript
function hasProperty(obj, prop) {
  return obj.hasOwnProperty(prop);
}

// Example
const obj = { a: 1, b: 2, c: 3 };
console.log(hasProperty(obj, 'b')); // Output: true
console.log(hasProperty(obj, 'd')); // Output: false
```

---

#### **Explanation**:
1. **Using `hasOwnProperty`**:
   - The `hasOwnProperty` method checks if the object has the given property as its own (not inherited).

2. **Execution**:
   - Returns `true` for `b` and `false` for `d`.

---

#### **Q6: Write a function to count how many times a character appears in a string.**
- **Input Example**:  
  ```javascript
  const str = "hello world";
  console.log(countCharacter(str, 'o')); // Output: 2
  ```
- **Expected Output**:  
  - `2`

---

#### **Solution**:

```javascript
function countCharacter(str, char) {
  return str.split(char).length - 1;
}

// Example
const str = "hello world";
console.log(countCharacter(str, 'o')); // Output: 2
```

---

#### **Explanation**:
1. **String Split**:
   - The `split(char)` method splits the string by the specified character and returns an array.
   - The length of the resulting array minus 1 gives the count of occurrences of the character.

2. **Execution**:
   - The character `'o'` appears twice in the string `"hello world"`.

---

#### **Q7: Write a function to convert a string to an array of words.**
- **Input Example**:  
  ```javascript
  const sentence = "Hello world from JavaScript";
  console.log(convertToArray(sentence)); // Output: ["Hello", "world", "from", "JavaScript"]
  ```
- **Expected Output**:  
  - `["Hello", "world", "from", "JavaScript"]`

---

#### **Solution**:

```javascript
function convertToArray(str) {
  return str.split(" ");
}

// Example
const sentence = "Hello world from JavaScript";
console.log(convertToArray(sentence)); // Output: ["Hello", "world", "from", "JavaScript"]
```

---

#### **Explanation**:
1. **Using `split(" ")`**:
   - The `split(" ")` method splits the string into an array of words based on spaces.

2. **Execution**:
   - The sentence `"Hello world from JavaScript"` is converted into an array of words.

---

#### **Q8: Write a function to find the second largest number in an array.**
- **Input Example**:  
  ```javascript
  const numbers = [10, 20, 30, 40, 50];
  console.log(secondLargest(numbers)); // Output: 40
  ```
- **Expected Output**:  
  - `40`

---

#### **Solution**:

```javascript
function secondLargest(arr) {
  const sorted = [...arr].sort((a, b) => b - a);
  return sorted[1];
}

// Example
const numbers = [10, 20, 30, 40, 50];
console.log(secondLargest(numbers)); // Output: 40
```

---

#### **Explanation**:
1. **Sorting in Descending Order**:
   - The array is sorted in descending order using `sort((a, b) => b - a)`.

2. **Execution**:
   - The second largest number is the second element in the sorted array.

---

This concludes **Week 11 Practice Questions**. Let me know if you'd like further clarification on any topics or if you want to continue with more questions!

Let's proceed with **Week 12 Practice Questions**, providing detailed solutions and explanations.

---

### **Week 12 Practice Questions**

---

#### **Q1: Write a function to find the sum of all even numbers in an array.**
- **Input Example**:  
  ```javascript
  const numbers = [1, 2, 3, 4, 5, 6];
  console.log(sumEvenNumbers(numbers)); // Output: 12
  ```
- **Expected Output**:  
  - `12`

---

#### **Solution**:

```javascript
function sumEvenNumbers(arr) {
  return arr.filter(num => num % 2 === 0).reduce((sum, num) => sum + num, 0);
}

// Example
const numbers = [1, 2, 3, 4, 5, 6];
console.log(sumEvenNumbers(numbers)); // Output: 12
```

---

#### **Explanation**:
1. **Using `filter`**:
   - The `filter` method selects all even numbers by checking if the number modulo `2` is `0`.

2. **Using `reduce`**:
   - After filtering the even numbers, `reduce` is used to accumulate their sum.

3. **Execution**:
   - The even numbers `[2, 4, 6]` are filtered and then summed to give `12`.

---

#### **Q2: Write a function to merge two sorted arrays into a single sorted array.**
- **Input Example**:  
  ```javascript
  const arr1 = [1, 3, 5];
  const arr2 = [2, 4, 6];
  console.log(mergeSortedArrays(arr1, arr2)); // Output: [1, 2, 3, 4, 5, 6]
  ```
- **Expected Output**:  
  - `[1, 2, 3, 4, 5, 6]`

---

#### **Solution**:

```javascript
function mergeSortedArrays(arr1, arr2) {
  return [...arr1, ...arr2].sort((a, b) => a - b);
}

// Example
const arr1 = [1, 3, 5];
const arr2 = [2, 4, 6];
console.log(mergeSortedArrays(arr1, arr2)); // Output: [1, 2, 3, 4, 5, 6]
```

---

#### **Explanation**:
1. **Array Spread and `sort`**:
   - The two arrays are combined using the spread operator (`...`) and then sorted using the `sort()` method.

2. **Execution**:
   - The combined array `[1, 3, 5, 2, 4, 6]` is sorted to `[1, 2, 3, 4, 5, 6]`.

---

#### **Q3: Write a function to remove all falsy values from an array.**
- **Input Example**:  
  ```javascript
  const array = [0, 1, false, 2, "", 3, NaN, 4];
  console.log(removeFalsyValues(array)); // Output: [1, 2, 3, 4]
  ```
- **Expected Output**:  
  - `[1, 2, 3, 4]`

---

#### **Solution**:

```javascript
function removeFalsyValues(arr) {
  return arr.filter(Boolean);
}

// Example
const array = [0, 1, false, 2, "", 3, NaN, 4];
console.log(removeFalsyValues(array)); // Output: [1, 2, 3, 4]
```

---

#### **Explanation**:
1. **Using `filter(Boolean)`**:
   - `filter(Boolean)` removes all falsy values from the array. Falsy values include `false`, `0`, `""`, `NaN`, `null`, and `undefined`.

2. **Execution**:
   - The array `[1, 2, 3, 4]` is returned after filtering out the falsy values.

---

#### **Q4: Write a function to check if a string is a palindrome (case insensitive).**
- **Input Example**:  
  ```javascript
  const str = "A man, a plan, a canal, Panama";
  console.log(isPalindrome(str)); // Output: true
  ```
- **Expected Output**:  
  - `true` if the string is a palindrome.

---

#### **Solution**:

```javascript
function isPalindrome(str) {
  const sanitizedStr = str.toLowerCase().replace(/[^a-z0-9]/g, "");
  return sanitizedStr === sanitizedStr.split("").reverse().join("");
}

// Example
const str = "A man, a plan, a canal, Panama";
console.log(isPalindrome(str)); // Output: true
```

---

#### **Explanation**:
1. **Sanitizing the String**:
   - The string is converted to lowercase, and all non-alphanumeric characters are removed using `replace(/[^a-z0-9]/g, "")`.

2. **Reversing the String**:
   - After sanitizing the string, it is compared to its reverse to check if it is a palindrome.

3. **Execution**:
   - `"A man, a plan, a canal, Panama"` is a palindrome, so the function returns `true`.

---

#### **Q5: Write a function to find the common elements between two arrays.**
- **Input Example**:  
  ```javascript
  const array1 = [1, 2, 3, 4];
  const array2 = [3, 4, 5, 6];
  console.log(findCommonElements(array1, array2)); // Output: [3, 4]
  ```
- **Expected Output**:  
  - `[3, 4]`

---

#### **Solution**:

```javascript
function findCommonElements(arr1, arr2) {
  return arr1.filter(item => arr2.includes(item));
}

// Example
const array1 = [1, 2, 3, 4];
const array2 = [3, 4, 5, 6];
console.log(findCommonElements(array1, array2)); // Output: [3, 4]
```

---

#### **Explanation**:
1. **Using `filter` and `includes`**:
   - `filter` is used to iterate over `arr1`, and `includes` checks if the current element is also in `arr2`.

2. **Execution**:
   - The common elements between `[1, 2, 3, 4]` and `[3, 4, 5, 6]` are `[3, 4]`.

---

#### **Q6: Write a function to find the largest number in an array.**
- **Input Example**:  
  ```javascript
  const numbers = [10, 20, 30, 40, 50];
  console.log(findLargestNumber(numbers)); // Output: 50
  ```
- **Expected Output**:  
  - `50`

---

#### **Solution**:

```javascript
function findLargestNumber(arr) {
  return Math.max(...arr);
}

// Example
const numbers = [10, 20, 30, 40, 50];
console.log(findLargestNumber(numbers)); // Output: 50
```

---

#### **Explanation**:
1. **Using `Math.max`**:
   - `Math.max(...arr)` finds the largest number in the array by spreading the array elements into the `Math.max` function.

2. **Execution**:
   - The largest number in `[10, 20, 30, 40, 50]` is `50`.

---

#### **Q7: Write a function to check if two strings are anagrams of each other.**
- **Input Example**:  
  ```javascript
  const str1 = "listen";
  const str2 = "silent";
  console.log(areAnagrams(str1, str2)); // Output: true
  ```
- **Expected Output**:  
  - `true` if the strings are anagrams.

---

#### **Solution**:

```javascript
function areAnagrams(str1, str2) {
  const sortedStr1 = str1.toLowerCase().split("").sort().join("");
  const sortedStr2 = str2.toLowerCase().split("").sort().join("");
  return sortedStr1 === sortedStr2;
}

// Example
const str1 = "listen";
const str2 = "silent";
console.log(areAnagrams(str1, str2)); // Output: true
```

---

#### **Explanation**:
1. **Sorting and Comparing**:
   - Both strings are converted to lowercase, split into characters, sorted, and joined back into strings.
   - If the sorted versions of both strings are equal, they are anagrams.

2. **Execution**:
   - `"listen"` and `"silent"` are anagrams, so the function returns `true`.

---

#### **Q8: Write a function to find the second smallest number in an array.**
- **Input Example**:  
  ```javascript
  const numbers = [10, 20, 30, 40, 50];
  console.log(secondSmallest(numbers)); // Output: 20
  ```
- **Expected Output**:  
  - `20`

---

#### **Solution**:

```javascript
function secondSmallest(arr) {
  const sortedArr = [...arr].sort((a, b) => a - b);
  return sortedArr[1];
}

// Example
const numbers = [10, 20, 30, 40, 50];
console.log(secondSmallest(numbers)); // Output: 20
```

---

#### **Explanation**:
1. **Sorting**:
   - The array is sorted in ascending order using the `sort((a, b) => a - b)` method.

2. **Execution**:
   - The second smallest number is at index `1` in the sorted array.

---

This concludes **Week 12 Practice Questions**. Let me know if you'd like to continue with more questions, focus on specific concepts, or explore other topics!
