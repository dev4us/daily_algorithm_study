# 7kyu_01_Jaden_Casing_Strings

## Q. 
Will Smith의 아들인 Jaden Smith는 The Karate Kid (2010)와 After Earth (2013)와 같은 영화에 출연한 스타입니다. Jaden는 그만의 철학 일부를 Twitter를 통해 공유하고는 합니다. 

특이한 점은 그는 트위터에 글을 쓸 때 거의 모든 단어를 대문자로 쓰는 것으로 유명합니다.

당신의 임무는 문자열을 Jaden Smith가 쓴 방식으로 변환하는 것입니다. 문자열은 Jaden Smith의 실제 인용문이지만 원래 입력 한 것과 같은 방식으로 대문자로 표기되지 않았습니다.

예:

Not Jaden-Cased: "How can mirrors be real if our eyes aren't real"

Jaden-Cased:     "How Can Mirrors Be Real If Our Eyes Aren't Real"

- - -
  
## A1.
```javascript
String.prototype.toJadenCase = function () {
  var splitArray = this.split(' ');
  var result = "";
    
  for(var i = 0; i < splitArray.length; i++){
    result += splitArray[i].charAt(0).toUpperCase() + splitArray[i].substring(1, splitArray.length) + ' ';
  }
    
  return result = result.slice(0, -1);
};
```

## E1.
