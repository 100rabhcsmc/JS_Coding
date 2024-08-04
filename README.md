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

### 6.Reverse Array

```js
const arr1 = [1, 2, 3, 4, 5];
let reversedArr1 = [];

// Use a for loop to reverse the array
for (let i = arr1.length - 1; i >= 0; i--) {
  reversedArr1.push(arr1[i]);
}

console.log(reversedArr1); // Output will be [5, 4, 3, 2, 1]
```

### 8. Reverse a String

```js
function reverseString(str) {
  return str.split("").reverse().join("");
}

console.log(reverseString("hello")); // Output: "olleh"
```

**Using the for loop**

```js
const Reverse = (str) => {
  var reverseStr = "";
  for (let i = str.length - 1; i >= 0; i--) {
    reverseStr = reverseStr + str[i];
  }
  return reverseStr;
};

console.log(Reverse("Hello")); // Output: "olleh"
```

### 7.Odd Number

```js
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];
let oddNumbers = [];

// Use a for loop to filter out odd numbers
for (let i = 0; i < numbers.length; i++) {
  if (numbers[i] % 2 !== 0) {
    oddNumbers.push(numbers[i]);
  }
}

console.log(oddNumbers); // Output will be [1, 3, 5, 7]
```

### 8. Check Palindrome

Palindrome means _same when read forward or backward_

```js
function isPalindrome(str) {
  const reversed = str.split("").reverse().join("");
  return str === reversed;
}

console.log(isPalindrome("racecar")); // Output: true
```

for loop

```js
const Reverse = (str) => {
  var reverseStr = "";
  for (let i = str.length - 1; i >= 0; i--) {
    reverseStr = reverseStr + str[i];
  }
  return str === reverseStr;
};

console.log(Reverse("racecar"));
```

### count of the char in string

input = 'aaabbc';
output = {a:3,b:2,c:1}

```js
const givenData = "aabbccc";

const charCount = (givenData) => {
  let newData = {};
  for (let i = 0; i < givenData.length; i++) {
    let char = givenData[i];
    if (newData[char]) {
      newData[char]++;
    } else {
      newData[char] = 1;
    }
  }
  return newData;
};

console.log(charCount(givenData));
```

same proble minor change **input = ["aaabbbcccc"];**

```js
const givenData = ["aabbccc"];

const charCount = (givenData) => {
  let newData = {};
  let str = givenData[0]; // Access the first element of the array
  for (let i = 0; i < str.length; i++) {
    let char = str[i];
    if (newData[char]) {
      newData[char]++;
    } else {
      newData[char] = 1;
    }
  }
  return newData;
};

console.log(charCount(givenData));
```
