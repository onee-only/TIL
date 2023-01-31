# Object Methods

<br>

## Object.values

object의 value들만 반환

```javascript
const person = {
    name: "person",
    age: 20,
};

console.log(Object.values(person)); // [ 'person', 20 ]
```

## Object.entries

object의 key와 value들을 반환

```javascript
const person = {
    name: "person",
    age: 20,
};

console.log(Object.entries(person));
// [ [ 'name', 'person' ], [ 'age', 20 ] ]
```

## Object.fromEntries

array로 object를 만든다.

```javascript
const arr = [
    ["name", "person"],
    ["age", 20],
];

console.log(Object.fromEntries(arr));
// { name: 'person', age: 20 }
```
