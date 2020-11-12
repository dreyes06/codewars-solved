##1 Sum of two lowest positive integers

Problem: Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 positive integers. No floats or non-positive integers will be passed.

For example, when an array is passed like [19, 5, 42, 2, 77], the output should be 7.

[10, 343445353, 3453445, 3453545353453] should return 3453455.

Solution: function sumTwoSmallestNumbers(numbers) {  
 let newNumbers = numbers.sort((a, b) => a - b)
 return newNumbers[0] + newNumbers[1]
}
///////////////////////////////////////

##2 Reverse Words

Problem: Complete the function that accepts a string parameter, and reverses each word in the string. All spaces in the string should be retained.

Example: "This is an example!" ==> "sihT si na !elpmaxe"
         "double  spaces"      ==> "elbuod  secaps"

Soluton: function reverseWords(str) {
  return str.split('').reverse().join('').split(" ").reverse().join(" ")
}
///////////////////////////////////////

##3 Highest and Lowest

Problem: In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

Example:

highAndLow("1 2 3 4 5");  // return "5 1"
highAndLow("1 2 -3 4 5"); // return "5 -3"
highAndLow("1 9 3 4 -5"); // return "9 -5"

Solution: 
function highAndLow(numbers){
let newNumbers = numbers.split(' ')
  
 let mappedNumbers = newNumbers.map((val) => {return +val})

return Math.max(...mappedNumbers) + ' ' +  Math.min(...mappedNumbers)
}
///////////////////////////////////////

##4 List Filtering

Problem: In this kata you will create a function that takes a list of non-negative integers and strings and returns a new list with the strings filtered out.

Example:
filter_list([1,2,'a','b']) == [1,2]
filter_list([1,'a','b',0,15]) == [1,0,15]
filter_list([1,2,'aasf','1','123',123]) == [1,2,123]

Solution: 
function filter_list(l) {
 return l.filter(v => typeof v == "number")
}
///////////////////////////////////////

##5 Isograms

Problem: An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

Example: 
isIsogram("Dermatoglyphics") == true
isIsogram("aba") == false
isIsogram("moOse") == false // -- ignore letter case

Solution:
function isIsogram(str){
  let letters = str.toLowerCase().split('')
  let checkLetters = []
  
  letters.forEach(function(letter){
    if(checkLetters.indexOf(letter) === -1) {
      checkLetters.push(letter)
    }
  })
  return letters.length === checkLetters.length ? true : false
}
///////////////////////////////////////

##You're a Square

Problem: Given an integral number, determine if it's a square number.

Examples:
-1  =>  false
 0  =>  true
 3  =>  false
 4  =>  true
25  =>  true
26  =>  false

Solution: 
const perfectSquare = (n) => {
  return Math.sqrt(n) % 1 === 0;
}