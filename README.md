
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
### Question 8: Print fibonaccci series
For example: 
input: 10

output:  0, 1,  1,  2,  3, 5, 8, 13, 21, 34

```javascript
//fibonacci series
function fibonacci(n) {
  let arr = [0, 1]
  for (let i = 2; i < n; i++) {
    arr.push(arr[i - 2] + arr[i - 1])
  }
  return arr;
}
const res = fibonacci(10)
console.log(res)
```
___
### Question 9: wap to give sample output
For example: 
input: [1, 2, 3, 4, 5]

       [2, 3, 4]

output: [3, 5, 7, 4]

```javascript
let x = [1, 2, 3, 4, 5]
let y = [2, 3, 4, 12, 15, 0, 3]

let result = []

if (x.length > y.length) {
  for (let i = 0; i < y.length; i++) {
    result.push(x[i] + y[i])
  }
  let arr = x.slice(result.length, x.length)
  result.push(...arr)
} else {
  for (let i = 0; i < x.length; i++) {
    result.push(x[i] + y[i])
  }
  let arr = y.slice(result.length, y.length)
  result.push(...arr)
}

console.log(result)
```
___

