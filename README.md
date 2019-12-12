# solved_tasks
* task 1
```javascript
const a = 123;
```
//Hello World!

* L1: Set Alarm
```javascript
function setAlarm(employed, vacation){
  return (employed === true && vacation === false) ? true : false;
}
```
* Be Concise I - The Ternary Operator
```javascript
const describeAge =(a)=>
  a<=12 ? "You're a(n) kid" :
  a<=17 ? "You're a(n) teenager" :
  a<=64 ? "You're a(n) adult" : "You're a(n) elderly";
```
* Basic Mathematical Operations
```javascript
function basicOp(operation, v1, v2) {
  let res;
  switch (operation) {
    case '+': return res = v1 + v2;
    case '-': return res = v1 - v2;
    case '*': return res = v1 * v2;
    case '/': return res = v1 / v2;
    }
}
```
* Power of two
```javascript
function isPowerOfTwo(x) {
  const n = Math.log2(x);
  return Math.ceil(n) - n === 0; 
}
```