# 0x01-ES6_promise

## Description

This project is a collection of JavaScript files that demonstrate the use of promises and error handling in an ES6 environment. It covers topics such as creating promises, handling resolved and rejected promises, working with multiple promises, and utilizing try-catch for error management.

## Setup

1. **Install NodeJS 12.11.x**

   In your home directory, run the following commands:

   ```bash
   curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
   sudo bash nodesource_setup.sh
   sudo apt install nodejs -y
   ```

   Verify the installation:

   ```bash
   nodejs -v
   npm -v
   ```

2. **Install Dependencies**

   In your project directory, install Jest, Babel, and ESLint using the supplied `package.json`:

   ```bash
   npm install
   ```

3. **Configuration Files**

   Add the following configuration files to your project directory:

   - `package.json`
   - `babel.config.js`
   - `.eslintrc.js`

## Usage

Each task in the project is represented by a separate JavaScript file. To run a specific task, use the following command:

```bash
npm run dev <filename>
```

For example:

```bash
npm run dev 0-main.js
```

## Task Details

### Task 0: Keep every promise you make and only make promises you can keep

This task introduces the concept of promises. It demonstrates creating a promise and checking if it is an instance of Promise.

### Task 1: Don't make a promise...if you know you can't keep it

This task involves creating a promise that resolves or rejects based on a boolean parameter.

### Task 2: Catch me if you can!

The task explores chaining handlers with promises. It logs a message when a promise is resolved.

### Task 3: Handle multiple successful promises

This task uses promises to simulate user profile signup and handles multiple promises to log the results.

### Task 4: Simple promise

This task introduces a simple promise that resolves with a predefined object.

### Task 5: Reject the promises

The task involves creating a promise that rejects with an error message based on the input.

### Task 6: Handle multiple promises

This task combines promises from previous tasks and logs the results after all promises are settled.

### Task 7: Load balancer

The loadBalancer function resolves with the value of the promise that resolves first among two given promises.

### Task 8: Throw error / try catch

This task introduces error handling with try-catch. It includes a function that throws an error when dividing by zero.

### Task 9: Throw an error

The task involves a function named `guardrail` that executes a given math function and logs the result or error messages.

## Response Data Format

The project includes utility functions `uploadPhoto` and `createUser` from the `utils.js` file. These functions return promises with specific response formats:

- `uploadPhoto`: `{ status: 200, body: 'photo-profile-1' }`
- `createUser`: `{ firstName: 'Guillaume', lastName: 'Salva' }`
