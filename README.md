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
```javascript
const validatePIN = pin => /^(\d{4}|\d{6})$/.test(pin);
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
* A wolf in sheep's clothing
```javascript
function warnTheSheep(queue) {
  if(queue.indexOf('wolf') === queue.length-1) {
    return "Pls go away and stop eating my sheep";
  } else {
    return `Oi! Sheep number ${queue.length-1 - queue.indexOf('wolf')}! You are about to be eaten by a wolf!`;
  }
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
   }
   
  const greet = (language) => data[language] || data.english;
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
* I love you, a little , a lot, passionately ... not at all
```javascript
function howMuchILoveYou(nbPetals) {
    const flower = ['not at all', 'I love you', 'a little', 'a lot', 'passionately', 'madly'];
    return flower[nbPetals % 6];
}
```
* DNA to RNA Conversion
```javascript
function DNAtoRNA(dna) {
  return dna.replace(/T/g, 'U');
}
```
* Is it a palindrome?
```javascript
function isPalindrome(x) {
  let strReverse = '';
  for (let i = 0; i < x.length; i++) {
    strReverse = x[i] + strReverse;
  }
  return x.toLowerCase() === strReverse.toLowerCase();
}
```
* Remove String Spaces
```javascript
function noSpace(x){
  let newStr = '';
  for (let i = 0; i < x.length; i++){
    if (x[i] !== ' ') newStr += x[i];
  }
  return newStr;
}
```
* Reversed Words
```javascript
const reverseWords = str => str.split(' ').reverse().join(' ');
```
* Do I get a bonus?
```javascript
function bonusTime(salary, bonus) {
 return bonus == true ?  `\u00A3${salary * 10}` : `\u00A3${salary}`;
}
```
* Complementary DNA
```javascript
function DNAStrand(dna){
  let compl = '';
  for (let i = 0; i < dna.length; i++) {
    if (dna[i] === 'A') compl += 'T';
    if (dna[i] === 'T') compl += 'A';
    if (dna[i] === 'C') compl += 'G';
    if (dna[i] === 'G') compl += 'C';
  }
  return compl;
}
```
* validate code with simple regex
```javascript
function validateCode(code) {
  code = String(code);
  return (code.startsWith(1) || code.startsWith(2) || code.startsWith(3));
}
```
* Flatten and sort an array
```javascript
function flattenAndSort(array) {
  let arr = [];
  array.forEach(el => {
    if (Number.isInteger(el)) {
      arr.push(el);
    } else if (Array.isArray(el) && el.length) {
      arr = [...arr, ...el];
    }
  })
  return arr.sort((a, b) => a - b);
}
```
* FIXME: Replace all dots
```javascript
const replaceDots = function(str) {
  return str.replace(/[.]/g, '-');
}
```
* MakeUpperCase
```javascript
const makeUpperCase = (str) => str.toUpperCase();
```
* The Wide-Mouthed frog!
```javascript
function mouthSize(animal) {
  return animal.toLowerCase() === 'alligator' ? 'small' : 'wide';
  }
```
* 5 without numbers !!
```javascript
const unusualFive = () => 'apple'.length;
```
* Santa's Naughty List
```javascript
function findChildren(santasList, children) {
  return santasList.filter((el, i)=> children.includes(el) && i === santasList.indexOf(el)).sort();
}
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
```javascript
function invert(array) {
   return array.map(el => -el);
}
```
* SpeedCode #2 - Array Madness
```javascript
function arrayMadness(a, b) {
  const sumOfSquares = a.reduce((acc, el) => acc + Math.pow(el, 2), 0);
  const sumOfCubes = b.reduce((acc, el) => acc + Math.pow(el, 3), 0);
  return sumOfSquares >= sumOfCubes;
}
```
* Sum Arrays
```javascript
function sum (numbers) {
    "use strict";
  if (numbers.length ===0) return 0;
  let count = 0;
  for (let i = 0; i < numbers.length; i++) {
    count += numbers[i];
  }
  return count;     
}
```
```javascript
const sum = numbers => numbers.reduce((acc, el) => acc + el, 0);
```
* Grasshopper - Array Mean
```javascript
const findAverage = function (nums) {
  return nums.reduce((acc, el) => acc + el, 0) / nums.length;
}
```
* Get number from string
```javascript
function getNumberFromString(s) {
  return +s.replace(/\D/g, '');
}
```
* Create Phone Number
```javascript
function createPhoneNumber(numbers){
  numbers.splice(6, 0, '-');
  return `(${numbers.join('').slice(0, 3)}) ${numbers.join('').slice(3)}`;
}
```
* Incrementer
```javascript
function incrementer(nums) {
    return nums.map((el, i) => (el + i + 1) % 10);
}
```
* Lottery machine
```javascript
function lottery(str){
    const num = str.replace(/[a-z, A-Z]/ig,'');
    if ( num === '') {
        return 'One more run!';
    } else {
        return num.split('').filter((el, i) => i === num.indexOf(el) ).join('');
    }
}
```
* Remove duplicate words
```javascript
function removeDuplicateWords(s) {
    return s.split(' ').filter((el, i, arr) => i === arr.indexOf(el)).join(' ');
}
```
* Check three and two
```javascript
function checkThreeAndTwo(arr) {
  let a = 0;
  let b = 0;
  let c = 0;
  for (let i = 0; i < arr.length; i++){
    if (arr[i] === "a") a += 1;
    if (arr[i] === "b") b += 1;
    if (arr[i] === "c") c += 1;
  }

  return (a === 2 || b === 2 || c === 2) && (a === 3 || b === 3 || c === 3);
}
```
* makeBackronym
```javascript
const makeBackronym = function(string){
  let res = '';
  const arr = string.toUpperCase().split('');
    for (let i = 0; i < arr.length; i++){
      res = res + dict[arr[i]] + ' ';
    }
  return res.slice(0, -1);
};
```
* Make a function that does arithmetic!
```javascript
function arithmetic(a, b, operator){
  const obj = {};
  obj.add = a + b;
  obj.subtract = a - b;
  obj.multiply = a * b;
  obj.divide = a / b;
  return obj[operator];
}
```
* Job Matching #1
```javascript
function match(candidate, job) {
  if(!candidate.minSalary || !job.maxSalary) throw "Error";
  return (candidate.minSalary * 0.9) <= job.maxSalary;
}
```
* Add property to every object in array
```javascript
for (let i = 0; i < questions.length; i++){
  questions[i].usersAnswer = null;
}
```
```javascript
questions.map(el => el.usersAnswer = null);
```
* Coding Meetup #2 - Higher-Order Functions Series - Greet developers
```javascript
function greetDevelopers(list) {
 list.forEach(function(el){
   el.greeting = `Hi ${el.firstName}, what do you like the most about ${el.language}?`;
  });
  return list;
}
```
```javascript
function greetDevelopers(list) {
  for (let i = 0; i < list.length; i++){
    list[i].greeting = `Hi ${list[i].firstName}, what do you like the most about ${list[i].language}?`
  }
  return list;
}
```
* Multiples of 3 or 5
```javascript
function solution(num){
    let sum = 0;
    for (let i = 1; i < num; i++) {
        if (i % 3 === 0 || i % 5 === 0) sum +=i;
    }
    return sum;
}
```
* 8 towers
```javascript
const towerCombination = n => n === 1 ? 1 : n * towerCombination(n - 1);
```
* Numbers to Objects
```javascript
function numObj(s){
  const arr = [];
  for (let i = 0; i < s.length; i++){
    const obj = {};
    obj[s[i]] = String.fromCharCode(s[i]);
    arr.push(obj);
  }
  return arr;
}
```
```javascript
function numObj(s){
  const arr = [];
  for (let i = 0; i < s.length; i++){
    arr.push({[s[i]]: String.fromCharCode(s[i])});
  }
  return arr;
}
```
* Coding Meetup #1 - Higher-Order Functions Series - Count the number of JavaScript developers coming from Europe
```javascript
function countDevelopers(list) {
  let count = 0;
  for (let i = 0; i < list.length; i++){
    if (list[i].continent === 'Europe' && list[i].language === 'JavaScript') count++;
  }
  return count;
}
```
```javascript
function countDevelopers(list) {
  return list.filter(el => el.continent === 'Europe' && el.language === 'JavaScript').length;
}
```
* Math engine
```javascript
function mathEngine(arr) {
  if (!arr) return 0;
  let prodOfPos = 1;
  let sumOfNeg = 0;
  for (let i = 0; i < arr.length; i++) {
    arr[i] < 0 ? sumOfNeg +=arr[i] : prodOfPos *=arr[i];
  }
  return prodOfPos + sumOfNeg;
}
```
* The wheat/rice and chessboard problem
```javascript
function squaresNeeded(grains){
    let i = 0;
    if (grains === 0) return 0;
    while (grains / 2 >= 1) {
        grains = grains / 2;
        i++;
    }
    return i + 1;
}
```
* What is my name score? #1
```javascript
function nameScore(name){
  let sum = 0;
  let obj = {};
  for(let i = 0; i < name.length; i++){
    for(let key in alpha){
      if(key.includes(name[i].toUpperCase())) sum = sum + alpha[key];
    }
  }
  obj[name] = sum;
  return obj;
}
```
* The Office I - Outed
```javascript
function outed(meet, boss){
  let totalScore = 0;
  let rating;
  
  for (let key in meet){
    if (key === boss) meet[key] = 2 * meet[key];
    totalScore += meet[key];
  }
  rating = totalScore / Object.keys(meet).length;
  return rating <= 5 ? 'Get Out Now!' : 'Nice Work Champ!';
}
```
* How many days are we represented in a foreign country?
```javascript
function daysRepresented(trips){
  const days = [];
  for (let i = 0; i < trips.length; i++){
    for (let j = trips[i][0]; j <= trips[i][1]; j++){
      if (!days.includes(j)) days.push(j);
    }
  }
  return days.length;
}
```
```javascript
function daysRepresented(trips){
  const obj = {};
  for (let i = 0; i < trips.length; i++){
    for (let j = trips[i][0]; j <= trips[i][1]; j++){
      if (!obj[j]) obj[j] = 1;
    }
  }
  return Object.keys(obj).length;
}
```
* Permute a Palindrome
```javascript
function permuteAPalindrome (input) { 
  const obj = {};
  for (let i = 0; i < input.length; i++){
    if (obj[input[i]]) obj[input[i]]++;
      else obj[input[i]] = 1;
  }
  let count = 0;
  for (let key in obj){
    if (obj[key] % 2 === 1) count++;
  }
  return count <= 1;
  
}
```
```javascript
function permuteAPalindrome (input) { 
  const obj = {};
  for (let i of input){
    if (obj[i]) delete obj[i];
      else obj[i] = 1;
  }
  return Object.keys(obj).length <= 1;
}
```
* Most valuable character
```javascript
function solve(st) {
     const obj = {};
     for (let i = 0; i < st.length; i++){
       obj[st[i]] = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
     }
     const array = Object.values(obj);
     const max = Math.max(...array);
     
     const arr = [];
     for (let key in obj){
       if (obj[key] === max) arr.push(key);
     }
     
     const res = arr.sort();
   return res[0];
}
```
* The Office II - Boredom Score
```javascript
function boredom(staff){
  const obj = {
    'accounts': 1,
    'finance': 2,
    'canteen': 10,
    'regulation': 3,
    'trading': 6,
    'change': 6,
    'IS': 8,
    'retail': 5,
    'cleaning': 4,
    'pissing about': 25
  };
  const arr = [];
  for (let key in staff){
    arr.push(obj[staff[key]]);
  }
  const score = arr.reduce((a, b) => a + b);
  return score >= 100 ? 'party time!!': score < 100 && score > 80 ? 'i can handle this' : 'kill me now'; 
}
```
* Coding Meetup #6 - Higher-Order Functions Series - Can they code in the same language?
```javascript
function isSameLanguage(list) {
  const arr = [];
  for (let item in list){
    arr.push(list[item].language);
  }
  console.log(arr)
  return list.every(el => el.language === list[0].language);
}
```
```javascript
const isSameLanguage = list => list.every(e => e.language === list[0].language);
```
* Coding Meetup #3 - Higher-Order Functions Series - Is Ruby coming?
```javascript
function isRubyComing(list) {
  const arr = [];
  for (let item in list){
     arr.push(list[item].language);
  }
  return arr.includes('Ruby');
}
```
```javascript
function isRubyComing(list) {
  for (let i = 0; i < list.length; i++){
    if (list[i].language === 'Ruby') return true;
  }
  return false;
}
```
```javascript
const isRubyComing = list => list.some(el => el.language === 'Ruby');
```
* String Reordering
```javascript
function sentence(List) {
  const arr = [];
  for (let el in List){
    arr.push(Object.keys(List[el])[0]);
  }
  
  const arrSorted = arr.sort((a, b) => a - b);
  
  const res = [];
  for (let item in arrSorted){
    for (let obj in List){
      if (arrSorted[item] === Object.keys(List[obj])[0]) {
        res.push(Object.values(List[obj])[0]);
      }
    }
  }
  return res.join(' ');
}
```
```javascript
function sentence(List) {
  const arr = [];
  for (let el in List){
    arr.push(Object.keys(List[el])[0]);
  }
  console.log(arr);
  const arrSorted = arr.sort((a, b) => a - b);
  console.log(arrSorted);
  let str = '';
  for (let item in arrSorted){
    for (let obj in List){
      if (arrSorted[item] === Object.keys(List[obj])[0])  str += Object.values(List[obj])[0] + ' ';
    }
  }
  return str.trim();
}
```
```javascript
function sentence(List) {
  const arr = List.sort((a, b) => Object.keys(a) - Object.keys(b));
  const str = arr.map(obj => Object.values(obj)).join(' ');
  return str;
}
```
* Coding Meetup #7 - Higher-Order Functions Series - Find the most senior developer
```javascript
function findSenior(list) {
  const arr = [];
  for (let i = 0; i < list.length; i++){
    arr.push(list[i].age);
  }
  arr.sort((a, b) => b - a);
  const max = Math.max(...arr);
  
  const res = [];
  for (let i = 0; i < list.length; i++){
    if (list[i].age === max) res.push(list[i]);
  }
  return res;
}
```
```javascript
const findSenior = list => {
  let max = Math.max(...list.map(el => el.age));
  return list.filter(el => el.age === max);
}
```
* Coding Meetup #10 - Higher-Order Functions Series - Create usernames
```javascript
function addUsername(list) {
  const date = new Date().getFullYear();
  for (let el in list){
    list[el].username = (list[el].firstName).toLowerCase() + (list[el].lastName)[0].toLowerCase() + (date - (list[el].age));
  }
  console.log(list);
  return list;
}
```
* Simple fibonacci strings
```javascript
function solve(n){
         let f0 = '0';
         let f1 = '01';
         let f2;
       if (n === 0) return f0;
       if (n === 1) return f1;
         let i = 2;
         while (i <= n){
           f2 = f1 + f0;
           f0 = f1;
           f1 = f2;
           i++;
         }
       return f2;
   }
