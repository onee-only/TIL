# Block Scope

javascript에서 block 안에서 선언이 된 변수는 block 안에서만 사용할 수 있다.

```javascript
const a = 1;

if (true) {
    a = 2;
    const b = 3;
}

console.log(a); // 2
console.log(b); // 에러
```

``{}``안에서 선언된 변수는 ``{}``안에서만 사용 가능하다. 

```javascript
if (true) {
    const a = 1;

    if (true) {
        const b = 2;

        console.log(a); // 1
    }

    console.log(b); // 에러
}
```

근데 var는 포함이 안 된다.

```javascript
if (true) {
    var a = 1;
}
console.log(a); // 1
```

function으로는 묶인다.

```javascript
function varSucks() {
    var a = 1;
}
console.log(a); // 에러
```