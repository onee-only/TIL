# Array Destructuring

다음과 같은 상황이 있다.

```javascript
const days = ["월", "화", "수"];
```

이 array의 모든 요소를 변수로 가져오고 싶다면 다음과 같이 할 수 있다.

```javascript
const mon = days[0];
const tuo = days[1];
const wed = days[2];
```

혹은 다음과 같이 할 수 있다.

```javascript
const [mon, tuo, wed] = days;
```

디폴트 값도 물론 가능하다.

```javascript
const [mon, tuo, wed, thu = "목"] = days;
```

이를 이용하면 다음과 같은 것도 할 수 있다.

```javascript
let a = 1;
let b = 2;

[a, b] = [b, a];
```

```javascript
const arr = [1, 2, 3, 4, 5];

const [, , third, ,] = arr;
```