# JavaScript6

## **✅ 최대값 for문**

### 1. 기본 문법

```jsx
for (초기값; 조건식; 증감식) {
  실행문;
}
```

### 2. 배열의 최대값 찾기

```jsx
var arr = [30, 40, 60];
var max = 0;

for (var i = 0; i < arr.length; i++) {
  if (max < arr[i]) {
    max = arr[i];
  }
}

document.write(max); // 60
```

## **✅ 함수 (Function)**

### 특징

- `return` 문은 있을 수도 있고 없을 수도 있음.
- 함수를 정의하는 방법: **선언문**, **표현식**, **Function 생성자**, **매개변수 활용**.

### 1. 함수 선언문

```jsx
function 함수명() {
  실행문;
  return;  // 선택적
}
```

### 2. 함수 표현식

```jsx
const add2 = function (a, b) {
  return a + b;
};
document.write(add2(5, 6));  // 11
```

### 3. 생성자 함수

```jsx
var add3 = new Function('a', 'b', 'return a * b');
document.write(add3(4, 3));  // 12
```

### 4. 최대값을 구하기 함수 예시

```jsx
function max1(ele) {
  let max = 0;
  for (var i = 0; i < ele.length; i++) {
    if (max < ele[i]) {
      max = ele[i];
    }
  }
  return max;
}

const arr = [10, 20, 30, 40, 50];
document.write(max1(arr));  // 50
```

### 5. 매개변수 있는 함수

**1) 함수 선언문**

```jsx
function add(a, b) {
  return a + b;
}

document.write(add(3, 4));  // 7
```

- `function add(a, b)` 형태로 선언.
- 호출 시 `(3, 4)` 값을 매개변수 `a`, `b`에 전달.

**2) 함수 표현식**

```jsx
const add2 = function (a, b) {
  return a + b;
};

document.write(add2(5, 6));  // 11
```

- 익명 함수를 변수 `add2`에 할당하여 사용.
- 선언문과 동일하게 동작하지만, **변수에 할당된 후에만 호출 가능**.