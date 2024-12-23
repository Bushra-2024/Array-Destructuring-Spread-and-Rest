# Array-Destructuring-Spread-and-Rest
Here’s a short and understandable explanation of Array, Destructuring, Spread, and Rest in JavaScript with examples to help you understand these concepts


<img src="https://miro.medium.com/v2/resize:fit:800/1*VQrahe38Lj6vM807CYC3vA.png">

**Arrays** in JavaScript are special objects that store multiple values as a collection of elements. These values can be of any type, including primitives (like numbers and strings) and objects (like arrays or other objects).


## Change elements in array.
You can add or modify array elements using their index. If you assign a value to a non-existing index, gaps will be filled with undefined.
```js
let arr = [1, 2];  
arr[3] = 4; // Adds a value at index 3  
console.log(arr); // [1, 2, undefined, 4]
```

## Array Methods
**Array methods in JavaScript are built-in functions that allow you to perform various operations on arrays, such as adding or removing elements, searching, sorting, or modifying the array in different ways. These methods provide easy ways to work with arrays without needing to manually iterate or modify them.**




### 1. `push( )`

Adds one or more elements to the end of an array.

Changes Parent: Yes, it changes the original array.

Example:

```js
let arr = [1, 2];
arr.push(3); // Adds 3 at the end
console.log(arr); // [1, 2, 3]
```




### 2. `pop( )`

Removes the last element from an array.

Changes Parent: Yes, it changes the original array.

Example:

```js
let arr = [1, 2, 3];
arr.pop(); // Removes 3
console.log(arr); // [1, 2]
```




### 3. `shift( )`
   
Removes the first element from an array.

Changes Parent: Yes, it changes the original array.

Example:

```js
let arr = [1, 2, 3];
arr.shift(); // Removes 1
console.log(arr); // [2, 3]
```




### 4. `unshift( )`

Adds one or more elements to the beginning of an array.

Changes Parent: Yes, it changes the original array.

Example:

```js
let arr = [2, 3];
arr.unshift(1); // Adds 1 at the start
console.log(arr); // [1, 2, 3]
```




### 5. `concat( )`

Combines two or more arrays or values into a new array.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr1 = [1, 2];
let arr2 = [3, 4];
let combined = arr1.concat(arr2); // Creates a new array
console.log(combined); // [1, 2, 3, 4]
console.log(arr1); // [1, 2] (original array is unchanged)
```




### 6. `slice( )`

Creates a shallow copy of a portion of an array into a new array.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
let sliced = arr.slice(1, 3); // Extracts elements from index 1 to 2
console.log(sliced); // [2, 3]
console.log(arr); // [1, 2, 3] (original array is unchanged)
```




### 7. `join( )`

Joins all elements of an array into a string.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
let joined = arr.join('-'); // Joins array elements with '-'
console.log(joined); // "1-2-3"
console.log(arr); // [1, 2, 3] (original array is unchanged)
```




### 8. `includes( )`

Checks if an array contains a certain element.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
console.log(arr.includes(2)); // true
console.log(arr.includes(4)); // false
```




### 9. `indexOf( )`

Returns the first index of a specified element in an array.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
console.log(arr.indexOf(2)); // 1
console.log(arr.indexOf(4)); // -1
```




### 10. `splice( )`
    
Description: Changes the contents of an array by removing or replacing elements.

Changes Parent: Yes, it changes the original array.

Example:

```js
let arr = [1, 2, 3];
arr.splice(1, 1, 4, 5); // Removes 2 and adds 4 and 5
console.log(arr); // [1, 4, 5, 3]
```




### 11. `toString( )`
    
Converts the array to a string, where elements are separated by commas.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
let str = arr.toString(); // Converts array to string
console.log(str); // "1,2,3"
console.log(arr); // [1, 2, 3] (original array is unchanged)
```




### 12. `toReversed( )`
    
Description: Returns a new array with elements in reverse order.

Changes Parent: No, it does not change the original array.

Example:

```js
let arr = [1, 2, 3];
let reversed = arr.toReversed(); // Creates a reversed array
console.log(reversed); // [3, 2, 1]
console.log(arr); // [1, 2, 3] (original array is unchanged)
```


# Destructuring

Destructuring in JavaScript is a shorthand syntax for extracting values from arrays or objects and assigning them to variables. It makes it easier to work with complex data structures.


**Array Destructuring**
Array destructuring allows you to unpack values from an array into individual variables.

Syntax:
```js
let [variable1, variable2] = array;
```


```js
Example:
const arr = [1, 2, 3];
const [a, b] = arr;
console.log(a); // 1
console.log(b); // 2
```


```js
You can also skip values using commas:
const arr = [1, 2, 3];
const [, , c] = arr;
console.log(c); // 3
```

```js
You can use default values too:
const arr = [1];
const [a, b = 2] = arr;
console.log(b); // 2 (default value)
```


# Spread Operator (...)

Is used to expand or spread elements from an iterable (such as an array, string, or object) into individual elements.

<img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*caR9nuGK5SypQRXvU9ubUA.png">
<img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*HKKrk4DZv7SzV_twfyPAmg.png">
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*BSWE0w4F9oB0XptO_wz1Og.png">
<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*G_AOqX1El5LlBX_bDFMy5g.png">


# Rest Parameter (...)
The rest parameter collects all remaining arguments into an array. It's typically used in function definitions to handle an arbitrary number of arguments.

```js
function sum(...theArgs) {
  let total = 0;
  for (let i = 0; i < theArgs.length; i++) {
    total += theArgs[i];  
  }
  return total;  
}
console.log(sum(1, 2, 3));  // Output: 6
console.log(sum(1, 2, 3, 4));  // Output: 10

```
