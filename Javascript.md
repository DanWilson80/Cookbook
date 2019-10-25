Javascript Information
======  
  
Index
[8_Useful_Array_Functions](#8_Useful_Array_Functions)
  
  
  
8_Useful_Array_Functions
------
**.filter()**
```
const words = ["spray", "limit", "elite", "exuberant", "destruction", "present", "happy"];

let longWords = words.filter(word => word.length > 6);
// this would filter out any words <= 6 letters
  
  
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
const filteredItems = items.filter(item => {
  return item.price <= 100
  });
  console.log(filteredItems)
  //returns all items <100
```

**.map()**
```
var numbers = [1, 4, 9];

var roots = numbers.map(Math.sqrt); //sqrt = square root
// roots is now [1, 2, 3] which is a new array
// numbers is still [1, 4, 9] the old array stays the same we never want to midify our original array
  
  
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }

const itemNames = items.map(item => {
  return item.name
 }); // returns a list of all names from the array
 
const itemPrices = items.map(item => {
  return item.price
 }); // returns a list of all prices from the array
```
  
**.reduce()**
```
const numbers = [0, 1, 2, 3, 4];

const total = numbers.reduce((currentTotal, number) => {
    return currentTotal;
  }, 0) // this value is the starting value
console.log(total) // will ouput 10 (0+1+2+3+4)
  
  
const myArray = [34, 24, 124, 24];

const answer = myArray.reduce((currentTotal, number) => currentTotal + number);
console.log(answer) // will output 206

const answer = myArray.reduce((currentTotal, number) => {
    currentTotal + number
    }, 100);
console.log(answer) // will output 306
  
  
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }

const total = items.reduce((currentTotal, item) => {
    return item.price + currentTotal
  }, 0)
console.log(total) // will return 1840
```
  
**.forEach**
```
const items = ["item1", "item2", "item3"]

const copy = [] // an empty array
items.forEach((item) => {
    copy.push(item) // pushes each item into the new array
  });
  
  
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
items.forEach((item) => {
    console.log(item.name)
  }); // will loop over every item in the array and return the name from each one and print it to the console
```
  
**.some()**
```
const numbers = [12, 5, 8, 1, 14];

const overTen = numbers.some((number) => {
    return number > 10
  });
console.log(overTen) // will return true. This is a boolean and if one answer is true then the function returns true.

const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
const inexpensiveItems = items.some((item) => {
    return item.price <= 100
  });
console.log(inexpensiveItems) // would return true as there is at least one item under 100.
```
  
**.every()**
```
.every() works exactly like .some() except it returns true if every value meets the criteria.
```
  
**.find()**
```
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
const foundItem = items.find((item) => {
    return item.name === "book"
  });
console.log(foundItem) // prints item containing book
```
  
**.includes()**
```
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
const includesTwo = items.includes(7)
  console.log(includesTwo); // this method takes an argument and loks for it in the array and returns a boolean. In this case it will return false.  
```
  
**.findIndex()**
```
const items{
    {name: "bike", price: 100}
    {name: "tv", price: 200}
    {name: "album", price: 10}
    {name: "book", price: 5}
    {name: "phone", price: 500}
    {name: "computer", price: 1000}
    {name: "keyboard", price: 25}
  }
  
const findId = items.findIndex((item) => {
    return item.name === "book"
   });
console.log(findId) // will return the Id of the book item

items.splice(findId, 1) // removes that Id from the items array

OR we can create a new array and preserve the old one (best practice)

const newItems = [
  ...items.slice(0, findId),
  ...items.slice(findId, +1)
  ]; // this slices either side of the array and joins it back together without the itemId
```
  
**Object.values(), Object.keys(), Object.entries**
```
var myEntry = {0: "a", 1: "b", 2: "c", 3: "d", 4: "e", 5: "f"}

console.log(Object.keys(myEntry)); // will log the keys ["0", "1", "2", "3", "4", "5"]

console.log(Object.values(myEntry)); // will log the values ["a", "b", "c", "d", "e", "f"]

console.log(Object.entries(myEntry)); // will log the entries [["0","a"]["1","b"]["2","c"]["3","d"]["4","e"]["5","f"]]
```
  

