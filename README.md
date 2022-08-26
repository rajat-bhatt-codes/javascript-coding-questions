
# Javascript Coding Questions


### Question 1: Capitalize First Letter Of Each Word Using JavaScript
For example: 

input: "there is a new book strore"

output: "There Is A New Book Strore"  

```javascript
const capitalizeString = (str) => {
  
  //split the string into arrya of strings
  let tempArr = str.split(" ")
  let resArr = []

  tempArr.forEach((item) => {
    resArr.push(item[0].toUpperCase() + item.slice(1, item.length))
  })

  //join the array to a string
  console.log(resArr.join(" "))
}

capitalizeString("hi my name is rajat")

```
___

### Question 2: Reverse a string Using JavaScript
For example: 

input: "hi my name is rajat"

output: tajar si eman ym ih  

```javascript

function reverseStr(str){
  let result =""
  for(let i=str.length-1; i>=0; i--){
   result += str[i]
}
  return result;
}

const x = reverseStr("hi my name is rajat")
console.log(x)

```
___

### Question 3: Count all the vowels in given string Using JavaScript
For example: 

input: "hi my name is rajat"

output: 6  

input: "aeiou"

output: 5 

```javascript

function countVowel(str){
  let count = 0
  let vowels = ['a','e','i','o','u']

  for(let i=0; i<str.length; i++){
    if(vowels.includes(str[i].toLowerCase())){
      count ++;
    }
  }
  return count
}

const x = countVowel("hi my name is rajat")
console.log(x)

```
___
### Question 4: Remove duplicate from array Using JavaScript
For example: 

input: [1, 2, 33, 4, 5, 4, 2, 33]

output: [1, 2, 33, 4, 5]

```javascript
//first solution
let arr =[1, 2, 33, 4, 5, 4, 2, 33]

console.log([... new Set(arr)])
```

```javascript
//Second solution
function removeDuplicate(arr) {
  let tempArr = []
  arr.forEach((item) => {
    if (!tempArr.includes(item)) {
      tempArr.push(item)
    }
  })
  return tempArr
}

const x=removeDuplicate([1, 2, 33, 4, 5, 4, 2, 33])
console.log(x)

```
___
### Question 5: Find max and in values in a given array
For example: 

input: [1, 2, 33, 4, 5, 4, 2, 33]

output: max=33, min=1

```javascript

function findMaxMin(arr) {
  let max = -100000;
  let min = 100000;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i]
    } else if (arr[i] < min) {
      min = arr[i]
    }
  }
  return [max, min]
}
const result =  findMaxMin( [1, 144, 55, 0]) 
console.log(`max = ${result[0]} & min = ${result[1]}`)

```
___
### Question 6: FizzBuzz Problem( if number is divided by 3 print fizz or if number is divided by 5 print buzz or if number is divided by 5 & 3 print fizzbuzz)
For example: 

```javascript
function fizzBuzz(n){
  for(let i=1; i<=n; i++){
    if(i%3 === 0 && i%5 === 0){
      console.log("FizzBuzz")
    }else if(i%3 === 0){
      console.log("Fizz")
    }else if(i%5 === 0){
      console.log("Buzz")
    }else{
      console.log(i)
    }
  }
}

fizzBuzz(15)
```
___

### Question 7: Reverse a String without Changing Position of words
For example: 
input: hi my name is rajat

output: ih ym eman si tajar

```javascript
function reverseStr(str){
  let tempArr = str.split(" ")
  const resultArr =tempArr.map(item =>{
    return item.split("").reverse().join("")
  })
  return resultArr.join(" ")
}

const x = reverseStr("hi my name is rajat")
console.log(x)
```
___
