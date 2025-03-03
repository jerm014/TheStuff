# Project 2347: ES6 classes
----


![1](2347_1.jpeg)

## Resources

**Read or watch**:

* [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
* [Metaprogramming](https://www.keithcirkel.co.uk/metaprogramming-in-es6-symbols/#symbolspecies)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* How to define a Class
* How to add methods to a class
* Why and how to add a static method to a class
* How to extend a class from another
* Metaprogramming and symbols
## Requirements

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`node 20.x.x`and`npm 9.x.x`
* Allowed editors:`vi`,`vim`,`emacs`,`Visual Studio Code`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`js`extension
* Your code will be tested using`Jest`and the command`npm run test`
* Your code will be verified against lint using ESLint
* Your code needs to pass all the tests and lint. You can verify the entire project running`npm run full-test`
## Setup

### Install NodeJS 20.x.x

(in your home directory):

``
```
curl -sL https://deb.nodesource.com/setup_20.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y

$ nodejs -v
v20.15.1
$ npm -v
10.7.0
```
### Install Jest, Babel, and ESLint

in your project directory:

* Install Jest using:`npm install --save-dev jest`
* Install Babel using:`npm install --save-dev babel-jest @babel/core @babel/preset-env`
* Install ESLint using:`npm install --save-dev eslint`
## Configuration files

### `package.json`

Click to show/hide file contents``
```
{
  "scripts": {
    "lint": "./node_modules/.bin/eslint",
    "check-lint": "lint [0-9]*.js",
    "dev": "npx babel-node",
    "test": "jest",
    "full-test": "./node_modules/.bin/eslint [0-9]*.js && jest"
  },
  "devDependencies": {
    "@babel/core": "^7.6.0",
    "@babel/preset-env": "^7.6.0",
    "@babel/node": "^7.8.0",
    "eslint": "^6.8.0",
    "eslint-config-airbnb-base": "^14.0.0",
    "eslint-plugin-import": "^2.18.2",
    "eslint-plugin-jest": "^22.17.0",
    "jest": "^24.9.0"
  }
}
```
### `babel.config.js`

Click to show/hide file contents``
```
module.exports = {
  presets: [
    [
      '@babel/preset-env',
      {
        targets: {
          node: 'current',
        },
      },
    ],
  ],
};
```
### `.eslintrc.js`

Click to show/hide file contents``
```
module.exports = {
  env: {
    browser: false,
    es6: true,
    jest: true,
  },
  extends: [
    'airbnb-base',
    'plugin:jest/all',
  ],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  plugins: ['jest'],
  rules: {
    'max-classes-per-file': 'off',
    'no-underscore-dangle': 'off',
    'no-console': 'off',
    'no-shadow': 'off',
    'no-restricted-syntax': [
      'error',
      'LabeledStatement',
      'WithStatement',
    ],
  },
  overrides:[
    {
      files: ['*.js'],
      excludedFiles: 'babel.config.js',
    }
  ]
};
```
### and…

Don’t forget to run`$ npm install`when you have the`package.json`


----
## Tasks
---
### 0. You used to attend a place like this at some point

Implement a class named <!--plain-NL-->`ClassRoom`<!--inline-NL-->:<!--plain-NL-->

- Prototype: `export default class ClassRoom`
- It should accept one attribute named `maxStudentsSize` (Number) and assigned to `_maxStudentsSize`

```
bob@dylan:~$ cat 0-main.js
import ClassRoom from "./0-classroom.js";

const room = new ClassRoom(10);
console.log(room._maxStudentsSize)

bob@dylan:~$ 
bob@dylan:~$ npm run dev 0-main.js 
10
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `0-classroom.js`


---
### 1. Let's make some classrooms

Import the <!--plain-NL-->`ClassRoom`<!--inline-NL--> class from <!--plain-NL-->`0-classroom.js`<!--inline-NL-->. <!--plain-NL-->

Implement a function named <!--plain-NL-->`initializeRooms`<!--inline-NL-->. It should return an array of 3 <!--plain-NL-->`ClassRoom`<!--inline-NL--> objects with the sizes 19, 20, and 34 (in this order).<!--plain-NL-->

```
bob@dylan:~$ cat 1-main.js
import initializeRooms from './1-make_classrooms.js';

console.log(initializeRooms());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 1-main.js 
[
  ClassRoom { _maxStudentsSize: 19 },
  ClassRoom { _maxStudentsSize: 20 },
  ClassRoom { _maxStudentsSize: 34 }
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `1-make_classrooms.js`


---
### 2. A Course, Getters, and Setters

Implement a class named <!--plain-NL-->`HolbertonCourse`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`name` (String)
`length` (Number)
`students` (array of Strings)
- `name` (String)
- `length` (Number)
- `students` (array of Strings)
- Make sure to verify the type of attributes during object creation
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.

- `name` (String)
- `length` (Number)
- `students` (array of Strings)

```
bob@dylan:~$ cat 2-main.js
import HolbertonCourse from "./2-hbtn_course.js";

const c1 = new HolbertonCourse("ES6", 1, ["Bob", "Jane"])
console.log(c1.name);
c1.name = "Python 101";
console.log(c1);

try {
    c1.name = 12;
} 
catch(err) {
    console.log(err);
}

try {
    const c2 = new HolbertonCourse("ES6", "1", ["Bob", "Jane"]);
}
catch(err) {
    console.log(err);
}

bob@dylan:~$ 
bob@dylan:~$ npm run dev 2-main.js 
ES6
HolbertonCourse {
  _name: 'Python 101',
  _length: 1,
  _students: [ 'Bob', 'Jane' ]
}
TypeError: Name must be a string
    ...
TypeError: Length must be a number
    ...
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `2-hbtn_course.js`


---
### 3. Methods, static methods, computed methods names..... MONEY

Implement a class named <!--plain-NL-->`Currency`<!--inline-NL-->:<!--plain-NL-->

- - Constructor attributes: 


`code` (String)
`name` (String)
- `code` (String)
- `name` (String)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.
- Implement a method named `displayFullCurrency` that will return the attributes in the following format `name (code)`.

- `code` (String)
- `name` (String)

```
bob@dylan:~$ cat 3-main.js
import Currency from "./3-currency.js";

const dollar = new Currency('$', 'Dollars');
console.log(dollar.displayFullCurrency());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 3-main.js 
Dollars ($)
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `3-currency.js`


---
### 4. Pricing

Import the class <!--plain-NL-->`Currency`<!--inline-NL--> from <!--plain-NL-->`3-currency.js`<!--inline-NL-->

Implement a class named <!--plain-NL-->`Pricing`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`amount` (Number)
`currency` (Currency)
- `amount` (Number)
- `currency` (Currency)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter and setter for each attribute.
- Implement a method named `displayFullPrice` that returns the attributes in the following format `amount currency_name (currency_code)`.
- Implement a static method named `convertPrice`. It should accept two arguments: `amount` (Number), `conversionRate` (Number). The function should return the amount multiplied by the conversion rate.

- `amount` (Number)
- `currency` (Currency)

```
bob@dylan:~$ cat 4-main.js
import Pricing from './4-pricing.js';
import Currency from './3-currency.js';

const p = new Pricing(100, new Currency("EUR", "Euro"))
console.log(p);
console.log(p.displayFullPrice());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 4-main.js 
Pricing {
  _amount: 100,
  _currency: Currency { _code: 'EUR', _name: 'Euro' }
}
100 Euro (EUR)
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `4-pricing.js`


---
### 5. A Building

Implement a class named <!--plain-NL-->`Building`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`sqft` (Number)
- `sqft` (Number)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter for each attribute.
- Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named `evacuationWarningMessage`.


If a class that extends from it does not have a `evacuationWarningMessage` method, throw an error with the message `Class extending Building must override evacuationWarningMessage`
- If a class that extends from it does not have a `evacuationWarningMessage` method, throw an error with the message `Class extending Building must override evacuationWarningMessage`

- `sqft` (Number)

- If a class that extends from it does not have a `evacuationWarningMessage` method, throw an error with the message `Class extending Building must override evacuationWarningMessage`

```
bob@dylan:~$ cat 5-main.js
import Building from './5-building.js';

const b = new Building(100);
console.log(b);

class TestBuilding extends Building {}

try {
    new TestBuilding(200)
}
catch(err) {
    console.log(err);
}

bob@dylan:~$ 
bob@dylan:~$ npm run dev 5-main.js 
Building { _sqft: 100 }
Error: Class extending Building must override evacuationWarningMessage
    ...
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `5-building.js`


---
### 6. Inheritance

Import <!--plain-NL-->`Building`<!--inline-NL--> from <!--plain-NL-->`5-building.js`<!--inline-NL-->.<!--plain-NL-->

Implement a class named <!--plain-NL-->`SkyHighBuilding`<!--inline-NL--> that extends from <!--plain-NL-->`Building`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`sqft` (Number) (must be assigned to the parent class `Building`)
`floors` (Number)
- `sqft` (Number) (must be assigned to the parent class `Building`)
- `floors` (Number)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Implement a getter for each attribute.
- Override the method named `evacuationWarningMessage` and return the following string `Evacuate slowly the NUMBER_OF_FLOORS floors`.

- `sqft` (Number) (must be assigned to the parent class `Building`)
- `floors` (Number)

```
bob@dylan:~$ cat 6-main.js
import SkyHighBuilding from './6-sky_high.js';

const building = new SkyHighBuilding(140, 60);
console.log(building.sqft);
console.log(building.floors);
console.log(building.evacuationWarningMessage());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 6-main.js 
140
60
Evacuate slowly the 60 floors
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `6-sky_high.js`


---
### 7. Airport

Implement a class named <!--plain-NL-->`Airport`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`name` (String)
`code` (String)
- `name` (String)
- `code` (String)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- The default string description of the class should return the airport `code` (example below).

- `name` (String)
- `code` (String)

```
bob@dylan:~$ cat 7-main.js
import Airport from "./7-airport.js";

const airportSF = new Airport('San Francisco Airport', 'SFO');
console.log(airportSF);
console.log(airportSF.toString());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 7-main.js 
Airport [SFO] { _name: 'San Francisco Airport', _code: 'SFO' }
[object SFO]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `7-airport.js`


---
### 8. Primitive - Holberton Class

Implement a class named <!--plain-NL-->`HolbertonClass`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`size` (Number)
`location` (String)
- `size` (Number)
- `location` (String)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- When the class is cast into a `Number`, it should return the size.
- When the class is cast into a `String`, it should return the location.

- `size` (Number)
- `location` (String)

```
bob@dylan:~$ cat 8-main.js
import HolbertonClass from "./8-hbtn_class.js";

const hc = new HolbertonClass(12, "Mezzanine")
console.log(Number(hc));
console.log(String(hc));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 8-main.js 
12
Mezzanine
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `8-hbtn_class.js`


---
### 9. Hoisting

Fix this code and make it work.<!--plain-NL-->

```
const class2019 = new HolbertonClass(2019, 'San Francisco');
const class2020 = new HolbertonClass(2020, 'San Francisco');

export class HolbertonClass {
  constructor(year, location) {
    this._year = year;
    this._location = location;
  }

  get year() {
    return this._year;
  }

  get location() {
    return this._location;
  }
}

const student1 = new StudentHolberton('Guillaume', 'Salva', class2020);
const student2 = new StudentHolberton('John', 'Doe', class2020);
const student3 = new StudentHolberton('Albert', 'Clinton', class2019);
const student4 = new StudentHolberton('Donald', 'Bush', class2019);
const student5 = new StudentHolberton('Jason', 'Sandler', class2019);

export class StudentHolberton {
  constructor(firstName, lastName) {
    this._firstName = firstName;
    this._lastName = lastName;
    this._holbertonClass = holbertonClass;
  }

  get fullName() {
    return `${this._firstName} ${this._lastName}`;
  }

  get holbertonClass() {
    return this.holbertonClass;
  }

  get fullStudentDescription() {
    return `${self._firstName} ${self._lastName} - ${self._holbertonClass.year} - ${self._holbertonClass.location}`;
  }
}


export const listOfStudents = [student1, student2, student3, student4, student5];

```

Result:<!--plain-NL-->

```
bob@dylan:~$ cat 9-main.js
import listOfStudents from "./9-hoisting.js";

console.log(listOfStudents);

const listPrinted = listOfStudents.map(
    student => student.fullStudentDescription
);

console.log(listPrinted)

bob@dylan:~$ 
bob@dylan:~$ npm run dev 9-main.js
[
  StudentHolberton {
    _firstName: 'Guillaume',
    _lastName: 'Salva',
    _holbertonClass: HolbertonClass { _year: 2020, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'John',
    _lastName: 'Doe',
    _holbertonClass: HolbertonClass { _year: 2020, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Albert',
    _lastName: 'Clinton',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Donald',
    _lastName: 'Bush',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  },
  StudentHolberton {
    _firstName: 'Jason',
    _lastName: 'Sandler',
    _holbertonClass: HolbertonClass { _year: 2019, _location: 'San Francisco' }
  }
]
[
  'Guillaume Salva - 2020 - San Francisco',
  'John Doe - 2020 - San Francisco',
  'Albert Clinton - 2019 - San Francisco',
  'Donald Bush - 2019 - San Francisco',
  'Jason Sandler - 2019 - San Francisco'
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `9-hoisting.js`


---
### 10. Vroom

Implement a class named <!--plain-NL-->`Car`<!--inline-NL-->:<!--plain-NL-->

- Constructor attributes: 


`brand` (String)
`motor` (String)
`color` (String)
- `brand` (String)
- `motor` (String)
- `color` (String)
- Each attribute must be stored in an “underscore” attribute version (ex: `name` is stored in `_name`)
- Add a method named `cloneCar`. This method should return a new object of the class.

- `brand` (String)
- `motor` (String)
- `color` (String)

Hint: Symbols in ES6<!--plain-NL-->

```
bob@dylan:~$ cat 10-main.js
import Car from "./10-car.js";

class TestCar extends Car {}

const tc1 = new TestCar("Nissan", "Turbo", "Pink");
const tc2 = tc1.cloneCar();

console.log(tc1);
console.log(tc1 instanceof TestCar);

console.log(tc2);
console.log(tc2 instanceof TestCar);

console.log(tc1 == tc2);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 10-main.js
TestCar { _brand: 'Nissan', _motor: 'Turbo', _color: 'Pink' }
true
TestCar { _brand: undefined, _motor: undefined, _color: undefined }
true
false
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_classes`
- File: `10-car.js`