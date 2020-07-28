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