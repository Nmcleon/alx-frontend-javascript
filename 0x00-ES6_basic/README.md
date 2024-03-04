# alx-frontend-javascript

## Setup

### Install NodeJS 12.11.x

In your home directory, run the following commands:

```bash
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs -y
```

Verify the installation:

```bash
nodejs -v
# Output should be: v12.11.1

npm -v
# Output should be: 6.11.3
```

### Install Jest, Babel, and ESLint

In your project directory, install Jest, Babel, and ESLint using the provided `package.json`:

```bash
npm install
```

### Configuration files

Add the following files to your project directory:

#### `package.json`

<details>
<summary>Click to show/hide file contents</summary>

```json
{
  "name": "alx-frontend-javascript",
  "version": "1.0.0",
  "description": "ES6 Basic Concepts",
  "main": "index.js",
  "scripts": {
    "test": "jest",
    "dev": "babel-node"
  },
  "keywords": ["ES6", "JavaScript"],
  "author": "Your Name",
  "license": "MIT",
  "dependencies": {
    "babel-cli": "^6.26.0",
    "babel-preset-env": "^1.7.0"
  },
  "devDependencies": {
    "babel-jest": "^26.6.3",
    "eslint": "^7.21.0",
    "eslint-config-airbnb-base": "^14.2.1",
    "eslint-plugin-import": "^2.22.1",
    "jest": "^26.6.3"
  }
}
```
</details>

#### `babel.config.js`

<details>
<summary>Click to show/hide file contents</summary>

```javascript
module.exports = {
  presets: ['env'],
};
```
</details>

#### `.eslintrc.js`

<details>
<summary>Click to show/hide file contents</summary>

```javascript
module.exports = {
  extends: 'airbnb-base',
  plugins: ['import'],
  rules: {
    'no-console': 'off',
  },
};
```
</details>

## Finally...

Don't forget to run the following command from the terminal of your project folder to install all necessary project dependencies:

```bash
npm install
```

## Tasks

### 0. Const or let?

Modify `taskFirst` to instantiate variables using `const` and `taskNext` to instantiate variables using `let`.

```javascript
// 0-constants.js
export function taskFirst() {
  const task = 'I prefer const when I can.';
  return task;
}

export function getLast() {
  return ' is okay';
}

export function taskNext() {
  let combination = 'But sometimes let';
  combination += getLast();

  return combination;
}
```

### 1. Block Scope

Given what you’ve read about `var` and hoisting, modify the variables inside the function `taskBlock` so that the variables aren’t overwritten inside the conditional block.

```javascript
// 1-block-scoped.js
export default function taskBlock(trueOrFalse) {
  let task = false;
  let task2 = true;

  if (trueOrFalse) {
    task = true;
    task2 = false;
  }

  return [task, task2];
}
```

### 2. Arrow functions

Rewrite the following standard function to use ES6’s arrow syntax of the function `add` (it will be an anonymous function after).

```javascript
// 2-arrow.js
export default function getNeighborhoodsList() {
  this.sanFranciscoNeighborhoods = ['SOMA', 'Union Square'];

  this.addNeighborhood = (newNeighborhood) => {
    this.sanFranciscoNeighborhoods.push(newNeighborhood);
    return this.sanFranciscoNeighborhoods;
  };
}
```

### 3. Parameter defaults

Condense the internals of the following function to 1 line - without changing the name of each function/variable.

```javascript
// 3-default-parameter.js
export default function getSumOfHoods(initialNumber, expansion1989 = 89, expansion2019 = 19) {
  return initialNumber + expansion1989 + expansion2019;
}
```

### 4. Rest parameter syntax for functions

Modify the following function to return the number of arguments passed to it using the rest parameter syntax.

```javascript
// 4-rest-parameter.js
export default function returnHowManyArguments(...args) {
  return args.length;
}
```

### 5. The wonders of spread syntax

Using spread syntax, concatenate 2 arrays and each character of a string by modifying the function below.

```javascript
// 5-spread-operator.js
export default function concatArrays(array1, array2, string) {
  return [...array1, ...array2, ...string];
}
```

### 6. Take advantage of template literals

Rewrite the return statement to use a template literal.

