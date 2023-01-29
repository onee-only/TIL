# Array Methods

<br>

## Array.from()
다음과 같은 상황이 있다.

```javascript
const buttons = document.getElementsByClassName("btn");

buttons.forEach(button => { 
    console.log("hi");
});
```

이 코드는 에러가 나는 코드다. <br> 
왜냐하면 buttons는 array가 아닌 array-like object인 HTMLCollection기 때문이다. <br>
이 때문에 buttons에는 forEach 메서드가 없는 것이다.

다음과 같이 바꾸면 실행이 된다.

```javascript
const buttons = document.getElementsByClassName("btn");

Array.from(buttons).forEach(button => { 
    console.log("hi");
});
```

Array.from()은 array-like object를 array로 바꿔준다.