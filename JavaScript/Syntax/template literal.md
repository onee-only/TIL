# Template Literal

다음과 같은 함수가 있다.

```javascript
function sayHi(name) {
    return "Hi, " + name + ". Nice to meet you.";
}
```

이를 다음과 같이 바꿀 수 있다.

```javascript
function sayHi(name) {
    return `Hi, ${name}. Nice to meet you.`;
}
```

템플릿 리터럴을 쓸 때에는 문자열이 반드시 ` `` `으로 감싸져 있어야 하고,<br>
값이 들어갈 자리에 `${}`를 해 준다.

다음과 같은 것도 가능하다.

```javascript
function something() {
    return `${30 * 40}`;
}
```