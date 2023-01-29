# Dead Zone

<br>

## Hoisting

```javascript
console.log(a); // undefined
var a = 1;
```

위 코드는 아무런 오류가 없다. <br>
왜냐하면 javascript가 아래와 같이 hoisting 해 주기 때문이다.

```javascript
var a;
console.log(a); // undefined
a = 1;
```

이것은 좋지 않다. 위 상황은 대부분 실수로 일어나는 상황이며, 이것은 예방해줄 필요가 있다. <br>
그러면 let을 써 주면 된다.

```javascript
console.log(a); // 에러
let a = 1;
```