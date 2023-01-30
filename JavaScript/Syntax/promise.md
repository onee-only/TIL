# Promise

<br>

## Promise 만들기

promise의 함수에는 resolve, reject가 있는데, <br>
만약 잘 됐다 하면 resolve를 해 주고, 아니다 싶으면 reject를 해 준다.

```javascript
const a = new Promise((resolve, reject) => {
    if (1 + 1 === 2) {
        resolve("good");
    } else {
        reject("bad");
    }
});
```

## then, catch

promise의 resolve 값을 받으려면 then을 이용할 수 있다.

```javascript
const a = new Promise((resolve, reject) => {
    if (1 + 1 === 2) {
        resolve("good");
    } else {
        reject("bad");
    }
});

a.then((value) => console.log(value)); // good
```

reject 값을 받으려면 catch를 이용한다. 에러가 나도 catch로 간다. <br>
reject가 에러를 날리는 것 같다.

```javascript
const a = new Promise((resolve, reject) => {
    if (1 + 1 !== 2) {
        resolve("good");
    } else {
        reject("bad");
    }
});

a.catch((value) => console.log(value)); // catch
```

둘 다 쓸 수 있다.

```javascript
const a = new Promise((resolve, reject) => {
    if (조건) {
        resolve("good");
    } else {
        reject("bad");
    }
});

a.then((value) => console.log(value)).catch((value) => console.log(value));
```

이러면 resolve일 땐 then, reject일 땐 catch를 실행하는 것이 된다.

## Promise Chaining

return만 해 준다면, then을 계속 쓸 수 있다.

```javascript
const a = new Promise((resolve, reject) => {
    if (true) {
        resolve("good");
    } else {
        reject("bad");
    }
});

a.then((value) => value + " man")
    .then((value) => value + " is")
    .then((value) => value + " me")
    .then((value) => console.log(value));
// good man is me
```

만약 중간에 에러가 나면 catch로 간다.

```javascript
a.then((value) => value + " man")
    .then((value) => value + " is")
    .then((value) => {
        throw Error();
    })
    .then((value) => console.log(value))
    .catch((e) => console.log("caught"));
// caught
```
