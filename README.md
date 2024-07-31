## JS Coding Question and solution

### 1. Nested Array in Single Array

```js
const arr = [1, [2, 3], [4, [5, 6]]];
let flatArr = [];

// Recursive function to flatten an array
function flattenArray(inputArray) {
  for (let i = 0; i < inputArray.length; i++) {
    if (Array.isArray(inputArray[i])) {
      flattenArray(inputArray[i]);
    } else {
      flatArr.push(inputArray[i]);
    }
  }
}

// Flatten the original array
flattenArray(arr);

console.log(flatArr); // Output will be [1, 2, 3, 4, 5, 6]
```

### 2.Sum of the array

```js
const arr = [1, 2, 3, 4, 5];
let sum = 0;

// Use a for loop to iterate through the array and sum the elements
for (let i = 0; i < arr.length; i++) {
  sum += arr[i];
}

console.log(sum); // Output will be 15
```

### 3. unique element from the array

```js
const arr = [1, 2, 3, 3, 4, 5, 5];
let uniqueArr = [];

// Use a for loop to add unique elements to the new array
for (let i = 0; i < arr.length; i++) {
  if (!uniqueArr.includes(arr[i])) {
    uniqueArr.push(arr[i]);
  }
}

console.log(uniqueArr); // Output will be [1, 2, 3, 4, 5]
```

### 4. Unique item get from two array

```js
const arr1 = [1, 2, 3, 4];
const arr2 = [3, 4, 5, 6];

let newArr = [];

// Use a for loop to find common elements
for (let i = 0; i < arr1.length; i++) {
  for (let j = 0; j < arr2.length; j++) {
    if (arr1[i] === arr2[j]) {
      newArr.push(arr1[i]);
      break;
      // Once we find a match, we can break out of the inner loop
    }
  }
}

console.log(newArr); // Output will be [3, 4]
```

### 5. first two item swap

```js
const array = [3, 5, 1, 4, 2];

let swappedArray = [];

// Use a for loop to swap the first two elements
for (let i = 0; i < array.length; i++) {
  if (i === 0) {
    swappedArray[1] = array[i];
  } else if (i === 1) {
    swappedArray[0] = array[i];
  } else {
    swappedArray[i] = array[i];
  }
}

console.log(swappedArray); // Output will be [5, 3, 1, 4, 2]
```