```
* N-th Fibonacci
```javascript
function nthFibo(n) {
  let f1 = 0;
  let f2 = 1;
  let f3;
  if (n === 1) return f1;
  if (n === 2) return f2;
  for (let i = 3; i <= n; i++){
    f3 = f1 + f2;
    f1 = f2;
    f2 = f3;
  }
  return f3;
}
```
* Fibonacci Reloaded
```javascript
function fib(n) {
  let f1 = 0;
  let f2 = 1;
  let f3;
  if (n === 1) return f1;
  if (n === 2) return f2;
  for (let i = 3; i <= n; i++){
    f3 = f1 + f2;
    f1 = f2;
    f2 = f3;
  }
  return f3;
}
```
* Basic Calculator
```javascript
function calculate (num1, operation, num2) {
   switch(operation) {
     case '+': return num1 + num2;
     case '-': return num1 - num2;
     case '*': return num1 * num2;
     case '/': return (num2 === 0) ? null: num1 / num2;
     default: return null;
   }
}
```
* Coding Meetup #8 - Higher-Order Functions Series - Will all continents be represented?
```javascript
function allContinents(list) {
  const obj = {
    Africa: 0, 
    Americas: 0,
    Asia: 0,
    Europe: 0,
    Oceania: 0
  };
  for (let item in list){
    for (let key in obj){
      if (list[item].continent === key) obj[key]++;
    }
  }
  for (let key in obj){
    if (obj[key] === 0) return false;
  }
  return true;
}
```
```javascript
function allContinents(list) {
  const arr = [];
  for (let el in list){
    if (arr.indexOf(list[el].continent) === -1) arr.push(list[el].continent);
  }
  return arr.length === 5;
}
```
```javascript
function allContinents(list) {
  return list.some(el => el.continent === 'Africa') && list.some(el => el.continent === 'Americas') &&
            list.some(el => el.continent === 'Asia') && list.some(el => el.continent === 'Europe') &&
              list.some(el => el.continent === 'Oceania');
}
```
* Walk-up Stairs
```javascript
function stairs(n){  
  if (n < 1) return '';
  let str = '';
  let s = ' ';
  for (let i = 1; i <= n; i++){
    for (let j = 1; j <= 4 * (n - i); j++){
      str += s;
    }
    for (let k = 1; k <= i; k++){
      str += (k % 10) + s;
    }
    for (let k = i; k >= 1; k--){
      if (k !== 1) str += (k % 10) + s;
        else str += (k % 10);
    }
    if (i !== n) str += '\n';
  }
  return str;
}
```
```javascript
function stairs(n){
  const res = [];
  for(let i = 1; i <= n; i++){
    const arr = [];
    for(let j = 1; j <= 2 *(n - i); j++){
      arr.push(" ");
    }
    for(let k = 1; k <= i; k++){
      arr.push(k % 10);
    }
    for(let l = i; l >= 1; l--){
      arr.push(l % 10);
    }
    res.push(arr.join(" "));
  }
  return res.join("\n");
}
```
* Number-Star ladder
```javascript
function pattern(n){
  let output = '1';
  let star = '*';
  for (let i = 2; i <= n; i++) {
    output += `\n1${star}${i}`;
    star += '*';
  }
 return output;
}
```
```javascript
function pattern(n) {
  let output = '1';
  for (let i = 2; i <= n; i++) {
    output += '\n1' + '*'.repeat(i-1) + i;
  }
 return output;
}
```
* Coding Meetup #11 - Higher-Order Functions Series - Find the average age
```javascript
function getAverageAge(list) {
   let sum = 0;
   for (let i = 0; i < list.length; i++){
     sum += list[i].age;
   }
   return Math.round(sum/list.length);
}
```
* Coding Meetup #12 - Higher-Order Functions Series - Find GitHub admins
```javascript
function findAdmin(list, lang) {
  const arrAdmin = [];
  for (let i = 0; i < list.length; i++) {
    if (list[i].language === lang && list[i].githubAdmin === 'yes') arrAdmin.push(list[i]);
  }
  return arrAdmin;
}
```
```javascript
function findAdmin(list, lang) {
  return list.filter(el => el.language === lang && el.githubAdmin === 'yes');
}
```
* Coding Meetup #13 - Higher-Order Functions Series - Is the meetup language-diverse?
```javascript
function isLanguageDiverse(list) {
  const obj = {
    Python: 0,
    Ruby: 0,
    JavaScript: 0
  };
  const arr = [];
  for (let el in list) {
    for (let key in obj) {
      if (list[el].language === key) obj[key]++;
    }
  }
  for (let key in obj) {
    arr.push(obj[key]);
  }
  const max = Math.max(...arr);
  return arr.every(el => max / el <= 2);
}
```
```javascript
function isLanguageDiverse(list) {
  list = [
    list.filter(el => el.language==='Python').length,
    list.filter(el => el.language==='Ruby').length,
    list.filter(el => el.language==='JavaScript').length]
  const max = Math.max(...list);
  return list.every(el => max / el <= 2);
}
```
* Coding Meetup #16 - Higher-Order Functions Series - Ask for missing details
```javascript
function askForMissingDetails(list) {
  const arr = [];
  for (let el in list) {
    for (let key in list[el]) {
      if (list[el][key] === null) {
        list[el].question = `Hi, could you please provide your ${key}.`;
        arr.push(list[el]);
      }
    }
  }
  return arr;
}
```
* Coding Meetup #14 - Higher-Order Functions Series - Order the food
```javascript
function orderFood(list) {
  const obj = {};
  for (let el in list) {
    if (!obj[list[el].meal]) obj[list[el].meal] = 1;
      else obj[list[el].meal]++;
  }
  return obj;
}
```
* Coding Meetup #15 - Higher-Order Functions Series - Find the odd names
```javascript
function findOddNames(list) {
   const arr = [];
   let sum;
  for (let el in list) {
    sum = 0;
    for (let i = 0; i < list[el].firstName.length; i++) {
      sum += list[el].firstName.charCodeAt(i);
    }
    if (sum % 2) arr.push(list[el]);
  }
  
  return arr;
}
```
```javascript
findOddNames = list => {
  return list.filter(el => (el.firstName).split('').reduce((a, b) => a + b.charCodeAt(), 0) % 2);
}
```
* Coding Meetup #17 - Higher-Order Functions Series - Sort by programming language
```javascript
function sortByLanguage(list) {
  return list.sort((a,b) => 
  (a.language > b.language) ? 1 : 
  (b.language > a.language) ? -1: 
  (a.firstName > b.firstName) ? 1 : 
  (b.firstName > a.firstName)? -1: 0);
}
```
```javascript
function sortByLanguage(list) {
  return list.sort((a, b) => {
    if (a.language === b.language) return a.firstName > b.firstName ? 1 : a.firstName === b.firstName ? 0 : -1;
  return a.language > b.language ? 1 : a.language === b.language ? 0 : -1;
  });
}
```
* Multiplication table
```javascript
multiplicationTable = function(size) {
  const arrRes = [];
  for (let i = 1; i <= size; i++){
    const arr = [];
    for (let j = 1; j <= size; j++){
      arr.push(i * j);
    }
    arrRes.push(arr);
  }
  return arrRes;
}
```
* Moving Zeros To The End
```javascript
const moveZeros = function (arr) {
  let count = 0;
  const arrRes = [];
  for (let i = 0; i < arr.length; i++){
    if (arr[i] === 0) count++;
    if (arr[i] !== 0) arrRes.push(arr[i]);
  }
  for (let i = 1; i <= count; i++){
    arrRes.push(0);
  }
  return arrRes;
}
```
* Test's results
```javascript
function testResult(arr) {
  const average = +(arr.reduce((a,b)=> a + b, 0) / arr.length).toFixed(3);
   const obj = {
        "h" : 0,
        "a" : 0,
        "l" : 0
   }
    for (let el of arr){
        if (el >= 9) obj["h"]++;
        else if (el >= 7) obj["a"]++;
        else obj["l"]++;
    }        
  return (obj["a"] === 0 && obj["l"]  === 0) ? [average, obj, "They did well"] : [average, obj];     
}
```
* Dictionary from two lists
```javascript
function createDict(keys, values){
  const obj = {};
  for (let i = 0; i < keys.length; i++){
      obj[keys[i]] = values[i];
      if (i >= values.length) obj[keys[i]] = null;
  }
  return obj;
}
```
* Alternating between three values
```javascript
function f(x, cc) { 
  if (x === cc.a) return x = cc.b;
   if (x === cc.b) return x = cc.c;
    if (x === cc.c) return x = cc.a;
}
```
* Semi-Optional
```javascript
function wrap(value) {
  return {value : value}; 
}
```
* Grasshopper - Create the rooms
```javascript
const rooms = {
  room1: {name: 'A', description: 'descriptionA', completed: true},
  room2: {name: 'B', description: 'descriptionB', completed: false},
  room3: {name: 'C', description: 'descriptionC', completed: true},
}
```
* Grasshopper - Object syntax debug
```javascript
const rooms = {
  first: {
    description: 'This is the first room',
    items: {
      chair: 'The old chair looks comfortable',
      lamp: 'This lamp looks ancient'
    }
  },
  second: {
    description: 'This is the second room',
    items: {
      couch: 'This couch looks like it would hurt your back',
      table: 'On the table there is an unopened bottle of water'
    }
  }
}
```
* What's wrong with these identifiers?
```javascript
const Person = {
  '1stname': "John",
  'second-name': "Doe",
  'email@ddress': "john.doe@email.com",
  'male.female': "M"
};
```
* TV channels
```javascript
function redarr(arr) {
  const newArr = arr.sort().filter((el, i) => i === arr.indexOf(el));
  const obj = {};
  for (let i = 0; i < newArr.length; i++){
    obj[i] = newArr[i];
  }
  return obj;
}
```
* Add property to every object in array
```javascript
questions.map(el => el.usersAnswer = null);
```
```javascript
for (let i = 0; i < questions.length; i++){
  questions[i].usersAnswer = null;
}
```
* Ironman Triathlon
```javascript
function iTri(s){
  const distance = 2.4 + 112 + 26.2;
  return s === 0 ? 'Starting Line... Good Luck!' :
 s < 2.4 ? {'Swim' : `${(distance - s).toFixed(2)} to go!`} :
 s < 114.4 ? {'Bike' : `${(distance - s).toFixed(2)} to go!`} :
 s < 130.6 ? {'Run' : `${(distance - s).toFixed(2)} to go!`} :
 s < distance ? {'Run' : `Nearly there!`} : "You're done! Stop running!";
}
```
* Blood-Alcohol Content
```javascript
function bloodAlcoholContent(drinks, weight, sex, time){
  const bac = (drinks.ounces * drinks.abv * 5.14 / weight * ((sex === 'male') ? 0.73 : 0.66)) - .015 * time;
  return +bac.toFixed(4);
}
```
* Simple Fun #286: Chemistry
```javascript
function chemistry(first, second) {
  function gcd(x, y) {
    while(y) {
      let t = y;
      y = x % y;
      x = t;
    }
    return x;
  }
  const a = +first.slice(first.indexOf('(') + 1, first.indexOf(')'));
  const b = +first.slice(first.lastIndexOf('(') + 1, first.lastIndexOf(')'));
  const c = +second.slice(second.indexOf('(') + 1, second.indexOf(')'));
  const d = +second.slice(second.lastIndexOf('(') + 1, second.lastIndexOf(')'));
  
  const X = first.slice(0, first.indexOf('('));
  const Y = first.slice(first.indexOf(')') + 1, first.lastIndexOf('('));
  const Z = second.slice(0, second.indexOf('('));
  const T = second.slice(second.indexOf(')') + 1, second.lastIndexOf('('));
  
  return [`${Z}(${c/gcd(c, b)})${Y}(${b/gcd(c, b)})`,
   `${X}(${a/gcd(a, d)})${T}(${d/gcd(a, d)})`]
}
```
* What's up next?
```javascript
function nextItem(xs, item) {
  const arr = [];
  for(let el of xs){
    if(arr.length === 1) return el;
    if(el === item) arr.push(el);
  }
}
```
* Training JS #12: loop statement --for..in and for..of
```javascript
function giveMeFive(obj){
  const arr = [];
  for (let key in obj){
    if (key.length === 5) arr.push(key);
    if (obj[key].length === 5) arr.push(obj[key]);
  }
  return arr;
}
```
* Pyramid Array
```javascript
function pyramid(n) {
  const result = [];
  for (let i = 1; i <= n; i++){
    const arr = [];
    for (let j = 1; j <= i; j++){
      arr.push(1);
    }
    result.push(arr);
  }
  return result;
}
```
* Find the Capitals
```javascript
function capital(capitals){
  const arr = [];
  for (let el in capitals){
    arr.push(`The capital of ${capitals[el].state || capitals[el].country} is ${capitals[el].capital}`)
  }
  return arr;
}
```
* Coding Meetup #4 - Higher-Order Functions Series - Find the first Python developer
```javascript
function getFirstPython(list) {
  const developer = list.find(x => x.language === "Python");
  return developer ? `${developer.firstName}, ${developer.country}` : "There will be no Python developers";
}
```
```javascript
function getFirstPython(list) {
  for (let el of list){
    if (el.language === 'Python') return `${el.firstName}, ${el.country}`;
  }
  return 'There will be no Python developers';
}
```
* Coding Meetup #9 - Higher-Order Functions Series - Is the meetup age-diverse?
```javascript
function isAgeDiverse(list) {
  const obj = {
    teens: 0,
    twenties: 0,
    thirties: 0,
    forties: 0,
    fifties: 0,
    sixties: 0,
    seventies: 0,
    eighties: 0,
    nineties: 0,
    centenarian: 0
  }
  for (let el of list) {
    if (el.age >= 10 && el.age < 20) obj['teens']++;
    if (el.age >= 20 && el.age < 30) obj['twenties']++;
    if (el.age >= 30 && el.age < 40) obj['thirties']++;
    if (el.age >= 40 && el.age < 50) obj['forties']++;
    if (el.age >= 50 && el.age < 60) obj['fifties']++;
    if (el.age >= 60 && el.age < 70) obj['sixties']++;
    if (el.age >= 70 && el.age < 80) obj['seventies']++;
    if (el.age >= 80 && el.age < 90) obj['eighties']++;
    if (el.age >= 90 && el.age < 100) obj['nineties']++;
    if (el.age >= 100) obj['centenarian']++;
  }
  for (let key in obj) {
    if (obj[key] === 0) return false;
  }
  return true;
}
```
```javascript
function isAgeDiverse(list) {
  const arr = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0];
  list.map(el => {
    if (el.age >= 10 && el.age < 20) arr[0]++;
    if (el.age >= 20 && el.age < 30) arr[1]++;
    if (el.age >= 30 && el.age < 40) arr[2]++;
    if (el.age >= 40 && el.age < 50) arr[3]++;
    if (el.age >= 50 && el.age < 60) arr[4]++;
    if (el.age >= 60 && el.age < 70) arr[5]++;
    if (el.age >= 70 && el.age < 80) arr[6]++;
    if (el.age >= 80 && el.age < 90) arr[7]++;
    if (el.age >= 90 && el.age < 100) arr[8]++;
    if (el.age >= 100) arr[9]++;
  })
  return arr.every(el => el !== 0);
}
```
* Tribonacci Sequence
```javascript
function tribonacci(signature,n) {
  let arr = [];
  if (n === 0) return arr;
  if (n <= 3) return signature.slice(0, n);
  arr[0] = signature[0];
  arr[1] = signature[1];
  arr[2] = signature[2];
  for (let i = 3; i < n; i++) {
   arr[i] = arr[i - 1] + arr[i - 2] + arr[i - 3];
  }
  return arr;
}
```
```javascript
function tribonacci(signature,n){
  let arr = [];
  if (n === 0) return arr;
  if (n <= 3) return signature.slice(0, n);
  let f1 = signature[0];
  let f2 = signature[1];
  let f3 = signature[2];
  arr = [f1, f2, f3];
  for (let i = 3; i < n; i++) {
    let f4 = f1 + f2 + f3;
    arr.push(f4);
    f1 = f2;
    f2 = f3;
    f3 = f4;
  }
  return arr;
}
```
* Take a Ten Minute Walk
```javascript
function isValidWalk(walk) {
  let n = 0;
  let s = 0;
  let e = 0;
  let w = 0;
    for (let i = 0; i < walk.length; i++){
      if (walk[i] === 'n') n++;
      if (walk[i] === 's') s++;
      if (walk[i] === 'e') e++;
      if (walk[i] === 'w') w++;
    }
  return walk.length === 10 && n === s && w === e;
}
```
* Find the middle element
```javascript
const gimme = function (arr) {
  let index;
  for (let i = 0; i < arr.length; i++){
    if (arr[i] !== Math.max(...arr) && arr[i] !== Math.min(...arr)) index = i;
  }
  return index;
}
```
```javascript
const gimme = function (arr) {
  const arrSorted = [...arr].sort((a, b) => a - b);
  return arr.indexOf(arrSorted[1]);
}
```
* Highest Rank Number in an Array
```javascript
function highestRank(arr){
  const obj = {};
  let max;
  let count = 0;
  for (let el of arr) {
    if (obj[el]) obj[el]++;
      else obj[el] = 1;
  }
  console.log(obj);
  for (let key in obj) {
    if (obj[key] >= count) {
      count = obj[key];
      max = +key;
    }
  }
  return max;
}
```
```javascript
function highestRank(arr){
  const obj = {};
  for (let el of arr) {
    if (obj[el]) obj[el]++;
      else obj[el] = 1;
  }
  let max = Math.max(...Object.values(obj));
  let keyMax = 0;
  for (let key in obj) {
    if (obj[key] === max && keyMax < key) keyMax = +key;
  }
  return keyMax;
}
```
* The Vowel Code
```javascript
function encode(string) {
  const obj = {
    a : 1,
    e : 2, 
    i : 3,
    o : 4,
    u : 5
  }
  return string.replace(/[aeiou]/g, v => {
    return obj[v];
  });
}

