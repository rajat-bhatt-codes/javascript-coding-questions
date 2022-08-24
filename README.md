
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