```javascript
// 6-string-interpolation.js
export default function getSanFranciscoDescription() {
  const year = 2017;
  const budget = {
    income: '$119,868',
    gdp: '$154.2 billion',
    capita: '$178,479',
  };

  return `As of ${year}, it was the seventh-highest income county in the United States, with a per capita personal income of ${budget.income}. As of 2015, San Francisco proper had a GDP of ${budget.gdp}, and a GDP per capita of ${budget.capita}.`;
}
```

### 7. Object property value shorthand syntax

Modify the following function’s budget object to simply use the keyname instead.

```javascript
// 7-getBudgetObject.js
export default function getBudgetObject(income, gdp, capita) {
  const budget = {
    income,
    gdp,
    capita,
  };

  return budget;
}
```

### 8. No need to create empty objects before adding in properties

Rewrite the `getBudgetForCurrentYear` function to use ES6 computed property names on the budget object.

```javascript
// 8-getBudgetCurrentYear.js
function getCurrentYear() {
  const date = new Date();
  return date.getFullYear();
}

export default function getBudgetForCurrentYear(income, gdp, capita) {
  const budget = {
    [`income-${getCurrentYear()}`]: income,
    [`gdp-${getCurrentYear()}`]: gdp,
    [`capita-${getCurrentYear()}`]: capita,
  };

  return budget;
}
```

### 9. ES6 method properties

Rewrite `getFullBudgetObject` to use ES6 method properties in the `fullBudget` object.

```javascript
// 9-getFullBudget.js
import getBudgetObject from './7-getBudgetObject.js';

export default function getFullBudgetObject(income, gdp, capita) {
  const budget = getBudgetObject(income, gdp, capita);
  const fullBudget = {
    ...budget,
    getIncomeInDollars(in

come) {
      return `$${income}`;
    },
    getIncomeInEuros(income) {
      return `${income} euros`;
    },
  };

  return fullBudget;
}
```

### 10. For...of Loops

Rewrite the function `appendToEachArrayValue` to use ES6’s `for...of` operator.

```javascript
// 10-loops.js
export default function appendToEachArrayValue(array, appendString) {
  for (const value of array) {
    array[array.indexOf(value)] = appendString + value;
  }

  return array;
}
```

### 11. Iterator

Write a function named `createEmployeesObject` that will receive two arguments:

- `departmentName` (String)
- `employees` (Array of Strings)

The function should return an object with the following format:

```javascript
// 11-createEmployeesObject.js
export default function createEmployeesObject(departmentName, employees) {
  return {
    [departmentName]: employees,
  };
}
```

### 12. Let's create a report object

Write a function named `createReportObject` whose parameter, `employeesList`, is the return value of the previous function `createEmployeesObject`.

```javascript
// 12-createReportObject.js
export default function createReportObject(employeesList) {
  return {
    allEmployees: employeesList,
    getNumberOfDepartments(employeesList) {
      return Object.keys(employeesList).length;
    },
  };
}
```

### 13. Iterating through report objects

Write a function named `createIteratorObject`, that will take into argument a report Object created with the previous function `createReportObject`.

```javascript
// 100-createIteratorObject.js
export default function createIteratorObject(report) {
  let currentDepartmentIndex = 0;
  let currentEmployeeIndex = 0;

  return {
    next() {
      const departments = Object.keys(report.allEmployees);
      const currentDepartment = departments[currentDepartmentIndex];

      if (currentDepartmentIndex < departments.length) {
        const employees = report.allEmployees[currentDepartment];
        const currentEmployee = employees[currentEmployeeIndex];

        if (currentEmployeeIndex < employees.length) {
          currentEmployeeIndex += 1;
          return { value: currentEmployee, done: false };
        }

        currentDepartmentIndex += 1;
        currentEmployeeIndex = 0;
        return this.next();
      }

      return { done: true };
    },
  };
}
```

### 14. Iterate through object

Write a function named `iterateThroughObject`. The function’s parameter `reportWithIterator` is the return value from `createIteratorObject`.

```javascript
// 101-iterateThroughObject.js
export default function iterateThroughObject(reportWithIterator) {
  const result = [];
  let iteratorResult = reportWithIterator.next();

  while (!iteratorResult.done) {
    result.push(iteratorResult.value);
    iteratorResult = reportWithIterator.next();
  }

  return result.join(' | ');
}
```

## Test the Functions

To test the functions, you can use the provided test scripts for each task. For example:

```bash
npm run dev 0-main.js
npm run dev 1-main.js
# ...
npm run dev 101-main.js
```                      
