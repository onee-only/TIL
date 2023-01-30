# Object Destructuring

다음과 같은 상황이 있다.

```javascript
const person = {
    favs: {
        food: "pizza",
    },
    name: "person",
    age: 18,
};
```

여기서 food를 빼 오고싶으면 어떻게 해야 할까?

```javascript
const favFood = person.favs.food;
```

아마 이렇게 할 것이다.

하지만 다음과 같이 작성할 수도 있다.

```javascript
const {
    favs: { food },
} = person;
```

이렇게 하면 person 안의 favs 안의 food만 빼 오는 것이다. <br>
그런데 무조건 food라는 이름으로 해야 할까?

```javascript
const {
    favs: { food: favFood },
} = person;
```

이제 food가 아닌 favFood이다.

디폴트 값을 설정할 수도 있다.

```javascript
const {
    favs: { music },
} = person;

console.log(music); // undefined
```

```javascript
const {
    favs: { music = "jazz" },
} = person;

console.log(music); // jazz
```
