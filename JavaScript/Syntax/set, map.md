# Set, Map

<br>

## Set

Set은 value들의 집합이다. value들은 중복될 수 없다.

```javascript
const a = new Set([1, 1, 1, 2, 3, 3, 4, 5]);

console.log(a); // Set { 1, 2, 3, 4, 5 }
```

위와 같이 중복되는 value들은 제거된다.

Set에는 여러가지 메서드가 있다.

```javascript
const a = new Set([1, 1, 1, 2, 3, 3, 4, 5]);

console.log(a); // Set { 1, 2, 3, 4, 5 }

console.log(a.has(1)); // true

a.delete(1);

console.log(a.has(1)); // false

console.log(a); // Set { 2, 3, 4, 5 }

a.add(6);

console.log(a); // Set { 2, 3, 4, 5, 6 }

a.clear();

console.log(a); // Set {}
```

## Weak Set

WeakSet은 Set은 Set인데 조금 다르다.

WeakSet의 요소 중 참조되지 않는 요소는 Garbage Collector가 동작할 때 사라진다.

## Map

Map은 key와 value로 이루어졌다. Set과 비슷하다.

```javascript
const map = new Map();

map.set("a", 1);
map.set("b", 2);

console.log(map); // Map { 'a' => 1, 'b' => 2 }

console.log(map.get("a")); // 1
```

## Weak Map

Weak Set과 비슷하다.