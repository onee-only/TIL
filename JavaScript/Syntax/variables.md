# Variables

<br>

## var


var는 큰 어플리케이션을 개발하는 상황 등에서 문제를 발생시킬 수 있다. <br>
아래 상황을 봐 보자.

```javascript
var name = "A"; // A의 코드 

name = "B";  // B의 코드
```

<p>
다른 개발자와 같이 작업을 할 때, 내가 의도한 바가 아니더라도, 덮어씌워질 수가 있다. <br>
어떤 때는 괜찮을 수도 있겠지만, 이것은 프로젝트를 완전히 망가뜨릴 수도 있다.
</p>

<p>
무엇이 변하지 말아야 하는지 명확히 할 필요가 있다.
</p>

## let, const
const를 사용하면 이를 해결할 수 있다.

```javascript
const name = "A";

name = "B";  // 에러
```

변수를 재할당 하고 싶으면 let을 사용하면 된다.

```javascript
let name = "A";

name = "B";
```

하지만 const도 모든 것을 보호해 주지는 못한다. 

```javascript
const food = {
    name: "pizza"
};

food = true;    // 에러

food.name = "sushi";    // 가능
```