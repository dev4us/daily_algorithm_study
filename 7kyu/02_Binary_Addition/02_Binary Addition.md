## **7kyu_02_Binary_Addition**

## Qusetion. 
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.
<br /><br />
두 개의 숫자를 함께 덧셈하고 그 합계를 이진수로 반환하는 함수를 구현한다. 변환은 덧셈 이전 또는 이후에 수행할 수 있다.

반환된 이진수는 문자열이어야 한다.
  
## Answer.
```javascript
function addBinary(a,b) {
 return (a + b).toString(2);
}
```

## Solution.
```javascript
function addBinary(a,b){
  return (a+b).toString(2)
}
```

