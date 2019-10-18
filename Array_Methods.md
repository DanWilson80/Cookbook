Different Array Methods and How They Work
======

```
const inventors = [
      { first: 'Albert', last: 'Einstein', year: 1879, passed: 1955 },
      { first: 'Isaac', last: 'Newton', year: 1643, passed: 1727 },
      { first: 'Galileo', last: 'Galilei', year: 1564, passed: 1642 },
      { first: 'Marie', last: 'Curie', year: 1867, passed: 1934 },
      { first: 'Johannes', last: 'Kepler', year: 1571, passed: 1630 },
      { first: 'Nicolaus', last: 'Copernicus', year: 1473, passed: 1543 },
      { first: 'Max', last: 'Planck', year: 1858, passed: 1947 },
      { first: 'Katherine', last: 'Blodgett', year: 1898, passed: 1979 },
      { first: 'Ada', last: 'Lovelace', year: 1815, passed: 1852 },
      { first: 'Sarah E.', last: 'Goode', year: 1855, passed: 1905 },
      { first: 'Lise', last: 'Meitner', year: 1878, passed: 1968 },
      { first: 'Hanna', last: 'Hammarström', year: 1829, passed: 1909 }
    ];

const people = ['Beck, Glenn', 'Becker, Carl', 'Beckett, Samuel', 'Beddoes, Mick', 'Beecher, Henry', 'Beethoven, Ludwig', 'Begin, Menachem', 'Belloc, Hilaire', 'Bellow, Saul', 'Benchley, Robert', 'Benenson, Peter', 'Ben-Gurion, David', 'Benjamin, Walter', 'Benn, Tony', 'Bennington, Chester', 'Benson, Leana', 'Bent, Silas', 'Bentsen, Lloyd', 'Berger, Ric', 'Bergman, Ingmar', 'Berio, Luciano', 'Berle, Milton', 'Berlin, Irving', 'Berne, Eric', 'Bernhard, Sandra', 'Berra, Yogi', 'Berry, Halle', 'Berry, Wendell', 'Bethea, Erin', 'Bevan, Aneurin', 'Bevel, Ken', 'Biden, Joseph', 'Bierce, Ambrose', 'Biko, Steve', 'Billings, Josh', 'Biondo, Frank', 'Birrell, Augustine', 'Black, Elk', 'Blair, Robert', 'Blair, Tony', 'Blake, William'];
```
  
* **Array.prototype.filter()**  
    1. Filter the list of inventors for those who were born in the 1500's  
```
const fifteen = inventors.filter(function (inventor) {
  if (inventor.year >= 1500 && inventor.year < 1600) {
    return true; //keep it
  }
});
console.log(fifteen);
console.table(fifteen);
```  
Can refactor the function to an ES6 arrow function, remove the if statement and calculate all in one line  
  
```
const fifteen = inventors.filter(inventor => (inventor.year >= 1500 && inventor.year < 1600))
console.table(fifteen);
```  
  
* **Array.prototype.map()**  
    2. Give us an array of the inventors' first and last names  
```
const names = inventors.map(inventor => (inventor.first + "" + inventor.last))
console.log(names);
```
```
const names = inventors.map(inventor => `${inventor.first} ${inventor.last}`)
console.log(names);
```  
  
* **Array.prototype.sort()**  
    3. Sort the inventors by birthdate, oldest to youngest  
    Sort works by allowing you to compare two items - so the following example will jump through the array comparing people by birth year 2 people at a time. We presented the results in a table using console.table  
```
const ordered = inventors.sort(function(firstPerson, secondPerson){
  if(a.year > b.year) {
    return 1;
  } else {
      return -1;
    }
});
```
```
const ordered = inventors.sort((a, b) => a.year > b.year ? 1 : -1);
console.table(ordered);
```  
  
* **Array.prototype.reduce()**  
    4. How many years did all the inventors live?  
