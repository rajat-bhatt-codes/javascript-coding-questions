
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
