Commands for the JS Console
======  

```
<p onClick="makeGreen()">×BREAK×DOWN×</p>

const dogs = [{ name: 'Snickers', age: 2 }, { name: 'hugo', age: 8 }];
const paragraph = document.querySelector('p');

function makeGreen() {
  const p = document.querySelector('p');
  p.style.color = '#BADA55';
  p.style.fontSize = '50px';
}
```  
  
  
* Regular 
```
console.log('hello');  
```   
* Interpolated  
```
console.log('Hello I am a %s string!', '🐵');
console.log(`Hello I am ${variable}`);
```
* Styled    
```
console.log('%c I am some great text', 'fontsize:50px; background:red; color:white;');
```
* Warning!  
```
console.warn('OHH NOOOOO');
```
* Error :|  
```  
console.error('Shit!');
```
* Info  
```
console.info('Crocodiles eat 3-4 people per year');
```  
* Testing  
*.assert checks if something is true and only returns something if it is false*  
```
console.assert(1 === 1, "That is wrong!") //This wont return anything because it is true
console.assert(1 === 2, "That is wrong, really!") //This will return a value because it is false
```  
* Clearing  
```
console.clear()
```  
* Viewing DOM Elements  
```
console.log(paragraph) 
console.dir(paragraph) //gives you the class list on this paragraph element
```  
* Grouping together  
```
dogs.forEach(dog => {
  console.group(`${dog.name}`);
  console.log(`This is ${dog.name}`);
  console.log(`${dog.name} is ${dog.age}`);
  console.log(`${dog.name} is ${dog.age}`);
  console.groupEnd(`${dog.name}`);
  });
  
// for a collapsed group use:
dogs.forEach(dog => {
  console.groupCollapsed(`${dog.name}`);
  console.log(`This is ${dog.name}`);
  console.log(`${dog.name} is ${dog.age}`);
  console.log(`${dog.name} is ${dog.age}`);
  console.groupEnd(`${dog.name}`);
  });
```
* Counting    
```
console.count('Dan');
console.count('Dan');
console.count('Dan');
console.count('Steve');
console.count('Steve');
console.count('Steve');
console.count('Dan');
console.count('Dan');
console.count('Steve');
```
* Timing   
```
console.time('fetching data');
fetch('https://api.github.com/users/kodee1980')
  .then(data => data.json())
  .then(data => {
console.timeEnd('fetching data');
console.log(data);
});
```  
* Table  
```
console.table(dogs);
```
