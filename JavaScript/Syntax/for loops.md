# For Loops

<br>

## for

```javascript
for (let i = 0; i < 10; i++) {
    console.log("hi");
}
```

## forEach

어레이 메서드. 각각의 요소에 대해 콜백 함수를 실행한다. <br>
콜백은 매개변수로 각각 `요소, 인덱스, 현재 배열`을 받는다.

```javascript
const arr = ["a", "b", "c"];

arr.forEach((element, index, array) => {
    console.log(element, index, array);
});
/*
a 0 [ 'a', 'b', 'c' ]
b 1 [ 'a', 'b', 'c' ]
c 2 [ 'a', 'b', 'c' ]
*/
```

## for of

각각의 요소에 대해 실행해준다.

```javascript
const arr = ["a", "b", "c"];

for (const element of arr) {
    console.log(element);
}
/*
a
b
c
*/
```

for of 반복문의 특징은 iterable한 모든 것에 쓸 수 있다는 것이다. <br>

```javascript
const str = "abc";

for (const element of str) {
    console.log(element);
}
/*
a
b
c
*/
```