function decode(string) {
  const obj1 = {
    1 : 'a',
    2 : 'e', 
    3 : 'i',
    4 : 'o',
    5 : 'u'
  }
  return string.replace(/[1-5]/g, v => {
    return obj1[v];
  });
}
```
* Regexp Basics - is it a letter?
```javascript
String.prototype.isLetter = function() {
 return /^[a-z]$/i.test(this);
}
```
* Regexp Basics - is it a vowel?
```javascript
String.prototype.vowel = function() {
  return /^[aouie]$/i.test(this);
}
```
* Exclamation marks series #5: Remove all exclamation marks from the end of words
```javascript
function remove(s){
  return s.replace(/\b!+/g, '');
}
```
* Number of Decimal Digits
```javascript
const digits = n => n.toString().length;
```
* Take the Derivative
```javascript
const derive = (coefficient,exponent) => `${coefficient * exponent}x^${exponent - 1}`;
```
* Responsible Drinking
```javascript
function hydrate(s) {
  const arr = s.split(' ');
  let str = '123456789';
  let n = 0;
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < str.length; j++) {
      if (arr[i] === str[j]) n += +arr[i];
    }
  }
  return n === 1 ? `1 glass of water` : `${n} glasses of water`;
}
```
```javascript
function hydrate(s) {
  const digits = s.replace(/\D/g, '').split('');
  const n = digits.reduce((a, b) => a + +b, 0);
  return n === 1 ? `1 glass of water` : `${n} glasses of water`;
}
```
* Dubstep
```javascript
const songDecoder = song => song.replace(/(WUB)+/g, ' ').trim();
```
* Smallest Difference
```javascript
function smallestDiff(arr1, arr2) {
  if (arr1.length === 0 && arr2.length === 0) return -1;
  if (arr1.length === 0) return Math.min(...arr2);
  if (arr2.length === 0) return Math.min(...arr1);
  let min = Number.MAX_VALUE;
  for (let i = 0; i < arr1.length; i++) {
    for (let j = 0; j < arr2.length; j++) {
      if (Math.abs(arr1[i] - arr2[j]) < min) min = Math.abs(arr1[i] - arr2[j]);
    }
  }
  return min;
}
```
* noobCode 01: SUPERSIZE ME.... or rather, this integer!
```javascript
function superSize(num) {
  const arr = String(num).split('');
  const arrSorted = arr.sort((a, b) => b - a);
  return +arrSorted.join('');
}
```
* Simple Sentences
```javascript
function makeSentence(parts) {
  let res = '';
  res = parts.join(' ').replace(/\./g, '').replace(/\s,/g, ',').trim();
  return res + '.';
}
```
* Counting Duplicates
```javascript
function duplicateCount(text) {
  const str = text.toLowerCase();
  const obj = {};
  for (let el of str) {
    if (obj[el]) obj[el]++;
      else obj[el] = 1;
  }
  let count = 0;
  for (let key in obj) {
    if (obj[key] > 1) count++;
  }
  return count;
}
```
```javascript
function duplicateCount(text) {
  const arr = text.toLowerCase().split('');
  const res = arr.filter((el, i) => i !== arr.indexOf(el) && i === arr.lastIndexOf(el));
  return res.length;
}
```
* altERnaTIng cAsE <=> ALTerNAtiNG CaSe
```javascript
String.prototype.toAlternatingCase = function () {
  let res = "";
    for (let i = 0; i < this.length; i++) {
      if (this[i] === this[i].toUpperCase()) 
        res += this[i].toLowerCase();
      else 
        res += this[i].toUpperCase();
    }
    return res;
}
```
* Rock Off!
```javascript
function solve(a, b) {
  let sA = 0, sB = 0;
  const l = a.length;
  for (let i = 0; i < l; i++){
    if (a[i] > b[i]) sA++;
    if (a[i] < b[i]) sB++;
  }
  return sA > sB ? `${sA}, ${sB}: Alice made "Kurt" proud!` : 
         sA < sB ? `${sA}, ${sB}: Bob made "Jeff" proud!` :
         `${sA}, ${sB}: that looks like a "draw"! Rock on!`;
}
```
* Number of People in the Bus
```javascript
const number = function(busStops){
  let result = 0;
  for (let i = 0; i < busStops.length; i++) {
    result += busStops[i][0] - busStops[i][1];
  }
  return result;
}
```
* Push a hash/an object into array
```javascript
const items = [];
items.push({a: "b", c: "d"});
```
* Decode Morse
```javascript
function decode(str) {
  if (str === '') return '';
  const dict = {
    a: ".-",
    b: "-...",
    c: "-.-.",
    d: "-..",
    e: ".",
    f: "..-.",
    g: "--.",
    h: "....",
    i: "..",
    j: ".---",
    k: "-.-",
    l: ".-..",
    m: "--",
    n: "-.",
    o: "---",
    p: ".--.",
    q: "--.-",
    r: ".-.",
    s: "...",
    t: "-",
    u: "..-",
    v: "...-",
    w: ".--",
    x: "-..-",
    y: "-.--",
    z: "--..",
    1: ".----",
    2: "..---",
    3: "...--",
    4: "....-",
    5: ".....",
    6: "-....",
    7: "--...",
    8: "---..",
    9: "----.",
    0: "-----",
  };
  
  const arr = str.split(' ');
  let res = "";
  for (let el of arr){
    for (let key in dict) {
      if (el === dict[key]) res += key;
    }
    if (el === '') res += ' ';
  }
  return res;
}
```
* Your order, please
```javascript
function order(words){
  if (!words.length) return '';
  const arrOfWords = words.split(' ');
  const arrOfInd = words.match(/\d/g);
  const result = [];
  for (let i = 1; i <= arrOfInd.length; i++) {
    const index = arrOfInd.indexOf(`${i}`);
    result.push(arrOfWords[index]);
  }
  return result.join(' ');
}
```
```javascript
function order(words){
  const arr = words.split(' ');
  const arrSorted = [];
  for(let i = 0; i <= arr.length; i++) {
    for(let j = 0; j < arr.length; j++) {
      if(arr[j].indexOf(i) >= 0) {
        arrSorted.push(arr[j]);
      }
    }
  }
  return arrSorted.join(' ');
}
```
* Find the lucky numbers
```javascript
const filterLucky = x => {
  return x.filter(el => el.toString().includes(7));
}
```
* Simple Fun #152: Invite More Women?
```javascript
const inviteMoreWomen = L => L.reduce((ac, el) => ac + el, 0) > 0;
```
* Row Weights
```javascript
function rowWeights(array) {
  let first = array.filter((el, i) => i % 2 === 0).reduce((ac, el) => ac + el, 0);
  let second = array.filter((el, i) => i % 2).reduce((ac, el) => ac + el, 0);
  return [first, second];
}
```
* Enumerable Magic #5- True for Just One?
```javascript
function one(arr, fun) {
  return arr.filter(fun).length === 1;
}
```
* Simple validation of a username with regex
```javascript
const validateUsr = username => /^[a-z0-9\_]{4,16}$/.test(username);
```
* Show multiples of 2 numbers within a range
```javascript
function multiples(s1,s2,s3){
  const arr = [];
  for (let i = 1; i < s3; i++) {
    if (i % s1 === 0 && i % s2 === 0) arr.push(i);
  }
  return arr;
}
```
* Short Long Short
```javascript
function solution(a, b) {
  return a.length > b.length ? b + a + b : a + b + a;
}
```
* Valid Phone Number
```javascript
function validPhoneNumber(phoneNumber) {
  const format = '() -'
  const res = phoneNumber.replace(/[0-9]/g, '');
  return format === res;
}
```
* Array element parity
```javascript
function solve(arr) {
  const arrFiltered = arr.filter(el => arr.indexOf(-el) === -1);
  return arrFiltered[0];
}
```
* A bugs trilogy: Episode 1 - "Let Math.Random(); decide your future"
```javascript
function yourFutureCareer() {
  const career = Math.random();
  if (career <= 0.32) return 'FrontEnd Developer';
  else if (career <= 0.65) return 'BackEnd Developer';
  else return 'Full-Stack Developer';
}
```
* Polish alphabet
```javascript
function correctPolishLetters (string) {
    return string.replace(/ą/g,'a')
    .replace(/ć/g,'c')
    .replace(/ę/g,'e')
    .replace(/ł/g,'l')
    .replace(/ń/g,'n')
    .replace(/ó/g,'o')
    .replace(/ś/g,'s')
    .replace(/ź/g,'z')
    .replace(/ż/g,'z');
  }
