# Generator

Generator는 중간에 멈출 수 있는 function이다.

형태는 다음과 같다.

```javascript
function* func() {
    yield 1;
    yield 2;
    yield 3;
}
```

yield는 return과 비슷하다.

```javascript
const gen = func();

console.log(gen.next()); // { value: 1, done: false }
console.log(gen.next()); // { value: 2, done: false }
console.log(gen.next()); // { value: 3, done: false }
console.log(gen.next()); // { value: undefined, done: true }
```
