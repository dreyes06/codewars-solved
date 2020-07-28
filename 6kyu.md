##1 Persistent Bugger

Problem: Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

Example:

 persistence(39) === 3 // because 3*9 = 27, 2*7 = 14, 1*4=4
                       // and 4 has only one digit

 persistence(999) === 4 // because 9*9*9 = 729, 7*2*9 = 126,
                        // 1*2*6 = 12, and finally 1*2 = 2

 persistence(4) === 0 // because 4 is already a one-digit number

 Solution: 
 function persistence(num) {
   let i = 0
   while(num.toString().length !==1){
   num = num.toString().split('').reduce((a, b) => a * b);
   i++
   }
   return i
}
///////////////////////////////////////

##2 Who Likes It?

Problem: You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement a function likes :: [String] -> String, which must take in input array, containing the names of people who like an item. It must return the display text as shown in the examples:

likes [] // must be "no one likes this"
likes ["Peter"] // must be "Peter likes this"
likes ["Jacob", "Alex"] // must be "Jacob and Alex like this"
likes ["Max", "John", "Mark"] // must be "Max, John and Mark like this"
likes ["Alex", "Jacob", "Mark", "Max"] // must be "Alex, Jacob and 2 others like this"
For 4 or more names, the number in and 2 others simply increases.

Solution: 
function likes(names) {
  if(names.length === 0){
     return 'no one likes this'
   }for(let i = 0;i < names.length;i++){
   if(names.length === 1){
     return names[i] + ' likes this'
   }else if(names.length === 2){
     return names[i] + ' and ' + names[i+1] + ' like this'
   }else if(names.length === 3){
     return names[i] + ', ' + names[i+1] + ' and ' + names[i+2] + ' like this'
   }else{
     return names[i] + ', ' + names[i+1] + ' and ' + (names.length-2) + ' others like this' 
   }
 }
}
///////////////////////////////////////