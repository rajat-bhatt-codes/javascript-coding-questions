
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


## Deployment

To deploy this project run

```bash
  npm run deploy
```

