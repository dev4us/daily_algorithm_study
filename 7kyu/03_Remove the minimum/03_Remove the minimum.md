## **7kyu_03_Remove the minimum**

## Question. 
The museum of incredible dull things wants to get rid of some exhibitions. Miriam, the interior architect, comes up with a plan to remove the most boring exhibitions. She gives them a rating, and then removes the one with the lowest rating.

However, just as she finished rating all exhibitions, she's off to an important fair, so she asks you to write a program that tells her the ratings of the items after one removed the lowest one. Fair enough.

Task
Given an array of integers, remove the smallest value. Do not mutate the original array/list. If there are multiple elements with the same value, remove the one with a lower index. If you get an empty array/list, return an empty array/list.

Don't change the order of the elements that are left.

**Examples**

removeSmallest([1,2,3,4,5]) = [2,3,4,5]

removeSmallest([5,3,2,1,4]) = [5,3,2,4]

removeSmallest([2,2,1,2,1]) = [2,2,2,1]

<br /><br />
놀라울 정도로 따분한 박물관에서는 몇몇 전시회를 제외시키고 싶어했습니다.
실내구조 건축가인 'Miriam'은 그 중 제일 지루한 전시회를 제외시키자는 생각을 했고, 그녀는 전시회에 점수를 매기기 시작했으며 가장 낮은 점수를 받은 전시회는 제외시켰습니다.

그녀가 전시회에 등급을 매긴 것처럼 당신에게 가장 낮은 점수의 전시회를 제외시킨 뒤에 그 전시회들의 등급을 알려주는 프로그램을 개발해달라고 요청했습니다. 어쩔 수 없죠

Task

1. 정수의 배열을 지정하여 최소 값을 제거하세요.
2.  원본 배열을 직접 수정하지 마세요. 
3. 값이 동일한 요소가 중복으로 존재한다면 낮은 key를 가진 요소를 제거하세요. 
4. 빈 배열 또는 리스트를 얻게된다면 그대로 반환해주세요.
5. 원소의 순서를 임의로 변경하지 마세요.

**예:**

removeSmallest([1,2,3,4,5]) = [2,3,4,5]

removeSmallest([5,3,2,1,4]) = [5,3,2,4]

removeSmallest([2,2,1,2,1]) = [2,2,2,1]

## Answer.
```javascript
function removeSmallest(numbers) {
  var arr = numbers;
  arr = arr.slice(0);
  
  arr.splice(arr.indexOf(Math.min.apply(null, arr)), 1);
  return arr;
}
```

## Solution.
```javascript
function removeSmallest(numbers) {
  let indexOfMin = numbers.indexOf(Math.min(...numbers));
  return [...numbers.slice(0, indexOfMin), ...numbers.slice(indexOfMin + 1)];
}
```

