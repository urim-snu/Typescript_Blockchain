# Typescript_Blockchain

Learning Typescript by making a Blockchain
By Nomad Coder

### Install Typescript

`$ yarn add global typescript`

### tsconfig.json

Ts에게 어떻게 JS로 compile 하는지에 대한 옵션을 알려주는 파일.

```json
{
  "compilerOptions": {
    "module": "commonjs",
    "target": "ES2015",
    "sourceMap": true,
    "outDir": "dist"
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules"]
}
```

(Nicolas' option)

### How to Compile

`$ tsc` -> index.js 와 index.js.map을 만든다.

### TS with Function Argument

함수의 argument 개수가 맞지 않을 때 컴파일을 막는다. (JS에서는 일어나지 않는 일),  
\* argument? : 선택적인 파라미터

### TS with Type

funcrion(argument : any) : 모든 type이 가능.
funcrion(argument:string) : string type만 가능.
funcrion(argument:number) : number type만 가능.

```ts
const foo = (arg: type): returnType => {};
```

### Interface

Type for Object

```ts
interface Human {
  name: string;
  age: number;
  gender: string;
}

const sayHi = (person: Human): string => {
  return `Hello ${person.name}`;
};
```

interface code는 compile 뒤에 js 파일에 포함되지 않는다.  
그러한 case를 원할 경우 class로 선언한다. (Java랑 비슷)

ex) react, express, node...

```ts
class Human {
  public name: string;
  public age: number;
  public gender: string;
  constructor(name: string, age: number, gender: string) {
    this.name = name;
    this.age = age;
    this.gender = gender;
  }
}

const Urim = new Human("Urim", 23, "male");
```

### import in TS (like Python)

```ts
import * as CryptoJS from "crypto-js";
```
