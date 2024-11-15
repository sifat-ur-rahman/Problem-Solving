# JavaScript Problem Solving 

## 1. Array Filtering And Mapping

Create an array of objects, each representing a person with properties like name, age, and gender. Write a function to filter out all females and then map the remaining people to an array of names. Print the final result.

```javascript
const people = [
  { name: "Alice", age: 25, gender: "female" },
  { name: "Bob", age: 30, gender: "male" },
  { name: "Charlie", age: 35, gender: "male" },
  { name: "Diana", age: 28, gender: "female" }
];

const getMaleNames = (arr) => {
  return arr.filter(person => person.gender === 'male').map(person => person.name);
};

console.log(getMaleNames(people));

```
## 2. Object Manipulation
Create an array of objects representing books with properties like title, author, and year. Write a function that takes the array and returns a new array with only the book titles. Print the result.

```javascript

const books = [
  { title: "Book One", author: "Author One", year: 2001 },
  { title: "Book Two", author: "Author Two", year: 2002 },
  { title: "Book Three", author: "Author Three", year: 2003 }
];

const getBookTitles = (arr) => {
  return arr.map(book => book.title);
};

console.log(getBookTitles(books));

```
## 3. Function Composition
Write three functions: one to square a number, one to double a number, and one to add 5 to a number. Compose these functions to create a new function that squares a number, doubles the result, and then adds 5.

```javascript

const square = (num) => num * num;
const double = (num) => num * 2;
const addFive = (num) => num + 5;

const composedFunction = (num) => addFive(double(square(num)));

console.log(composedFunction(2));

```
## 4. Sorting Objects
Create an array of objects representing cars with properties like make, model, and year. Write a function to sort the array of cars by the year of manufacture in ascending order. Print the sorted array.

```javascript

const cars = [
  { make: "Toyota", model: "Camry", year: 2019 },
  { make: "Honda", model: "Accord", year: 2018 },
  { make: "Tesla", model: "Model 3", year: 2020 }
];

const sortCarsByYear = (arr) => {
  return arr.sort((a, b) => a.year - b.year);
};

console.log(sortCarsByYear(cars));

```
## 5. Find And Modify
Write a function that searches an array of objects for a specific person by name. If found, modify their age property. Print the updated array.

```javascript

const people = [
  { name: "Alice", age: 25 },
  { name: "Bob", age: 30 },
  { name: "Charlie", age: 35 }
];

const updatePersonAge = (arr, personName, newAge) => {
  const person = arr.find(person => person.name === personName);
  if (person) {
    person.age = newAge;
  }
  return arr;
};

console.log(updatePersonAge(people, "Bob", 31));


```
## 6. Array Reduction
Create an array of numbers. Write a function that uses the reduce method to calculate the sum of all even numbers in the array.

```javascript

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const sumEvenNumbers = (arr) => {
  return arr.reduce((sum, num) => {
    return num % 2 === 0 ? sum + num : sum;
  }, 0);
};

console.log(sumEvenNumbers(numbers)); 
```
## 7. Leap Year Checker
Write a function that determines whether a given year is a leap year.

```javascript

const isLeapYear = (year) => {
  return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0);
};

console.log(isLeapYear(2020)); 
console.log(isLeapYear(2021)); 
```
## 8. Unique Values
Create an array of numbers with some duplicate values. Write a function to filter out the duplicate values and return a new array with only unique numbers. Print the result.

```javascript

const numbers = [1, 2, 3, 4, 3, 2, 1, 5, 6, 5];

const getUniqueValues = (arr) => {
  return [...new Set(arr)];
};

console.log(getUniqueValues(numbers)); 
```
## 9. Find Maximum Value
Write a function that takes an array of numbers and returns the maximum value.

```javascript

const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

const findMaxValue = (arr) => {
  return Math.max(...arr);
};

console.log(findMaxValue(numbers)); 
```
## 10. Advanced Sorting
Create an array of objects representing students with 'name' and 'grades' properties. Write a function to sort the students by average grade in descending order.

