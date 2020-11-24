console.log('Problem Solving Q: 1 ');

/* Longest Word */

/*  
Have the function LongestWord(sen) take the sen parameter being passed and return the largest word in the string. If there are two or more words that are the same length, return the first word from the string with that length. Ignore punctuation and assume sen will not be empty.
*/

function LongestWord(sen) {
  // check if sen is empty string
  if(sen.length === 0){
    // return 'there are 0 words'
    return 'there are 0 words'
  }

  // the initial value for the output
  let output = ''; // 'lol'

  // Process
  // convert the sen (string) to an array (have each word alone)
  const words = sen.split(' '); // ["lol", 'a', "time"]
  // iterate over the array (words)
  for (let index = 0; index < words.length; index++) {
    // check if the element (the current word) the longest word till now or not
    if (words[index].length > output.length) {
      // make the output (longest world) equal current world
      output = words[index];
    }
  }
  // return the longest wor
  return output;
}

/* 
Examples:
LongestWord('lol time'); // => 'time'
LongestWord('I love cats'); // => 'love'
LongestWord('coding is awesome'); // => 'awesome'
LongestWord('hello world'); // => 'hello'
*/



console.log('Problem Solving Q: 2 ');

function LongestWord_2 (sen) { 
  sen=sen.replace(/[^a-zA-Z ]/ig,'')
  words = sen.split(" ")
  LongestWord_2 = words[0]
  for (i = 0; i<words.length; i ++) {
  	if (words[i].length > LongestWord_2 .length) {
  	  LongestWord_2 = words[i]	
  	}
  }
 return LongestWord_2
}

console.log('Problem Solving Q: 3 ');


function firstReverse(str) {
  return.str.split('').revers().join('');
}



/* 
Examples:
firstReverse('I Love Code'); // => 'edoC evoL I'
firstReverse('Hello World'); // => 'dlroW olleH'
firstReverse('How are you?'); // => '?uoy era woH'
*/

function usernameValidation(str) {


console.log('Problem Solving Q: 4 ');


if (str.length < 4 || str.length > 25) {
  return false;
}
if (!str[0].match(/[a-z]/i)) {
  return false;
}
if (!str.match(/^[0-9a-zA-Z_]+$/)) {
  return false;
}
if (str[str.length -1] === '_') {
  return false;
}
return true;
}



console.log('Problem Solving Q: 5 ');
function FindIntersection(strArr){
  let firstString = strArr[0]
  let secondString = strArr[1]
  let firstElementArray = []
  let secondElementArray = []
 
  firstString.split(',').map((oneNumber) => {
    firstElementArray.push(Number(oneNumber))
  })
  secondString.split(',').map((oneNumber) => {
    secondElementArray.push(Number(oneNumber))
  })

  
  let myAnswer = (secondElementArray.filter(e =>firstElementArray.includes(e))).toString()
  
  
  if(!myAnswer){
    return "false"
  } else  {
    return myAnswer; 
  }
}
document.getElementById("displayAnswer").innerHTML = FindIntersection(strArr);





console.log('Problem Solving Q: 6');



function evenOrNot(num) {
 if (mum %2==0){return true}
 return false;
}

/* 
Examples:
evenOrNot(1) // => false
evenOrNot(2) // => true
evenOrNot(5) // => false
evenOrNot(99) // => false
evenOrNot(0) // => true
*/

console.log('Problem Solving Q: 7');

function SumOddNumber(numbers) {

let sum =0;

  let oddNumbers = []

  for (let i =0; i < numbers.length; i++){
    if (numbers[i] % 2 !== 0){
      oddNumbers.push(numbers[i])
    }
  }
  sum+=oddNumbers[i];
  return sum;
};

