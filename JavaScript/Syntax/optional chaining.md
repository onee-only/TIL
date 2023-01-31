# Optional Chaining

다음과 같은 상황이 있다.

```javascript
const personA = {
    name: "personA",
    profile: {
        email: "something",
    },
};

const personB = {
    name: "personB",
};

console.log(personA.profile.email); // something
console.log(personB.profile.email); // TypeError: Cannot read property 'email' of undefined
```

personB는 프로필이 없을 수 있기 때문에 체크를 해 줘야 한다.

```javascript
console.log(personB.profile && personB.profile.email); // undefined
```

하지만 이 코드는 자칫하면 매우 길어질 수 있다. <br>
이 때 optional chaining을 이용할 수 있다.

```javascript
console.log(personB.profile?.email); // undefined
```

만약 profile이 undefined면 undefined를 반환하고, 아니면 오른쪽으로 더 들어간다.
