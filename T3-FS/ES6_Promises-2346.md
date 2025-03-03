# Project 2346: ES6 Promises
----


![1](2346_1.jpeg)

## Resources

**Read or watch**:

* [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
* [JavaScript Promise: An introduction](https://developers.google.com/web/fundamentals/primers/promises)
* [Await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
* [Async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
* [Throw / Try](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw)
## Learning Objectives

At the end of this project, you are expected to be able to[explain to anyone](https://fs.blog/feynman-learning-technique/),**without the help of Google**:

* Promises (how, why, and what)
* How to use the`then`,`resolve`,`catch`methods
* How to use every method of the Promise object
* Throw / Try
* The await operator
* How to use an`async`function
## Requirements

* All your files will be interpreted/compiled on Ubuntu 20.04 LTS using`node 20.x.x`and`npm 9.x.x`
* Allowed editors:`vi`,`vim`,`emacs`,`Visual Studio Code`
* All your files should end with a new line
* A`README.md`file, at the root of the folder of the project, is mandatory
* Your code should use the`js`extension
* Your code will be tested using`Jest`and the command`npm run test`
* Your code will be verified against lint using ESLint
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
* Install Babel using:`npm install --save-dev babel-jest @babel/core @babel/preset-env @babel/cli`
* Install ESLint using:`npm install --save-dev eslint`
## Files

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
### `utils.js`

Use when you get to tasks requiring`uploadPhoto`and`createUser`.Click to show/hide file contents`

### ``

``
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

## Response Data Format

`uploadPhoto`returns a response with the format

``
```
{
  status: 200,
  body: 'photo-profile-1',
}
```

`createUser`returns a response with the format

``
```
{
  firstName: 'Guillaume',
  lastName: 'Salva',
}
```

----
## Tasks
---
### 0. Keep every promise you make and only make promises you can keep

Return a Promise using this prototype <!--plain-NL-->`function getResponseFromAPI()`<!--inline-NL-->

```
bob@dylan:~$ cat 0-main.js
import getResponseFromAPI from "./0-promise.js";

const response = getResponseFromAPI();
console.log(response instanceof Promise);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 0-main.js 
true
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `0-promise.js`


---
### 1. Don't make a promise...if you know you can't keep it

Using the prototype below, return a <!--plain-NL-->`promise`<!--inline-NL-->. The parameter is a <!--plain-NL-->`boolean`<!--inline-NL-->.<!--plain-NL-->

```
getFullResponseFromAPI(success)

```

When the argument is:<!--plain-NL-->

- `true`

resolve the promise by passing an object with 2 attributes:


`status`: `200`
`body`: `'Success'`
- resolve the promise by passing an object with 2 attributes:


`status`: `200`
`body`: `'Success'`
- `status`: `200`
- `body`: `'Success'`
- `false`

reject the promise with an error object with the message `The fake API is not working currently`
- reject the promise with an error object with the message `The fake API is not working currently`

- resolve the promise by passing an object with 2 attributes:


`status`: `200`
`body`: `'Success'`
- `status`: `200`
- `body`: `'Success'`

- `status`: `200`
- `body`: `'Success'`

- reject the promise with an error object with the message `The fake API is not working currently`

Try testing it out for yourself<!--plain-NL-->

```
bob@dylan:~$ cat 1-main.js
import getFullResponseFromAPI from './1-promise';

console.log(getFullResponseFromAPI(true));
console.log(getFullResponseFromAPI(false));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 1-main.js 
Promise { { status: 200, body: 'Success' } }
Promise {
  <rejected> Error: The fake API is not working currently
    ...
    ...
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `1-promise.js`


---
### 2. Catch me if you can!

Using the function prototype below<!--plain-NL-->

```
function handleResponseFromAPI(promise)

```

Append three handlers to the function:<!--plain-NL-->

- When the Promise resolves, return an object with the following attributes


`status`: `200`
`body`: `success`
- `status`: `200`
- `body`: `success`
- When the Promise rejects, return an empty `Error` object
- For every resolution, log `Got a response from the API` to the console

- `status`: `200`
- `body`: `success`

```
bob@dylan:~$ cat 2-main.js
import handleResponseFromAPI from "./2-then";

const promise = Promise.resolve();
handleResponseFromAPI(promise);

bob@dylan:~$ 
bob@dylan:~$ npm run dev 2-main.js 
Got a response from the API
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `2-then.js`


---
### 3. Handle multiple successful promises

In this file, import <!--plain-NL-->`uploadPhoto`<!--inline-NL--> and <!--plain-NL-->`createUser`<!--inline-NL--> from <!--plain-NL-->`utils.js`<!--inline-NL-->

Knowing that the functions in <!--plain-NL-->`utils.js`<!--inline-NL--> return promises, use the prototype below to collectively resolve all promises and log <!--plain-NL-->`body firstName lastName`<!--inline-NL--> to the console.<!--plain-NL-->

```
function handleProfileSignup()

```

In the event of an error, log <!--plain-NL-->`Signup system offline`<!--inline-NL--> to the console<!--plain-NL-->

```
bob@dylan:~$ cat 3-main.js
import handleProfileSignup from "./3-all";

handleProfileSignup();

bob@dylan:~$ 
bob@dylan:~$ npm run dev 3-main.js 
photo-profile-1 Guillaume Salva
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `3-all.js`


---
### 4. Simple promise

Using the following prototype<!--plain-NL-->

```
function signUpUser(firstName, lastName) {
}

```

That returns a resolved promise with this object:<!--plain-NL-->

```
{
  firstName: value,
  lastName: value,
}

```

```
bob@dylan:~$ cat 4-main.js
import signUpUser from "./4-user-promise";

console.log(signUpUser("Bob", "Dylan"));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 4-main.js 
Promise { { firstName: 'Bob', lastName: 'Dylan' } }
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `4-user-promise.js`


---
### 5. Reject the promises

Write and export a function named <!--plain-NL-->`uploadPhoto`<!--inline-NL-->. It should accept one argument <!--plain-NL-->`fileName`<!--inline-NL--> (string). <!--plain-NL-->

The function should return a Promise rejecting with an Error and the string <!--plain-NL-->`$fileName cannot be processed`<!--inline-NL-->

```
export default function uploadPhoto(filename) {

}

```

```
bob@dylan:~$ cat 5-main.js
import uploadPhoto from './5-photo-reject';

console.log(uploadPhoto('guillaume.jpg'));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 5-main.js 
Promise {
  <rejected> Error: guillaume.jpg cannot be processed
  ..
    ..
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `5-photo-reject.js`


---
### 6. Handle multiple promises

Import <!--plain-NL-->`signUpUser`<!--inline-NL--> from <!--plain-NL-->`4-user-promise.js`<!--inline-NL--> and <!--plain-NL-->`uploadPhoto`<!--inline-NL--> from <!--plain-NL-->`5-photo-reject.js`<!--inline-NL-->.<!--plain-NL-->

Write and export a function named <!--plain-NL-->`handleProfileSignup`<!--inline-NL-->. It should accept three arguments <!--plain-NL-->`firstName`<!--inline-NL--> (string), <!--plain-NL-->`lastName`<!--inline-NL--> (string), and <!--plain-NL-->`fileName`<!--inline-NL--> (string). The function should call the two other functions. When the promises are all settled it should return an array with the following structure:<!--plain-NL-->

```
[
    {
      status: status_of_the_promise,
      value: value or error returned by the Promise
    },
    ...
  ]

```

```
bob@dylan:~$ cat 6-main.js
import handleProfileSignup from './6-final-user';

console.log(handleProfileSignup("Bob", "Dylan", "bob_dylan.jpg"));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 6-main.js 
Promise { <pending> }
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `6-final-user.js`


---
### 7. Load balancer

Write and export a function named <!--plain-NL-->`loadBalancer`<!--inline-NL-->. It should accept two arguments <!--plain-NL-->`chinaDownload`<!--inline-NL--> (Promise) and <!--plain-NL-->`USDownload`<!--inline-NL--> (Promise).<!--plain-NL-->

The function should return the value returned by the promise that resolved the first.<!--plain-NL-->

```
export default function loadBalancer(chinaDownload, USDownload) {

}

```

```
bob@dylan:~$ cat 7-main.js
import loadBalancer from "./7-load_balancer";

const ukSuccess = 'Downloading from UK is faster';
const frSuccess = 'Downloading from FR is faster';

const promiseUK = new Promise(function(resolve, reject) {
    setTimeout(resolve, 100, ukSuccess);
});

const promiseUKSlow = new Promise(function(resolve, reject) {
    setTimeout(resolve, 400, ukSuccess);
});

const promiseFR = new Promise(function(resolve, reject) {
    setTimeout(resolve, 200, frSuccess);
});

const test = async () => {
    console.log(await loadBalancer(promiseUK, promiseFR));
    console.log(await loadBalancer(promiseUKSlow, promiseFR));
}

test();

bob@dylan:~$ 
bob@dylan:~$ npm run dev 7-main.js 
Downloading from UK is faster
Downloading from FR is faster
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `7-load_balancer.js`


---
### 8. Throw an error

Write a function named <!--plain-NL-->`divideFunction`<!--inline-NL--> that will accept two arguments: <!--plain-NL-->`numerator`<!--inline-NL--> (Number) and <!--plain-NL-->`denominator`<!--inline-NL--> (Number).<!--plain-NL-->

When the <!--plain-NL-->`denominator`<!--inline-NL--> argument is equal to 0, the function should throw a new error with the message <!--plain-NL-->`cannot divide by 0`<!--inline-NL-->. Otherwise it should return the numerator divided by the denominator.<!--plain-NL-->

```
export default function divideFunction(numerator, denominator) {

}

```

```
bob@dylan:~$ cat 8-main.js
import divideFunction from './8-try';

console.log(divideFunction(10, 2));
console.log(divideFunction(10, 0));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 8-main.js 
5
..../8-try.js:15
  throw Error('cannot divide by 0');
  ^
.....

bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `8-try.js`


---
### 9. Throw error / try catch

Write a function named <!--plain-NL-->`guardrail`<!--inline-NL--> that will accept one argument <!--plain-NL-->`mathFunction`<!--inline-NL--> (Function).<!--plain-NL-->

This function should create and return an array named <!--plain-NL-->`queue`<!--inline-NL-->. <!--plain-NL-->

When the <!--plain-NL-->`mathFunction`<!--inline-NL--> function is executed, the value returned by the function should be appended to the queue. 
If this function throws an error, the error message should be appended to the queue. 
In every case, the message <!--plain-NL-->`Guardrail was processed`<!--inline-NL--> should be added to the queue. <!--plain-NL-->

Example:<!--plain-NL-->

```
[
  1000,
  'Guardrail was processed',
]

```

```
bob@dylan:~$ cat 9-main.js
import guardrail from './9-try';
import divideFunction from './8-try';

console.log(guardrail(() => { return divideFunction(10, 2)}));
console.log(guardrail(() => { return divideFunction(10, 0)}));

bob@dylan:~$ 
bob@dylan:~$ npm run dev 9-main.js 
[ 5, 'Guardrail was processed' ]
[ 'Error: cannot divide by 0', 'Guardrail was processed' ]
bob@dylan:~$ 

```

**Repo:**

- GitHub repository: `atlas-web_back_end`
- Directory: `ES6_promise`
- File: `9-try.js`