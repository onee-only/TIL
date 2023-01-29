# Arrow Function

<br>

## 기존 function

funtion의 원형은 아래와 같다.

```javascript
function a() {

}
```

이를 익명함수로 만들 수도 있다.


```javascript
function() {

};
```

이걸 대입할 수도 있다.


```javascript
const a = function() {

};
```

## Arrow Function

기존의 익명함수는 화살표 함수로 대체될 수 있다.

```javascript
const a = function() {

};

const b = () => {

};
```

만약 화살표 함수가 return문만 있다면 이를 축약시킬 수 있다.

```javascript
const a = function() {
    return 1 + 1;
};

const b = () => {
    return 1 + 1;
};

const c = () => 1 + 1;
```

만약 object를 return한다고 하면 다음과 같이 할 수 있다.

```javascript
const a = () => ({
    name: "a",
    something: true
});
```