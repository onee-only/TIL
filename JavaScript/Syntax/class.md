# Class

<br>

## Class

class는 설계도라 보면 된다.

다음과 같이 이루어져 있다.

```javascript
class Person {
    constructor(name) {
        this.name = name;
    }
    sayHi() {
        console.log(`Hi, I'm ${this.name}`);
    }
}
```

생성자와 메서드가 있는 기본적인 형태다.

인스턴스는 다음과 같이 생성할 수 있다.

```javascript
const somebody = new Person("somebody");
somebody.sayHi(); // "Hi, I'm somebody"
```

클래스가 오브젝트와 다른 점은 인스턴스를 동적으로 생성한다는 것이다.

클래스는 인스턴스를 찍어내는 공장이고, 오브젝트는 그냥 오브젝트다.

## extends

클래스를 확장한 클래스를 만들 수 있다.

```javascript
class Person {
    constructor(name) {
        this.name = name;
    }
    sayHi() {
        console.log(`Hi, I'm ${this.name}`);
    }
}

class Student extends Person {
    constructor(name, grade) {
        super(name);
        this.grade = grade;
    }
    imStudent() {
        console.log("I'm student. grade:", this.grade);
    }
}

const student = new Student("person", 1);

student.sayHi(); // Hi, I'm person
student.imStudent(); // I'm student. grade: 1
```

extends를 사용하면 오른쪽 클래스의 모든 것을 상속한다. <br>
super()를 사용하면 상속받은 클래스의 생성자를 부른다.

## properties

### field declaration

field는 constructor 없이 초기화 할 수 있다.

```javascript
class Person {
    name = "person";
}
```

### private properties

필드나 메서드 앞에 #를 붙이면 클래스 밖에서 쓸 수 없다.

```javascript
class Person {
    #socialSecurityNumber = "111111-1111111";
    get socialSecurityNumber() {
        this.#warn();
        return "SECRET";
    }

    #warn() {
        console.log("Do not attemp to access");
    }
}

const person = new Person();

console.log(person.#socialSecurityNumber); // 에러
console.log(person.socialSecurityNumber);
// Do not attemp to access
// SECRET

person.#warn(); // 에러
```

private 필드는 get {이름} 하고 getter를 사용할 수 있다.  
setter도 똑같다.

### static properties

필드나 메서드 앞에 static을 붙일 수 있다.

```javascript
class Person {
    static define() {
        console.log("I'm Human");
    }

    static #unreachable() {
        return "this is unreachable";
    }
}

const person = new Person();

Person.define(); // I'm Human
person.define(); // 에러

Person.#unreachable(); // 에러
person.#unreachable(); // 에러
```
