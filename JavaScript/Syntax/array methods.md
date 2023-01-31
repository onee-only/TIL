# Array Methods

<br>

## Array.from

다음과 같은 상황이 있다.

```javascript
const buttons = document.getElementsByClassName("btn");

buttons.forEach((button) => {
    console.log("hi");
});
```

이 코드는 에러가 나는 코드다. <br>
왜냐하면 buttons는 array가 아닌 array-like object인 HTMLCollection기 때문이다.<br>
이 때문에 buttons에는 forEach 메서드가 없는 것이다.

다음과 같이 바꾸면 실행이 된다.

```javascript
const buttons = document.getElementsByClassName("btn");

Array.from(buttons).forEach((button) => {
    console.log("hi");
});
```

Array.from()은 array-like object를 array로 바꿔준다.

## Array.flat

array를 펴준다.

```javascript
const flatTest = [1, [[2], [3, [[5, 5]]]]];

console.log(flatTest.flat()); // [1, [2], [3, [[5, 5]]]]
console.log(flatTest.flat(2)); // [1, 2, 3, [[5, 5]]]
console.log(flatTest.flat(3)); // [1, 2, 3, [5, 5]]
console.log(flatTest.flat(4)); // [1, 2, 3, 5, 5]
```

## Array.sort

배열을 정렬해준다. 사용자 지정 비교 function을 인수로 넣을 수 있다.

```javascript
const people = [
    {
        name: "person1",
        age: 12,
    },
    {
        name: "person2",
        age: 30,
    },
];

const orderPeopleByAge = (personA, personB) => {
    return personB.age - personA.age;
};

console.log(people.sort(orderPeopleByAge));
// [ { name: 'person2', age: 30 }, { name: 'person1', age: 12 } ]
```

비교 함수의 반환값이

0보다 작으면 첫번째 매개변수가 더 작다. <br>
0이면 서로 같다. <br>
0보다 크면 두번째 매개변수가 더 작다.

그리고 Array.sort는 실제 배열에 영향을 준다.
