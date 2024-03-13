# 0x03-ES6_data_manipulation

---

# ES6 Data Manipulation Project

This project demonstrates various data manipulation techniques using ES6 features in JavaScript, focusing on array methods like `map`, `filter`, and `reduce`, as well as data structures like `Set` and `Map`. The project is structured into several tasks, each showcasing a different aspect of data manipulation and ES6 features.

## Setup

To set up the project, follow these steps:

1. **Install NodeJS 12.11.x**:
   - Run the following commands in your terminal:
     ```bash
     curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
     sudo bash nodesource_setup.sh
     sudo apt install nodejs -y
     ```
   - Verify the installation by checking the versions:
     ```bash
     nodejs -v
     npm -v
     ```

2. **Install Jest, Babel, and ESLint**:
   - Navigate to your project directory and run:
     ```bash
     npm install
     ```
   - This command installs the necessary packages based on the `package.json` file.

## Configuration Files

The project includes the following configuration files:

- `package.json`: Lists project dependencies and scripts.
- `babel.config.js`: Configures Babel for transpiling ES6 code.
- `.eslintrc.js`: Configures ESLint for linting JavaScript code.

## Tasks

The project is divided into several tasks, each focusing on a specific data manipulation technique or ES6 feature:

1. **Basic List of Objects**: Create a function `getListStudents` that returns an array of student objects.
2. **More Mapping**: Create a function `getListStudentIds` that returns an array of student IDs.
3. **Filter**: Create a function `getStudentsByLocation` that filters students by location.
4. **Reduce**: Create a function `getStudentIdsSum` that sums up student IDs.
5. **Combine**: Create a function `updateStudentGradeByCity` that updates student grades based on city.
6. **Typed Arrays**: Create a function `createInt8TypedArray` that manipulates ArrayBuffer.
7. **Set Data Structure**: Create a function `setFromArray` that converts an array to a Set.
8. **More Set Data Structure**: Create a function `hasValuesFromArray` that checks if a Set contains all elements of an array.
9. **Clean Set**: Create a function `cleanSet` that filters and formats Set values.
10. **Map Data Structure**: Create a function `groceriesList` that returns a Map of groceries.
11. **More Map Data Structure**: Create a function `updateUniqueItems` that updates Map items with a specific condition.
12. **Weak Link Data Structure**: Implement a WeakMap to track API query counts and throw an error if the count exceeds a threshold.

## Running the Project

To run any of the tasks, use the following command:

```bash
npm run dev <task-file>.js
```

Replace `<task-file>` with the filename of the task you wish to run (e.g., `0-main.js`, `1-main.js`, etc.).

---                   
  
