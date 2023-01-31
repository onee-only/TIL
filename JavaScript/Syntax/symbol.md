# Symbol

Symbol은 고유한 성질을 가진다.

```javascript
const a = Symbol();
const b = Symbol();

console.log(a === b); // false
```

description을 설정할 수도 있다. 설정해도 같아지지는 않는다.

```javascript
const a = Symbol("c");
const b = Symbol("c");

console.log(a === b); // false
```