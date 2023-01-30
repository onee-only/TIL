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

## Promise.all

Promise.all은 인수로 주어진 promise들이 모두 끝난 후에 <br>
모든 value를 가지고 promise를 반환한다.

```javascript
const a = new Promise((resolve) => {
    setTimeout(resolve, 50, "a done");
});
const b = new Promise((resolve) => {
    setTimeout(resolve, 150, "b done");
});
const c = new Promise((resolve) => {
    setTimeout(resolve, 30, "c done");
});

const d = Promise.all([a,b,c]);

d.then(values => console.log(values));
// [ 'a done', 'b done', 'c done' ]
```

## Promise.race

Promise.race는 인수로 받은 promise의 배열 중에 <br> 
가장 빨리 끝나는 promise의 value로 promise를 반환한다.

```javascript
const a = new Promise((resolve) => {
    setTimeout(resolve, 50, "a done");
});
const b = new Promise((resolve) => {
    setTimeout(resolve, 150, "b done");
});
const c = new Promise((resolve) => {
    setTimeout(resolve, 30, "c done");
});

const d = Promise.race([a,b,c]);

d.then(value => console.log(value));
// 'c done'
```