```
* Ones and Zeros
```javascript
const binaryArrayToNumber = arr => {
  return parseInt(arr.join(''), 2);
}
```
* Training JS #29: methods of arrayObject---concat() and join()
```javascript
function bigToSmall(arr) {
  return [].concat(...arr).sort((a, b) => b - a).join('>');
}
```
```javascript
const bigToSmall = arr => arr.reduce((acc, cur) => acc.concat(cur)).sort((a, b) => b - a).join('>');
```
* Add new item (collections are passed by reference)
```javascript
function addExtra(listOfNumbers){
  return listOfNumbers.concat(1);
}
```
```javascript
function addExtra(listOfNumbers) {
    return [...listOfNumbers, 1];
}
```
* Longest vowel chain
```javascript
function solve(s){
  const str = 'aouei';
  let count = 0;
  let max = 0;
  for (let i = 0; i < s.length; i++) {
    if (str.includes(s[i])) {
      count++; 
      if (count > max) {
          max = count;
      }
    }
    else {
      count = 0;
    }
  }
  return max;
}
```
```javascript
function solve(str) {
    let vowels = [],
        counter = 0;
    for (let char of str) {
        if ('aeiou'.includes(char))
            vowels.push(char);
        else {
            if (vowels.length > counter) counter = vowels.length;
            vowels = [];
        }
    }
    if (vowels.length === str.length) counter = vowels.length;
    return counter;
}
```
* Sorting Arrays
```javascript
function sortArray(a1, a2) {
  let res = [];
  for (let i = 0; i < a1.length; i++) {
     for (let j = 0; j < a2.length; j++) {
        if (a1[i][0] === a2[j][0]) {
         res.push(a2[j])
        }
     }
  }
    return res;
}
```
* Sort with a sorting array
```javascript
function sort(initialArray, sortingArray) {
  const arr = [];
  for (let i = 0; i < sortingArray.length; i++) {
    arr[sortingArray[i]] = initialArray[i];
  }
  return arr;
}
```
* Freudian translator
```javascript
const toFreud = str => str.replace(/\S+/g, 'sex');
```
```javascript
const toFreud = str => str.replace(/[^ ]+/g, 'sex');
```
```javascript
function toFreud(string) {
  if (string.length === 0) return "";
  const arr = string.split(' ');
  return arr.map(el => 'sex').join(' ');
}
```
* A Rule of Divisibility by 7
```javascript
function seven(m) {
  let count = 0;
    while (m > 99) {
      m = parseInt(m / 10) - (2 * (m % 10));
      count++;
    }
  return [m, count];
}
```
* Training JS #11: loop statement --break,continue
```javascript
function grabDoll(dolls){
  const bag=[];
  for (let i = 0; i < dolls.length; i++) {
    if (dolls[i] !== "Hello Kitty" && dolls[i] !== "Barbie doll") continue;
    bag.push(dolls[i]);
    if (bag.length === 3) break;
  }
  return bag;
}
```
* Find the missing element between two arrays
```javascript
function findMissing(arr1, arr2) {
  const newArr1 = arr1.sort((a, b) => a - b);
  const newArr2 = arr2.sort((a, b) => a - b);
  for (let i = 0; i < newArr1.length; i++) {
    if (newArr2[i] !== newArr1[i])
      return newArr1[i];
  }
}
```
* Reverse List Order
```javascript
function reverseList(list) {
  const rev = [];
  for (let i = list.length - 1; i >= 0 ; i--) {
    rev.push(list[i]);
  }
  return rev;
}
```
```javascript
const reverseList = (list) => list.reverse();
```
* A Gift Well Spent
```javascript
const buy = function(x, arr){
  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] + arr[j] === x)
        return [i, j];
    }
  }
  return null;
}
```
* Validate my Password
```javascript
function validPass(pass){
  if (pass.length <= 3 || pass.length >= 20) {
    return 'INVALID';
  }
  let str = pass.replace(/[^0-9a-zA-Z]/g, '');
  return (/[0-9]/g.test(str) && /[a-zA-Z]/g.test(str) && str === pass) ? 'VALID' : 'INVALID';
}
```
```javascript
function validPass(password){
  return /(?=.+[a-z])(?=.+\d)^[a-z\d]{3,20}$/i.test(password) ? 'VALID' : 'INVALID';
}
```
```javascript
function validPass(password) {
  const t1 = /^\w{3,20}$/.test(password);
  const t2 = /\d/.test(password);
  const t3 = /[a-zA-Z]/.test(password);
  return t1 && t2 && t3 ? "VALID" : "INVALID";
}
```
* Are arrow functions odd?
```javascript
function odds(values){
  return values.filter(el => el % 2 !== 0);
}
```
* Disemvowel Trolls
```javascript
function disemvowel(str) {
  return str.replace(/[aouei]/ig, '');
}
```
* List Filtering
```javascript
function filter_list(l) {
  return l.filter(el => typeof(el) === 'number');
}
```
