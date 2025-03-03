# Project 2348: ES6 data manipulation
----


![1](2348_1.jpg)

## Resources

**Read or watch**:

* [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
* [Typed Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Typed_arrays)
* [Set Data Structure](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set)
* [Map Data Structure](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
* [WeakMap](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/WeakMap)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* How to use map, filter and reduce on arrays
* Typed arrays
* The Set, Map, and Weak link data structures
## Requirements

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`node 20.x.x`and`npm 9.x.x`
* Allowed editors:`vi`,`vim`,`emacs`,`Visual Studio Code`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`js`extension
* Your code will be tested using`Jest`and the command`npm run test`
* Your code will be verified against lint using ESLint
* Your code needs to pass all the tests and lint. You can verify the entire project running`npm run full-test`
* All of your functions must be exported
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
    "@babel/node": "^7.8.0",
    "@babel/preset-env": "^7.6.0",
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
### 0. Basic list of objects

Create a function named <!--plain-NL-->`getListStudents`<!--inline-NL--> that returns an array of objects. <!--plain-NL-->

Each object should have three attributes: <!--plain-NL-->`id`<!--inline-NL--> (Number), <!--plain-NL-->`firstName`<!--inline-NL--> (String), and <!--plain-NL-->`location`<!--inline-NL--> (String). <!--plain-NL-->

The array contains the following students in order: <!--plain-NL-->

- `Guillaume`, id: `1`, in `San Francisco`
- `James`, id: `2`, in `Columbia`
- `Serena`, id: `5`, in `San Francisco`

```
bob@dylan:~$ cat 0-main.js
import getListStudents from "./0-get_list_students.js";

console.log(getListStudents());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 0-main.js 
[
  { id: 1, firstName: 'Guillaume', location: 'San Francisco' },
  { id: 2, firstName: 'James', location: 'Columbia' },
  { id: 5, firstName: 'Serena', location: 'San Francisco' }
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `0-get_list_students.js`


---
### 1. More mapping

Create a function <!--plain-NL-->`getListStudentIds`<!--inline-NL--> that returns an array of ids from a list of object.<!--plain-NL-->

This function is taking one argument which is an array of objects - and this array is the same format as <!--plain-NL-->`getListStudents`<!--inline-NL--> from the previous task.<!--plain-NL-->

If the argument is not an array, the function is returning an empty array.<!--plain-NL-->

You must use the <!--plain-NL-->`map`<!--inline-NL--> function on the array.<!--plain-NL-->

```
bob@dylan:~$ cat 1-main.js
import getListStudentIds from "./1-get_list_student_ids.js";
import getListStudents from "./0-get_list_students.js";

console.log(getListStudentIds("hello"));
console.log(getListStudentIds(getListStudents()));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 1-main.js 
[]
[ 1, 2, 5 ]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `1-get_list_student_ids.js`


---
### 2. Filter

Create a function <!--plain-NL-->`getStudentsByLocation`<!--inline-NL--> that returns an array of objects who are located in a specific city.<!--plain-NL-->

It should accept a list of students (from <!--plain-NL-->`getListStudents`<!--inline-NL-->) and a <!--plain-NL-->`city`<!--inline-NL--> (string) as parameters.<!--plain-NL-->

You must use the <!--plain-NL-->`filter`<!--inline-NL--> function on the array.<!--plain-NL-->

```
bob@dylan:~$ cat 2-main.js
import getListStudents from "./0-get_list_students.js";
import getStudentsByLocation from "./2-get_students_by_loc.js";

const students = getListStudents();

console.log(getStudentsByLocation(students, 'San Francisco'));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 2-main.js 
[
  { id: 1, firstName: 'Guillaume', location: 'San Francisco' },
  { id: 5, firstName: 'Serena', location: 'San Francisco' }
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `2-get_students_by_loc.js`


---
### 3. Reduce

Create a function <!--plain-NL-->`getStudentIdsSum`<!--inline-NL--> that returns the sum of all the student ids.<!--plain-NL-->

It should accept a list of students (from <!--plain-NL-->`getListStudents`<!--inline-NL-->) as a parameter. <!--plain-NL-->

You must use the <!--plain-NL-->`reduce`<!--inline-NL--> function on the array. <!--plain-NL-->

```
bob@dylan:~$ cat 3-main.js
import getListStudents from "./0-get_list_students.js";
import getStudentIdsSum from "./3-get_ids_sum.js";

const students = getListStudents();
const value = getStudentIdsSum(students);

console.log(value);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 3-main.js 
8
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `3-get_ids_sum.js`


---
### 4. Combine

Create a function <!--plain-NL-->`updateStudentGradeByCity`<!--inline-NL--> that returns an array of students for a specific city with their new grade<!--plain-NL-->

It should accept a list of students (from <!--plain-NL-->`getListStudents`<!--inline-NL-->), a <!--plain-NL-->`city`<!--inline-NL--> (String), and <!--plain-NL-->`newGrades`<!--inline-NL--> (Array of “grade” objects) as parameters. <!--plain-NL-->

`newGrades`<!--inline-NL--> is an array of objects with this format:<!--plain-NL-->

```
  {
    studentId: 31,
    grade: 78,
  }

```

If a student doesn’t have grade in <!--plain-NL-->`newGrades`<!--inline-NL-->, the final grade should be <!--plain-NL-->`N/A`<!--inline-NL-->.<!--plain-NL-->

You must use <!--plain-NL-->`filter`<!--inline-NL--> and <!--plain-NL-->`map`<!--inline-NL--> combined.<!--plain-NL-->

```
bob@dylan:~$ cat 4-main.js
import getListStudents from "./0-get_list_students.js";
import updateStudentGradeByCity from "./4-update_grade_by_city.js";

console.log(updateStudentGradeByCity(getListStudents(), "San Francisco", [{ studentId: 5, grade: 97 }, { studentId: 1, grade: 86 }]));

console.log(updateStudentGradeByCity(getListStudents(), "San Francisco", [{ studentId: 5, grade: 97 }]));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 4-main.js 
[
  {
    id: 1,
    firstName: 'Guillaume',
    location: 'San Francisco',
    grade: 86
  },
  { id: 5, firstName: 'Serena', location: 'San Francisco', grade: 97 }
]
[
  {
    id: 1,
    firstName: 'Guillaume',
    location: 'San Francisco',
    grade: 'N/A'
  },
  { id: 5, firstName: 'Serena', location: 'San Francisco', grade: 97 }
]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `4-update_grade_by_city.js`


---
### 5. Typed Arrays

Create a function named <!--plain-NL-->`createInt8TypedArray`<!--inline-NL--> that returns a new <!--plain-NL-->`ArrayBuffer`<!--inline-NL--> with an <!--plain-NL-->`Int8`<!--inline-NL--> value at a specific position.<!--plain-NL-->

It should accept three arguments: <!--plain-NL-->`length`<!--inline-NL--> (Number), <!--plain-NL-->`position`<!--inline-NL--> (Number), and <!--plain-NL-->`value`<!--inline-NL--> (Number).<!--plain-NL-->

If adding the value is not possible the error <!--plain-NL-->`Position outside range`<!--inline-NL--> should be thrown.<!--plain-NL-->

```
bob@dylan:~$ cat 5-main.js
import createInt8TypedArray from "./5-typed_arrays.js";

console.log(createInt8TypedArray(10, 2, 89));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 5-main.js 
DataView {
  byteLength: 10,
  byteOffset: 0,
  buffer: ArrayBuffer {
    [Uint8Contents]: <00 00 59 00 00 00 00 00 00 00>,
    byteLength: 10
  }
}
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `5-typed_arrays.js`


---
### 6. Set data structure

Create a function named <!--plain-NL-->`setFromArray`<!--inline-NL--> that returns a <!--plain-NL-->`Set`<!--inline-NL--> from an array.<!--plain-NL-->

It accepts an argument (Array, of any kind of element). <!--plain-NL-->

```
bob@dylan:~$ cat 6-main.js
import setFromArray from "./6-set.js";

console.log(setFromArray([12, 32, 15, 78, 98, 15]));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 6-main.js 
Set { 12, 32, 15, 78, 98 }
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `6-set.js`


---
### 7. More set data structure

Create a function named <!--plain-NL-->`hasValuesFromArray`<!--inline-NL--> that returns a boolean if all the elements in the array exist within the set.<!--plain-NL-->

It accepts two arguments: a <!--plain-NL-->`set`<!--inline-NL--> (Set) and an <!--plain-NL-->`array`<!--inline-NL--> (Array). <!--plain-NL-->

```
bob@dylan:~$ cat 7-main.js
import hasValuesFromArray from "./7-has_array_values.js";

console.log(hasValuesFromArray(new Set([1, 2, 3, 4, 5]), [1]));
console.log(hasValuesFromArray(new Set([1, 2, 3, 4, 5]), [10]));
console.log(hasValuesFromArray(new Set([1, 2, 3, 4, 5]), [1, 10]));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 7-main.js 
true
false
false
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `7-has_array_values.js`


---
### 8. Clean set

Create a function named <!--plain-NL-->`cleanSet`<!--inline-NL--> that returns a string of all the set values that start with a specific string (<!--plain-NL-->`startString`<!--inline-NL-->).<!--plain-NL-->

It accepts two arguments: a <!--plain-NL-->`set`<!--inline-NL--> (Set) and a <!--plain-NL-->`startString`<!--inline-NL--> (String). <!--plain-NL-->

When a value starts with <!--plain-NL-->`startString`<!--inline-NL--> you only append the rest of the string. The string contains all the values of the set separated by <!--plain-NL-->`-`<!--inline-NL-->. <!--plain-NL-->

```
bob@dylan:~$ cat 8-main.js
import cleanSet from "./8-clean_set.js";

console.log(cleanSet(new Set(['bonjovi', 'bonaparte', 'bonappetit', 'banana']), 'bon'));
console.log(cleanSet(new Set(['bonjovi', 'bonaparte', 'bonappetit', 'banana']), ''));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 8-main.js 
jovi-aparte-appetit

bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `8-clean_set.js`


---
### 9. Map data structure

Create a function named <!--plain-NL-->`groceriesList`<!--inline-NL--> that returns a map of groceries with the following items (name, quantity): <!--plain-NL-->

```
Apples, 10
Tomatoes, 10
Pasta, 1
Rice, 1
Banana, 5

```

Result:<!--plain-NL-->

```
bob@dylan:~$ cat 9-main.js
import groceriesList from "./9-groceries_list.js";

console.log(groceriesList());

bob@dylan:~$ 
bob@dylan:~$ npm run dev 9-main.js 
Map {
  'Apples' => 10,
  'Tomatoes' => 10,
  'Pasta' => 1,
  'Rice' => 1,
  'Banana' => 5
}
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `9-groceries_list.js`


---
### 10. More map data structure

Create a function named <!--plain-NL-->`updateUniqueItems`<!--inline-NL--> that returns an updated map for all items with initial quantity at 1.<!--plain-NL-->

It should accept a map as an argument. The map it accepts for argument is similar to the map you create in the previous task.<!--plain-NL-->

For each entry of the map where the quantity is 1, update the quantity to 100. 
If updating the quantity is not possible (argument is not a map) the error <!--plain-NL-->`Cannot process`<!--inline-NL--> should be thrown.<!--plain-NL-->

```
bob@dylan:~$ cat 10-main.js
import updateUniqueItems from "./10-update_uniq_items.js";
import groceriesList from "./9-groceries_list.js";

const map = groceriesList();
console.log(map);

updateUniqueItems(map)
console.log(map);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 10-main.js 
Map {
  'Apples' => 10,
  'Tomatoes' => 10,
  'Pasta' => 1,
  'Rice' => 1,
  'Banana' => 5
}
Map {
  'Apples' => 10,
  'Tomatoes' => 10,
  'Pasta' => 100,
  'Rice' => 100,
  'Banana' => 5
}
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_data_manipulation`
- File: `10-update_uniq_items.js`