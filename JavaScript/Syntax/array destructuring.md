# Array Destructuring

다음과 같은 상황이 있다.

```javascript
const days = ["월", "화", "수"];
```

이 array의 모든 요소를 변수로 가져오고 싶다면 다음과 같이 할 수 있다.

```javascript
const mon = days[0];
const two = days[1];
const wed = days[2];
```

혹은 다음과 같이 할 수 있다.

```javascript
const [mon, two, wed] = days;
```

디폴트 값도 물론 가능하다.

```javascript
const [mon, two, wed, thu = "목"] = days;
```