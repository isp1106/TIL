## datatype 확인
```javascript
console.log(typeof 'Hello world!'); //String
console.log(typeof 123);  //Number
console.log(typeof true); //Boolean
console.log(typeof undefined); //undefined
console.log(typeof null); // Null
console.log(typeof {}); //Object
console.log(typeof []); //Array

function getType(data) {
  return Object.prototype.toString.call(data);
}

console.log(getType(123)); //Number
console.log(getType(false)); //Boolean
console.log(getType(null)); // Null
console.log(getType({})); //Object
console.log(getType([])); //Array
```

## javascript import / export
```javascript
- getType.js
export default function getType(data) {
  return Object.prototype.toString.call(data).slice(8, -1);
}

- main.js
import getType from './getType'
```