```
const totalYears = inventors.reduce((total, inventor) => {
    return total + (inventor.passed - inventor.year);
  }, 0);
console.table(inventors);
console.log(totalYears);
```  
* **.sort**    
    5. Sort the inventors by years lived   
```
const livedOrder = inventors.sort(function (a, b) {
const lastGuy = a.passed - a.year;
const nextGuy = b.passed - b.year;
   if (lastGuy > nextGuy) {
    return 1;
   } else {
      return -1;
   }
});
console.table(livedOrder);
```
```
const oldest = inventors.sort((a, b) => {
  const lastGuy = a.passed - a.year;
  const nextGuy = b.passed - b.year;
  return lastGuy > nextGuy ? -1 : 1;
});
console.table(oldest);
```  
* **.map and .filter**  
    6. create a list of Boulevards in Paris that contain 'de' anywhere in the name    
    
https://en.wikipedia.org/wiki/Category:Boulevards_in_Paris  
```
const category = document.querySelector(".mw-category");
const links = Array.from(category.querySelectorAll('a'));
const de = links
    .map(link => link.textContent)
    .filter(streetName => streetName.includes('de'));
```  
* **.sort**  
    7. sort Exercise - Sort the people alphabetically by last name      
```
const alpha = people.sort((lastOne, nextOne) => {
  const [aLast, aFirst] = lastOne.split(', ');
  const [bLast, bFirst] = lastOne.split(', ');
  return aLast > bLast ? -1 : 1;
});
console.log(alpha)
```  
* **.reduce**  
    8. Reduce Exercise - Sum up the instances of each of these  
```
const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck'];

const transportation = data.reduce(function (obj, item) {
    if (!obj[item]) {
      obj[item] = 0;
    }
    obj[item]++;
    return obj;
    }, {});
    console.log(transportation);
```  
  
```
const people = [
   { name: 'Wes', year: 1988 },
   { name: 'Kait', year: 1986 },
   { name: 'Irv', year: 1970 },
   { name: 'Lux', year: 2015 }
];

const comments = [
   { text: 'Love this!', id: 523423 },
   { text: 'Super good', id: 823423 },
   { text: 'You are the best', id: 2039842 },
   { text: 'Ramen is my fav food ever', id: 123523 },
   { text: 'Nice Nice Nice!', id: 542328 }
];
```  
* **Some and Every Checks**  
* **Array.prototype.some()**  
    9.Is at least one person 19 or older?  
```    
const isAdult = people.some(person => {
  const currentYear = (new Date()).getFullYear();
  return currentYear - person.year >= 19;
});
console.log({ isAdult });
```
```
const isAdult = people.some(person => ((new Date()).getFullYear()) - person.year >= 19)
console.log({ isAdult });
```
* **Array.prototype.every()**   
    10. Is everyone 19 or older?   
```    
const allAdults = people.every(person => {
  const currentYear = (new Date()).getFullYear();
  return currentYear - person.year >= 19;
});
console.log({ allAdults })
```
```
const allAdults = people.some(person => ((new Date()).getFullYear()) - person.year >= 19)
console.log({ allAdults });
```
```
const allOfAge = people.every((person) => {
   return person.year <= 2000
});
console.log(allOfAge)
```
* **Array.prototype.find()**
    11. Find is like filter, but instead returns just the one you are looking for. Find the comment with the ID of 823423  
```
const findId = comments.find(comment => {
  return comment.id === 823423
})
console.log(findId)
```
* **Array.prototype.findIndex()**
    12. Find and delete the comment with the ID of 823423  
```
const index = comments.findIndex(comment => {
   return comment.id === 823423
})
// can use splice to remove the item
comments.splice(index, 1);

console.log(index);

//or create a new array by slicing each side of the index
//... = spread operator from es6
const newComments = [
    ...comments.slice(0, index),
    ...comments.slice(index + 1)
];

console.table(newComments);  
```  
  
  
