# Spread, Rest

<br>

## Spread 연산자

다음과 같은 두 array가 있다.

```javascript
const a = [1, 2, 3];
const b = [4, 5, 6];
```

이 둘을 합치고 싶으면 어떻게 해야 할까?

```javascript
const c = a + b; // "1,2,34,5,6"
const d = [a, b]; // [ [ 1, 2, 3 ], [ 4, 5, 6 ] ]
```

이럴 땐 spread 연산자를 쓸 수 있다.

```javascript
const c = [...a, ...b]; // [ 1, 2, 3, 4, 5, 6 ]
```

spread 연산자는 unpack을 해 준다고 보면 된다.

object에도 적용 가능하다.

```javascript
const a = {
    hi: "hi",
    yes: true,
};
const b = {
    hello: "hello",
    num: 5,
};

const c = { ...a, ...b };

/*
{
    hi: 'hi',
    yes: true,
    hello: 'hello',
    num: 5
}
*/
```

## Rest 연산자

다음과 같은 함수가 있다.

```javascript
function log(something) {
    console.log(something);
}
```

이 함수를 이렇게 쓰고싶다.

```javascript
log(1, 2, 3, "aefaef", "eaereiarl", {}, ["5", 5]); // 1
```

보다시피 첫번째 인수만 들어가는 것을 볼 수 있다.

이럴 때는 rest 연산자를 쓰면 된다.

```javascript
function log(...something) {
    console.log(something);
}

log(1, 2, 3, "aefaef", "eaereiarl", {}, ["5", 5]);
// [ 1, 2, 3, 'aefaef', 'eaereiarl', {}, [ '5', 5 ] ]
```

rest 연산자는 spread 연산자와 반대로 pack을 해 준다고 생각할 수 있다.

이런 것도 가능하다

```javascript
function log(first, second, ...something) {
    console.log("first : ", first);
    console.log("second : ", second);
    console.log(something);
}

log(1, 2, 3, "aefaef", "eaereiarl", {}, ["5", 5]);

/*
first :  1
second :  2
[ 3, 'aefaef', 'eaereiarl', {}, [ '5', 5 ] ]
*/
```
