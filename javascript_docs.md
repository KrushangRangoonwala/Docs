# JavaScript Arrays
```javascript
const points = [40, 100, 1, 5, 25, 10, "Saab", "Volvo", "BMW"];
```

### Converting an Array to a String
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();  // Banana,Orange,Apple,Mango

document.getElementById("demo").innerHTML = fruits;  // Banana,Orange,Apple,Mango
```

```javascript
console.log(typeof fruits);  // obeject
```
### Difference Between Arrays and Objects
In JavaScript, arrays use numbered indexes.  
In JavaScript, objects use named indexes.
For accessing elements in array we use _numbers_ while in object we use _name_ (string) .

#### How to Recognize an Array
```javascript
console.log(Array.isArray(fruits));  // true
console.log(fruits instanceof Array);  // true
```
## Array Methods
<details>
<summary>Array length</summary>
  
```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let size = fruits.length;
```
</details>

<details><summary>Array toString()</summary>

```JavaScript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
console.log(courses.toString()); //HTML,CSS,JavaScript,React
```
</details>
<details><summary>Array at()</summary>

```JavaScript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
console.log(fruits.at(2));  // Apple
console.log(fruits[2]);  // Apple
```
</details>
<details><summary>Array join()</summary>

```JavaScript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
console.log(courses.join('|')); //HTML|CSS|JavaScript|React
```
</details>



<details><summary>Array pop()</summary>
removes the last element from an array:
  
```JavaScript
let numArr = [20, 30, 40, 50];
let popped = numArr.pop(); // remove last item
console.log(popped); // 5x0
```
</details>

<details><summary>Array push()</summary>
adds a new element to an array (at the end):

```JavaScript
let numArr = [20, 30, 40, 50];
numArr.push(60); //[20, 30, 40, 50, 60]
numArr.push(70, 80, 90); //[20, 30, 40, 50, 60 ,70,80,90]
```
</details>

<details><summary>Array shift()</summary>
removes the first array element and "shifts" all other elements to a lower index.
  
```JavaScript
let numArr = [20, 30, 40, 50];
let shift = numArr.shift(); // remove item from start 
console.log(shift);  // 20 
console.log(numArr);  // 30, 40, 50
```
</details>


<details><summary>Array unshift()</summary>
adds a new element to an array (at the beginning), and "unshifts" older elements:
  
```JavaScript
let numArr = [20, 30, 40, 50];
numArr.unshift(10, 20);  // 10, 20, 20, 30, 40, 50
```
</details>

<details><summary>Array delete()</summary>
delete() leaves undefined holes in the array.
  
```JavaScript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[1];
consoloe.log(fruits);  // Banana,,Apple,Mango
```
</details>

<details><summary>Array concat()</summary>

```JavaScript
let arr1 = [11, 12, 13];
let arr2 = [14, 15, 16];
let arr3 = [17, 18, 19];

let newArr = arr1.concat(arr2, arr3);
console.log(newArr); //[11, 12, 13, 14, 15,16, 17, 18, 19]
```
</details>

<details><summary>Array copyWithin()</summary>
copyWithin  : overwrites the existing values. -> does not add items to the array. -> does not change the length of the array.
arr.copywithin(position, start_index, end_index)
  
```JavaScript
let fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.copyWithin(2, 0);  //Banana,Orange,Banana,Orange

 fruits = ["Banana", "Orange", "Apple", "Mango", "Kiwi", "Papaya"];
fruits.copyWithin(2, 0, 2);  // Banana,Orange,Banana,Orange,Kiwi,Papaya

```
</details>

<details><summary>Array flat()</summary>
creates a __new array__ with sub-array elements concatenated to a specified depth:
  
```JavaScript
myArr = [[1,2],[3,4],[5,6]];
console.log( myArr.flat());  // 1,2,3,4,5,6
```
</details>

<details><summary>Array flatMap() : method first maps all elements of an array and then creates a __new array__ by flattening the array</summary>
creates a __new array__ with sub-array elements concatenated to a specified depth:
  
```JavaScript
const myArr = [1, 2, 3, 4, 5, 6];
const newArr = myArr.flatMap(x => [x, x * 10]);
console.log(newArr);  // 1,10,2,20,3,30,4,40,5,50,6,60

```
</details>

<details><summary>Array splice() : </summary>
used to 
  +add new items 
  +remove items
return removed items
  
```JavaScript
arr.splice(position, count_of_want_to_remove_element, new_elements, new_elements, ...);
fruits = ["Banana", "Orange", "Apple", "Mango"];
let removed = fruits.splice(2, 2, "Lemon", "Kiwi"); 
console.log(fruits);  //Banana,Orange,Lemon,Kiwi
console.log(removed);  //Apple,Mango
```
</details>

<details><summary>Array toSpliced() : Don't update original array, return new array</summary>

```JavaScript
let spliced = months.toSpliced(1, 2,"Mar", "Apr");
console.log(months);  //(remain unchanged) "Jan", "Feb", "Mar", "Apr"  
console.log(spliced);  //Jan,Mar,Apr,Apr
```
</details>

<details><summary>Array slice() : remove items </summary>

```JavaScript
arr.slice(start-index , end-index);  
fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
console.log(fruits.slice(1)); // Orange,Lemon,Apple,Mango
console.log(fruits.slice(1,3)); // "Orange", "Lemon"
```
</details>

