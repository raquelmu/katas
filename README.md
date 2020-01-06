###Numbers to Letters

```javascript
function switcher(x){
const alphabet = ["z" ,"y" ,"x" ,"w" ,"v" ,"u" ,"t" ,"s" ,"r" ,"q" ,"p" ,"o" ,"n" ,"m" ,"l" ,"k" ,"j" ,"i" ,"h" ,"g" ,"f" ,"e" ,"d" ,"c" ,"b" ,"a","!" ,"?" ," "];
  let word = "";
  for(let i = 0; i < x.length; i++){
    word = word + alphabet[parseInt(x[i])-1];
  }
  return word;
}
```
###Remove first and last character

```javascript
function removeChar(str){
 let word = "";
 for(let i = 1; i<str.length-1; i++){
  word = word + str[i];
 }
  return word;
}
```
###Vowel count

```javascript
function getCount(str){
  var vowelsCount = 0;
  for(let i = 0; i < str.length; i++){
    if(str[i] === "a" || str[i] === "e"|| str[i] === "i"|| str[i] === "o"|| str[i] === "u"){
    vowelsCount += 1;
    }
  } 
  return vowelsCount;
}
```

###Sum mixed array  

```javascript
function sumMix(x){
  let sumCount = 0;
  for(let i = 0; i < x.length; i++){
  sumCount += parseInt(x[i]);
  }
  return sumCount;
}
```
###Count positives / Sum of negatives

```javascript
function countPositivesSumNegatives(input) {
  if (input == null || input.length == 0){
    return [];
  }
  let newArray = [0,0];
  for (let i = 0; i < input.length; i++) {
    if(input[i] > 0){
    newArray[0] += 1;
    }
    else{
    newArray[1] += input[i];
    }
  }
  return newArray;
}
```

###Get the mean of an array

```javascript
function getAverage(marks){
  let sumaNotas = 0;
  let notaFinal = 0;
  let notaMedia = 0;

  for(let i = 0; i < marks.length; i++){
    sumaNotas += marks[i];
  }

  notaFinal = sumaNotas / marks.length;
  notaMedia = Math.floor(notaFinal);
  return notaMedia;
}
```
###Find numbers which are divisible by given number

```javascript
function divisibleBy(numbers, divisor){
  let correctNumbers = [];
  for (let i = 0; i < numbers.length; i++){
     if(numbers[i] % divisor === 0){
      correctNumbers.push(numbers[i]);
      }
  }
  return correctNumbers;
}
```

###List Filtering

```javascript
function filter_list(l) {
  let numbers = [];
  for(let i = 0; i < l.length; i++){
    if(l[i] >= 0 && typeof l[i] === "number"){
    numbers.push(l[i]);
    }
  }
  return numbers;
}
```

###Credit Card Mask


```javascript
function maskify(cc) {
  let newString = "";
  let finalString = "";
  if(cc.length > 4){
    for(let i = 0; i < cc.length-4; i++){
      newString += "#";
    }
    finalString = newString + cc.slice(cc.length-4, cc.length);
    return finalString;
  }
  else{
  return cc;
  }
}
```

###Flatten


```javascript
function flatten (array){
  let newArray = [];
  for (let i = 0; i < array.length; i++){
    if(typeof array[i] === "object"){
      for (let x= 0; x < array[i].length; x++){
        newArray.push(array[i][x]);
      }
    }
    else{
      newArray.push(array[i]);
    }
  }
  return newArray;
}

```


###Square Every Digit


```javascript
function squareDigits(num){
  let result = "";
  let nums_string = num.toString()
  for(let i = 0; i < nums_string.length; i++){
    result += (nums_string[i] * nums_string[i]);
  }
  result = parseInt(result);
  return result
}
```