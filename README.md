## solved_tasks from Codewars

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
* Calculate Price Excluding VAT
```javascript
function excludingVatPrice(price) {
  if (price === null) return -1;
  else return +(price / 1.15).toFixed(2);
}
```
* Binary Addition
```javascript
const addBinary = (a,b) => (a + b).toString(2);
```
* Filling an array (part 1)
```javascript
const arr = N => {
  const arr = [];
  for (let i = 0; i < N; i++) {
    arr.push(i);
  }
  return arr;
}
```
* Count the Monkeys!
```javascript
function monkeyCount(n) {
  const arr = [];
  for (let i = 1; i <= n; i++) {
    arr.push(i);
  }
  return arr;
}
```
* Sum Arrays
```javascript
function sum (numbers) {
  if (numbers.length === 0) return 0;
  let count = 0;
  for (let i = 0; i < numbers.length; i++) {
    count += numbers[i];
  }
  return count;     
}
```
* To square(root) or not to square(root)
```javascript
function squareOrSquareRoot(array) {
  const arr = [];
  for (let i = 0; i < array.length; i++) {
    if (Number.isInteger(Math.sqrt(array[i]))) {
      arr.push(Math.sqrt(array[i]));
    } else {
      arr.push(Math.pow(array[i], 2));
    }
  }
  return arr; 
}
```
* Is every value in the array an array?
```javascript
const arrCheck = value => {
  if (value.length === 0) return true;
  for (let i = 0; i < value.length; i++) {
    if (Array.isArray(value[i]) === false) return false;
  }
  return true;
}
```
* A Needle in the Haystack
```javascript
function findNeedle(haystack) {
let index = 0;
  for (let i = 0; i < haystack.length; i++) {
    if (haystack[i] === 'needle') index = i;
  }
  return `found the needle at position ${index}`;
}
```
* Difference of Volumes of Cuboids
```javascript
const findDifference = (a, b) => {
  let vol1 = 1;
  let vol2 = 1;
  for (let i = 0, j = 0; i < a.length, j < b.length; i++, j++) {
    vol1 *= a[i]; vol2 *= b[j];
  }
  return Math.abs(vol1 - vol2);
}
```
* Enumerable Magic #3 - Does My List Include This?
```javascript
function include(arr, item){
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === item) return true;
  }
  return false;
}
```
* Counting sheep...
```javascript
function countSheeps(arrayOfSheep) {
  if (arrayOfSheep.length === 0) return 0;
  let count = 0;
  for (let i = 0; i < arrayOfSheep.length; i++) {
    if (arrayOfSheep[i] === true) count++;
  }
  return count;
}
```
* Find the first non-consecutive number
```javascript
function firstNonConsecutive (arr) {
  for (let i = 0; i < arr.length - 1; i++) {
    if (arr[i + 1] !== arr[i] + 1) return arr[i + 1];
  }
  return null;
}
```
* Odd or Even?
```javascript
function oddOrEven(array) {
   let sum = 0;
   for (let i = 0; i < array.length; i++) {
     sum += array[i];
   }
   return sum % 2 === 0 ? 'even' : 'odd';
}
```
* Divide and Conquer
```javascript
function divCon(x){
  let sum1 = 0;
  let sum2 = 0;
  for (let i = 0; i < x.length; i++) {
    if (typeof x[i] === 'number') sum1 += x[i];
    if (typeof x[i] === 'string') sum2 += +x[i];
  }
  return sum1 - sum2;
}
```
* Sum of Odd Cubed Numbers
```javascript
function cubeOdd(arr) {
  let sum = 0;
  const cubedArr = [];
  for (let i = 0; i < arr.length; i++) {
    if (typeof arr[i] !== 'number') return undefined;
    cubedArr.push(Math.pow(arr[i], 3));
    if (Math.abs(cubedArr[i]) % 2 === 1) sum += cubedArr[i];
  }
return sum;
}
```
* Remove the minimum
```javascript
function removeSmallest(numbers) {
  if (numbers.length === 0) return [];
  let min = numbers[0];
  let index = 0;
  for (let i = 1; i < numbers.length; i++) {
    if (numbers[i] < min) {
      min = numbers[i];
      index = i;
      }
  }
  const arr = [];
  for (let i = 0; i < numbers.length; i++) {
    if (index === i) continue;
    arr.push(numbers[i]);
    }
  return arr;
}
```
* Sum without highest and lowest number
```javascript
function sumArray(array) {
  if (array === null || array.length <= 1) return 0;
//   const min = Math.min(...array);
//   const max = Math.max(...array);
  let sum = 0;
  for (let i = 0; i < array.length; i++) {
    sum += array[i];
  }
//   return sum - min - max;
return sum - Math.min(...array) - Math.max(...array);
}
```
* Find the divisors!
```javascript
function divisors(integer) {
  const arr = []; 
  for (let i = 2; i < integer; i++) {
    if (integer % i === 0) arr.push(i);
  }
  return arr.length === 0 ? `${integer} is prime` : arr;
}
```
* Be Concise IV - Index of an element in an array
```javascript
const find = (array, element) => array.includes(element) ? array.indexOf(element) : 'Not found';
```
* Array.diff
```javascript
const array_diff = (a, b) => a.filter(el => !b.includes(el));
```
* filterEvenLengthWords
```javascript
const filterEvenLengthWords = words => words.filter(el => el.length % 2 === 0);
```
* Find how many times did a team from a given country win the Champions League?
```javascript
function countWins (winnerList, country) {
  let winNum = 0;
  for (let i = 0; i < winnerList.length; i++) {
    if (winnerList[i].country === country) winNum++;
  }
  return winNum;
}
```
* Sum of differences in array
```javascript
function sumOfDifferences(arr) {
 const sorted = arr.sort((a, b) => b - a);
let sum = 0;
for(let i = 0; i < arr.length - 1; i++) {
  sum += sorted[i] - sorted[i + 1];

}
return sum;
}
```
* Well of Ideas - Easy Version
```javascript
function well(x){
  const numOfIdeas = x.filter(el => el === 'good').length;
  if (numOfIdeas >= 1 && numOfIdeas <=2) return 'Publish!';
  else if (numOfIdeas > 2) return 'I smell a series!';
  else return 'Fail!'
}
```
* Find the Slope
```javascript
function slope(points) {
  if (points[2] - points[0] === 0) return 'undefined';
  else return ((points[3] - points[1]) / (points[2] - points[0])).toString();
}
```
* Array plus array
```javascript
function arrayPlusArray(arr1, arr2) {
  const sum1 = arr1.reduce((acc, cur) => acc + cur);
  const sum2 = arr2.reduce((acc, cur) => acc + cur);
  return sum1 + sum2; 
}
```
* Sum Arrays
```javascript
const sum = numbers => numbers.reduce((acc, el) => acc + el, 0);
```
* SpeedCode #2 - Array Madness
```javascript
function arrayMadness(a, b) {
  const sumOfSquares = a.reduce((acc, el) => acc + Math.pow(el, 2), 0);
  const sumOfCubes = b.reduce((acc, el) => acc + Math.pow(el, 3), 0);
  return sumOfSquares >= sumOfCubes;
}
```
* Convert number to reversed array of digits
```javascript
const digitize = n => String(n).split('').map(el => +el).reverse();
```
* Enumerable Magic #25 - Take the First N Elements
```javascript
const take = (arr, n) => arr.splice(0, n); 
//const take = (arr, n) => arr.slice(0, n);
```
* Remove First and Last Character Part Two
```javascript
function array(arr) {
  const res = arr.split(',').slice(1, -1).join(' ');
  return res.length >= 1 ? res : null;
}
```
* Abbreviate a Two Word Name
```javascript
function abbrevName(name){
  let ind;
  for (let i = 0; i < name.length; i++) {
    if (name.charAt(i) === ' ') ind = i;
  }
  return `${name[0]}.${name[ind + 1]}`.toUpperCase();
}
```
* Double Char
```javascript
function doubleChar(str) {
  let newStr = '';
  for (let i = 0; i < str.length; i++) {
    newStr += str[i] + str[i];
  }
  return newStr;
}
```
* Regex count lowercase letters
```javascript
function lowercaseCount(str){
  let count =  0;
  const string = 'abcdefghijklmnopqrstuvwxyz';
  for (let i = 0; i < str.length; i++) {
    if (string.includes(str[i])) count++;
  }
  return count;
}
```
* Spacify
```javascript
function spacify(str) {
  let newStr = '';
  for (let i = 0; i < str.length; i++) {
    newStr += str[i] + ' ';
  }
  console.log(newStr);
  return newStr.slice(0, -1);
}
```
* Unique In Order
```javascript
const uniqueInOrder = (iterable) => {
  let res = [];
  for(let i = 0; i < iterable.length; i++) {
    if(iterable[i + 1] !== iterable[i]) {
      res.push(iterable[i]);
    }
  }
  return res;
}
```
* Thinking & Testing : Something capitalized
```javascript
function testit(s){
  let arr = s.split('');
  for (let i = 0; i < arr.length; i++){
    if (arr[i + 1]=== ' ' || arr[i + 1] === undefined) {
      arr[i] = arr[i].toUpperCase();
    }
  }
return arr.join('');
}
```
* Mumbling
```javascript
function accum(s) {
	const arr = [];
	for (let i = 0; i < s.length; i++) {
    let str = s[i].toUpperCase();
    for (let j = 0; j < i; j++ ) {
        str += s[i].toLowerCase();
      }
      arr.push(str);
    }
    return arr.join('-');
}
```
* Do you speak "English"?
```javascript
function spEng(sentence){
  return sentence.toLowerCase().includes('english');
}
```
* Don't give me five!
```javascript
function dontGiveMeFive(start, end) {
  let count = 0;
  for (let i = start; i < end + 1; i++) {
    if (!String(i).includes('5')) count++;
  }
  return count;
}
```
* Regex validate PIN code
```javascript
const validatePIN = pin => {
    let str = '0123456789';
    for (let i = 0; i < pin.length; i++) {
     if (!(str.includes(pin[i]))) return false;
    }
    return pin.length === 4 || pin.length === 6;
 }
```
* Credit Card Mask
```javascript
function maskify(cc) {
  if (cc.length < 4) return cc;
  let res = '';
  for (let i = 0; i < cc.length - 4; i++) {
    res += '#';
  }
  return res + cc.slice(-4);
}
```
* Tail Swap
```javascript
function tailSwap(arr) {
  const resArr = arr.join(':').split(':');
  return [`${resArr[0]}:${resArr[3]}`, `${resArr[2]}:${resArr[1]}`];
}
```
* Numbers to Letters
```javascript
function switcher(x){
  const str = ' zyxwvutsrqponmlkjihgfedcba!? ';
  const arr = x.map(el => str[el]);
  return arr.join('');
}
```
* 5 without numbers !!
```javascript
const unusualFive = () => 'apple'.length;
```
* Vowel remover
```javascript
function shortcut(string){
  return string.replace(/[aouie]/g,'');
}
```
* Fake Binary
```javascript
function fakeBin(x){
  return x.replace(/[0-4]/g, 0).replace(/[5-9]/g, 1);
}
```
* Get number from string
```javascript
function getNumberFromString(s) {
  return +s.replace(/\D/g, '');
}
```
* Correct the mistakes of the character recognition software
```javascript
function correct(string) {
	return string.replace(/5/g, 'S').replace(/0/g, 'O').replace(/1/g, 'I');
}
```
* Name Shuffler
```javascript
function nameShuffler(str) {
  return str.split(' ').reverse().join(' ');
}
```
* Squash the bugs
```javascript
function findLongest(str) {
  
  const spl = str.split(" ");
  let longest = 0;
  
  for (let i = 0; i < spl.length; i++) {
    if (spl[i].length > longest) longest = spl[i].length;
  }
  return longest;
}
```
* Every possible sum of two digits
```javascript
function digits(num){

  const arr = String(num).split('');
  const arrSum = [];
  
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++)
    arrSum.push(+arr[i] + +arr[j]);
  }
  return arrSum;
}
```
* Is every value in the array an array?
```javascript
const arrCheck = value => {
  if (value.length === 0) return true;
  for (let i = 0; i < value.length; i++) {
    if (Array.isArray(value[i]) === false) return false;
  }
  return true;
}
```
* What is type of variable?
```javascript
function type(value) {
  if (value === null) return 'null';
  if (Array.isArray(value)) return 'array';
  if (value instanceof Date) return 'date';
  if (value instanceof Object) return 'object';
  return typeof value;
}
```
* Tortoise racing
```javascript
function race(v1, v2, g) {
    if (v1 >= v2) return null;
    const time = g / (v2 - v1);
    const hour = Math.trunc(time);
    const min = Math.trunc((time * 60) % 60);
    const sec = Math.trunc((time * 3600) % 60);
    return [hour, min, sec];
}
```
* Highest and Lowest
```javascript
function highAndLow(numbers){
  const arr = numbers.split(' ');
  const min = Math.min(...arr);
  const max = Math.max(...arr);
  return `${max} ${min}`;
}
```
* Descending Order
```javascript
function descendingOrder(n){
  const arr = String(n).split('').sort((a, b) => b - a);
  return +arr.join('');
}
```
* Can Santa save Christmas?
```javascript
function determineTime(durations){
  let sum = 0;
  for (let i = 0; i < durations.length; i++) {
    const arr = durations[i].split(':');
    let hours = arr[0] * 3600;
    let minutes = arr[1] * 60;
    let seconds = +arr[2];
    sum += hours + minutes + seconds;
  }
  return sum <= 86400;
}
```
* Welcome!
```javascript
 const data = {
	english: 'Welcome',
  czech: 'Vitejte',
  danish: 'Velkomst',
  dutch: 'Welkom',
  estonian: 'Tere tulemast',
  finnish: 'Tervetuloa',
  flemish: 'Welgekomen',
  french: 'Bienvenue',
  german: 'Willkommen',
  irish: 'Failte',
  italian: 'Benvenuto',
  latvian: 'Gaidits',
  lithuanian: 'Laukiamas',
  polish: 'Witamy',
  spanish: 'Bienvenido',
  swedish: 'Valkommen',
  welsh: 'Croeso',
  IP_ADDRESS_INVALID: 'Welcome',
  IP_ADDRESS_NOT_FOUND: 'Welcome',
  IP_ADDRESS_REQUIRED: 'Welcome',
  }
  
 const greet = (language) => data[language];
```
* Duck Duck Goose
```javascript
const duckDuckGoose = (players, goose) => players[(goose - 1) % players.length].name;
```
* Check the exam
```javascript
function checkExam(arr1, arr2) {
  let score = 0;
  for (let i = 0; i < arr1.length; i++) {
      if (arr1[i] === arr2[i]) score += 4;
      if (arr1[i] !== arr2[i] && arr2[i] === '') score += 0;
      if (arr1[i] !== arr2[i] && arr2[i] !== '') score -= 1;
  }
  return score > 0 ? score : 0;
}
```
* If you can't sleep, just count sheep!
```javascript
let countSheep = function (num){
  let s = '';
  for (let i = 1; i <= num; i++) {
    s += `${i} sheep...`;
  }
  return s;
}
```
* Total amount of points
```javascript
function points(games) {
  let points = 0;

  for(let i = 0; i < games.length; i++) {
    let x = parseInt(games[i].split(':')[0]);
    let y = parseInt(games[i].split(':')[1]);
    if(x === y) points += 1;
    if(x > y) points += 3;
  }
  return points;
}
```
* Breaking chocolate problem
```javascript
const breakChocolate = (n, m) => n === 0 || m === 0 ? 0 : n * m - 1;
```
* Sum of angles
```javascript
const angle = (n) => 180 * (n - 2);
```