```javascript

const students = [
  { name: "Alice", grades: [90, 85, 88] },
  { name: "Bob", grades: [78, 82, 80] },
  { name: "Charlie", grades: [95, 92, 93] }
];

const getAverageGrade = (grades) => {
  return grades.reduce((sum, grade) => sum + grade, 0) / grades.length;
};

const sortStudentsByAverageGrade = (arr) => {
  return arr.sort((a, b) => getAverageGrade(b.grades) - getAverageGrade(a.grades));
};

console.log(sortStudentsByAverageGrade(students));

```
## 11. Functional Programming - Reduce
Write a function that uses the reduce function to calculate the total value of an array of objects with a 'quantity' and 'price' property.

```javascript

const items = [
  { quantity: 2, price: 10 },
  { quantity: 1, price: 20 },
  { quantity: 3, price: 15 }
];

const calculateTotalValue = (arr) => {
  return arr.reduce((total, item) => total + item.quantity * item.price, 0);
};

console.log(calculateTotalValue(items)); 
```
## 12. Reverse a string.

```javascript
function reverseString(str) {
    return str.split('').reverse().join('');
  }
  
console.log(reverseString('hello')); // Output: 'olleh'
```

## 13. Remove falsy values from array 

```javascript
let array = ['a',false,'b',NaN, 0, undefined, 'c',null,'','d']
//passing Boolean to array.filter() will remove falsy value from array
let newArray=array.filter(Boolean)
// console.log(newArray)
```
## 14. Convert any value to boolean(true or false)

```javascript
let value = 'hero'
// console.log(!!value)
```

## 15.Resizing any array 

```javascript
let letter = ['a','b','c','d','e']
letter.length = 3
// console.log(letter)
```
## 16. How to flatter a multi-dimensional array

```javascript
let num = [1, 2, [3, 4], 5, 6, [[7], 8]]
let newNum = num.flat(Infinity)
```
## 17. Short conditionals

```javascript
const captain = "Sakib";

//-------&&-------
//Instead of doing this
 if(captain === "Sakib"){
    console.log('ok')
 }
 //we can use &&
 captain === "Sakib" && console.log('ok')

 //-----||-------
 //Instead of doing this
 if(captain !== "Sakib"){
    console.log('Not ok')
 }
 //we can use &&
 captain !== "Sakib" && console.log('Not ok')
```


## 18. Replace all occurances of a string

```javascript
const quote = "React is a JS framework & this framework is the most popular front-end framework right now"

//Replace all occurances of 'framework' with 'library'.
const newQuote = quote.replace(/framework/g,"library")
// console.log(newQuote)
```


## 19. Know performance of a task 

```javascript
const startTime = performance.now()

for (let i = 0; i <= 50; i++) {
    // console.log(i)
    
}

const endTime = performance.now()

const time = `loop took ${endTime-startTime} milliseconds to finish`
// console.log(time)
```
## 20. Calculate the factorial of a number.

```javascript
function factorial(num) {
    if (num === 0 || num === 1) {
      return 1;
    }
    let result = 1;
    for (let i = 2; i <= num; i++) {
      result *= i;
    }
    return result;
  }
  
  console.log(factorial(5)); // Output: 120
```
## 22. Find the largest number in an array.
```javascript
function findLargestNumber(arr) {
    let largest = arr[0];
    for (let i = 1; i < arr.length; i++) {
      if (arr[i] > largest) {
        largest = arr[i];
      }
    }
    return largest;
  }
  
  const numbers = [4, 7, 2, 9, 1];
  console.log(findLargestNumber(numbers)); // Output: 9
  ```
## 23. Check if a given number is prime.
```javascript
function isPrime(num) {
    if (num <= 1) {
      return false;
    }
    for (let i = 2; i <= Math.sqrt(num); i++) {
      if (num % i === 0) {
        return false;
      }
    }
    return true;
  }
  
  console.log(isPrime(7)); // Output: true
  console.log(isPrime(12)); // Output: false
  ```

## 24. Remove duplicates from an array.
```javascript
function removeDuplicates(arr) {
    return Array.from(new Set(arr));
  }
  
const numbers = [1, 2, 2, 3, 4, 4, 5];
console.log(removeDuplicates(numbers)); 
  // Output: [1, 2, 3, 4, 5]
```

