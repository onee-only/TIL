# Async, Await

<br>

## Async, Await

비동기 처리는 다음 두 방식으로 표현할 수 있다.

```javascript
const getMoviesPromise = () => {
    fetch("https://yts.mx/api/v2/list_movies.json")
        .then((response) => response.json())
        .then((json) => console.log(json));
};

const getMoviesAsync = async () => {
    const response = await fetch("https://yts.mx/api/v2/list_movies.json");
    const json = await response.json();
    console.log(json);
};
```

async, await 방식이 더 신식이며, 더 편하기도 하다.

async 함수는 다음과 같이 표현이 가능하다.

```javascript
async function myFunction() {}

const anonFunction = async () => {};
```

await은 Promise가 resolve나 reject하기까지 기다릴 수 있게 해 준다.

## 팁

async, await을 사용할 때 try, catch, finally를 사용하면 <br>
.then(), .catch(), .finally()사용한 것과 같다.

