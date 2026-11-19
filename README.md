# Prime Number Checker

A small Node.js utility that checks whether an integer is a prime number.

## Features

- Checks whether a provided integer is prime
- Handles numbers below 2, `2`, even numbers, and odd composite numbers
- Uses trial division up to the square root of the input
- Exports the `isPrime` function for use in other Node.js modules

## Installation

Requires [Node.js](https://nodejs.org/).

Install dependencies:

```bash
npm install
```

## Usage

### Import the function

```js
const { isPrime } = require("./index");

console.log(isPrime(2));  // true
console.log(isPrime(7));  // true
console.log(isPrime(10)); // false
console.log(isPrime(1));  // false
```

### Run the application

```bash
node index.js
```

## How it works

The `isPrime` function applies the following rules:

1. Numbers less than `2` are not prime.
2. `2` is prime.
3. Any other even number is not prime.
4. For odd numbers, it checks divisibility by odd integers from `3` up to the square root of the input.
5. If any divisor is found, the number is composite; otherwise, it is prime.

Example:

```js
isPrime(9); // false, because 9 is divisible by 3
isPrime(11); // true
```

## API

### `isPrime(num)`

Checks whether `num` is a prime number.

| Parameter | Type     | Description                  |
|-----------|----------|------------------------------|
| `num`     | `number` | The integer number to check. |

| Return value | Description                                  |
|--------------|----------------------------------------------|
| `true`       | The number is prime.                         |
| `false`      | The number is not prime or is less than `2`. |

## Testing

Run the test suite with:

```bash
npm test
```

## Project structure

```text
.
├── index.js
├── package.json
├── LICENSE
└── README.md
```

## License

This project is licensed under the [MIT License](LICENSE).
