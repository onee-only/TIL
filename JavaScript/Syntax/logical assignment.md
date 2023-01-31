# Logical Assignment

<br>

## Logical OR Operator

이름을 입력받아 인사하는 코드가 있다.

```javascript
let yourName = prompt("type your name");

console.log(`Hi, ${yourName}`);
```

만약 이름을 입력받지 못하면 미리 만든 이름으로 대체하고 싶다고 하자.

```javascript
let yourName = prompt("type your name");

if (!yourName) {
    yourName = "anonymous";
}

console.log(`Hi, ${yourName}`);
```

아니면 이렇게 할 수도 있다.

```javascript
let yourName = prompt("type your name");

yourName ||= "anonymous";

console.log(`Hi, ${yourName}`);
```

logical or operator는 만약 대입하고 있는 변수가 falsy하다면 대입을 하고, 아니면 그대로 둔다.

## Logical AND Operator

이건 OR과 반대다. 만약 value가 있다면 덮어씌워준다.

```javascript
let a = "a";

a &&= "b";
console.log(a); // "b"
```

## Logical NULLISH Operator

이건 OR과 비슷하지만, value가 undefined거나 null일 때만 덮어씌운다.

```javascript
let a = null;

a ??= "";

console.log(a); // ''

a ??= "a";

console.log(a); // ''
```