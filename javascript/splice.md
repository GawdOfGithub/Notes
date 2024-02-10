## The splice method in JavaScript is used to change the contents of an array by removing or replacing existing elements and/or adding new elements. The signature of the splice method is as follows:
```javascript
array.splice(start, deleteCount, item1, item2, ...);
```
 * **start**: The index at which to start changing the array. If negative, it will begin that many elements from the end of the array. If greater than the length of the array, start will be set to the length of the array. If negative, it will be set to (length + start) where length is the length of the array.
   * **deleteCount**: An integer indicating the number of elements in the array to remove from start. If deleteCount is 0, no elements are removed. If deleteCount is greater than the number of elements left in the array starting at start, then all of the elements through the end of the array will be deleted.
   *  **item1, item2**, ...: The elements to add to the array, beginning from the start index. If you don't specify any elements, splice will only remove elements from the array.

   ## Really awesome example 

  ```javascript
  let fruits = ['apple', 'banana', 'cherry', 'date'];

// Case 1: Remove elements starting from index 1 (banana) with deleteCount 2
let removedElements = fruits.splice(1, 2);
console.log('Removed Elements:', removedElements);
// Output: Removed Elements: ['banana', 'cherry']
console.log('Modified Array:', fruits);

// Output:  Modified Array: ['apple', 'date']

// Case 2: Insert 'kiwi' and 'grape' starting from index 1, without removing any elements
fruits.splice(1, 0, 'kiwi', 'grape');
console.log('Modified Array:', fruits);
// Output: Modified Array: ['apple', 'kiwi', 'grape', 'date']

// Case 3: Replace 'kiwi' and 'grape' with 'orange', 'lemon', and 'lime' starting from index 1
fruits.splice(1, 2, 'orange', 'lemon', 'lime');
console.log('Modified Array:', fruits);
// Output: Modified Array: ['apple', 'orange', 'lemon', 'lime', 'date']
