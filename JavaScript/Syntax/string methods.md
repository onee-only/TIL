# String Methods

<br>

## includes

문자열이 들어있는지 검사

```javascript
"abcdefg".includes("c"); // true
```

## repeat

문자열을 반복

```javascript
"a".repeat(3); // "aaa"
```

## startsWith, endsWith

처음, 뒤의 문자열이 일치하는지 검사

```javascript
const string = "Hi, Nice to meet you";

string.startsWith("Hi"); // true
string.endsWith("you"); // true
```

## padStart, padEnd

maxLength까지 문자열의 앞, 뒤에 string을 추가한다. 필요하면 반복도 한다.

```javascript
console.log("o".padStart(6, "x")); // xxxxxo
console.log("piz".padEnd(5, "za")); // pizza
```

문자열 자체를 바꾸는 게 아닌 바뀐 문자열을 반환한다.

## trim, trimStart, trimEnd

문자열 앞, 뒤의 공백을 없애준다.

```javascript
const str = "     hello    ";

console.log(str.trimStart()); // "hello    "
console.log(str.trimEnd()); // "      hello"
console.log(str.trim()); // "hello"
```

마찬가지로 문자열을 반환한다.

## replaceAll

코드로 보는 게 더 쉬울 것 같다.

```javascript
const a = "abbbc";

const b = a.replaceAll("b", "d");

console.log(a); // "abbbc"
console.log(b); // "adddc"
```