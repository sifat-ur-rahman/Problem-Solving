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

console.log(getMaleNames(people)); // Output: ["Bob", "Charlie"]
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

console.log(getBookTitles(books)); // Output: ["Book One", "Book Two", "Book Three"]
```

