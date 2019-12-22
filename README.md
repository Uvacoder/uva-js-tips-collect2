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
* Powers of 3
```javascript
function largestPower(n){
  let k = 0;
  while (Math.pow(3, k) < n) k++;
    return k - 1;
}
```
* Factorial 1
```javascript
function factorial(n){
  if (n === 0) return 1;
  if (n < 0 || n > 12) throw new RangeError();
  let res = 1;
  for (let i = 1; i <= n; i++) {
    res *= i;
  }
  return res;
}
```
* Sum of the first nth term of Series
```javascript
function SeriesSum(n) {
  if (n === 0) return '0.00';
  let sum = 1;
  for (let i = 4; i < n * 3; i += 3) {
    sum = sum + 1/i;
  }
  return String(sum.toFixed(2));
}
```
* Filter the number
```javascript
const FilterString = function(value) {
  let str = '';
  for (let i = 0; i < value.length; i++) {
    if (!isNaN(value[i])) str += value[i];
  }
  return Number(str);
}
```
* Is integer safe to use?
```javascript
const SafeInteger = (n) => Number.isSafeInteger(n);
```
* Invert values
```javascript
function invert(array) {
   if (array.length === 0) return [];
   for (let i = 0; i < array.length; i++) {
     array[i] = -array[i];
   }
   return array;
}
```
* Alan Partridge II - Apple Turnover
```javascript
function apple(x){
  if (typeof x === 'string') x = Number(x);
  if (Math.pow(x, 2) > 1000) return 'It\'s hotter than the sun!!';
  else return 'Help yourself to a honeycomb Yorkie for the glovebox.';
}
```
* You're a square!
```javascript
const isSquare = function(n) {
   return Math.sqrt(n) % 1 === 0;
}
```
* Beginner Series #4 Cockroach
```javascript
const cockroachSpeed = (s) => Math.floor(s * 1e+5 / 3600);
```
* Holiday VIII - Duty Free
```javascript
const dutyFree = (normPrice, discount, hol) => Math.floor(hol/(normPrice * discount * 0.01));
```
* Lario and Muigi Pipe Problem
```javascript
function pipeFix(numbers){
  const min = Math.min(...numbers);
  const max = Math.max(...numbers);
  const arr = [];
  for (let i = min; i <= max; i++) {
    arr.push(i);
  }
  return arr;
}
```
* Expressions Matter
```javascript
function expressionMatter(a, b, c) {
  return Math.max(a + b + c, a * b * c, (a + b) * c, a * (b + c), a * b + c, a + b * c);
}
```
* For Twins: 2. Math operations
```javascript
function iceBrickVolume(radius, bottleLength, rimLength) {
  return (2 * radius ** 2) * (bottleLength - rimLength);
}
```
* Vowel Count
```javascript
function getCount(str) {
  let vowelsCount = 0;
  let arrVowels = ['a', 'e', 'i', 'o', 'u' ];
  for (let i = 0; i < str.length; i++) {
    for (let j = 0; j < arrVowels.length; j++) {
      if (str[i] === arrVowels[j]) {
        vowelsCount++;
        }
    }
  }
  return vowelsCount;
}
```
* Count Odd Numbers below n
```javascript
const oddCount = (n) => Math.floor(n / 2);
```