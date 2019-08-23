## **7kyu_04_Highest and Lowest**

## Question. 
In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

**Examples**

highAndLow("1 2 3 4 5");  // return "5 1"

highAndLow("1 2 -3 4 5"); // return "5 -3"

highAndLow("1 9 3 4 -5"); // return "9 -5"

<br /><br />
이번 문제에서는 최소값과 최대값 사이에 공백을 주어 문자열로 반환해보세요.


**예:**

highAndLow("1 2 3 4 5");  // return "5 1"

highAndLow("1 2 -3 4 5"); // return "5 -3"

highAndLow("1 9 3 4 -5"); // return "9 -5"

## Answer.
```javascript
function highAndLow(numbers){
  var arrayNums = numbers.split(" ");
  
  return Math.max.apply(null, arrayNums) + " " + Math.min.apply(null, arrayNums);
}
```

## Popular Solution.
```javascript
function highAndLow(numbers){
  numbers = numbers.split(' ').map(Number);
  return Math.max.apply(0, numbers) + ' ' + Math.min.apply(0, numbers);
}
```

