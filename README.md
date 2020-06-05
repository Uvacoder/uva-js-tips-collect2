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
    obj[s[i]] = String.fromCharCode(s[i])
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