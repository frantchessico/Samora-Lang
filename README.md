
# Samora Lang

Samora Lang is a simple and expressive programming language designed just for fun, mostly for learning purposes.


## Getting Started

To get started with Samora Lang, follow these steps:

1. Install the Samora Lang compiler and interpreter.

### Arch Linux
Using the Arch User Repository
```
$   yay -S samora-lang
```

2. Write your Samora Lang code in a text editor or an integrated development environment (IDE).
3. Save your Samora Lang code with a `.sml` extension.

## Hello, World!

To familiarize yourself with Samora Lang, here's a "Hello, World!" example:

```sml
print("Hello, World!");
```

## Read a file from the filesystem
```sml
let content = readFile("file.txt")
println(content)
```
## Write data to a file
```sml
let data = "This is some content"
writeFile("file.txt", data)
```
## Delete a file
```sml
deleteFile("file.txt")
```

## Create Directory
```sml
makeDir("path")
```
## Language Features

Samora Lang boasts the following key features:

### Recursion

Samora Lang supports recursion, allowing functions to call themselves. This enables the solution of problems that can be divided into smaller, similar subproblems. Recursive algorithms and data structures can be implemented efficiently in Samora Lang.

### Nested if Statements

Samora Lang allows for nested if statements, providing the ability to have conditional statements within other conditional statements. This grants developers more control over the flow of their programs by allowing multiple conditions to be evaluated in a structured and hierarchical manner.

### Closures

Closures in Samora Lang enable functions to access and manipulate variables defined outside their own scope. They capture the environment in which they are created, retaining access to variables and their values. This feature allows for the creation of functions that can "remember" and operate on specific data, even after exiting their original scope.

## Examples

Here are some examples to illustrate the usage of Samora Lang's features:

### Recursive Factorial Function

```sml
let factorial = fn(n) {
  if (n == 0) {
    1;
  } else {
    n * factorial(n - 1);
  }
};

let result = factorial(5);
print("The factorial of 5 is: ", result);
```

In this example, the `factorial` function calculates the factorial of a given number using recursion.

### Closure Example

```
let adder = fn(x) {
  fn(y) {
    x + y;
  };
};

let addTwo = adder(2);
let result = addTwo(3);
print("2 + 3 = ", result);
```

In this example, the `adder` function returns a closure that adds the provided value `x` to any value `y` passed to it. The closure `addTwo` adds 2 to its argument `3` and returns the result `5`.

### Single-line Comments Example

```sml
// This is a single-line comment.
# This is also a single-line comment.
```
### Array Example

```sml
let numbers = [1, 2, 3, 4, 5];
print(numbers[2]); 
```

In this example, an array `numbers` is created, and its third element (index 2) is accessed and printed.

### Hash (Dictionary) Example

```sml
let person = {"name": "John", "age": 25};
print(person["name"]);
```

In this example, a hash `person` is created with keys `"name"` and `"age"`. The value corresponding to the key `"name"` is accessed and printed.

### Map and Reduce Example
    ```sml
    let numbers = [1, 2, 3, 4, 5];
    let squared = map(numbers, fn(x) { x * x });
    let sum = reduce(squared, fn(acc, x) { acc + x }, 0);
    print("The sum of squared numbers is: ", sum);
    ```
## Contributing

Contributions to Samora Lang are welcome! If you find any issues, have ideas for improvements, or would like to add new features, please open an issue or submit a pull request on the official Samora Lang GitHub repository.

## License

Samora Lang

is released under the [MIT License](https://opensource.org/licenses/MIT).

## Acknowledgments

Samora Lang was inspired by various programming languages and their respective communities. We would like to express our gratitude to all the contributors and developers who have played a role in shaping programming languages and making them accessible to a wide audience.

## Contact

For any inquiries or questions, please contact the Samora Lang development team at [grahms@outlook.com]

---

Feel free to customize this README to include more details, provide installation instructions, and incorporate any other relevant information about your language.
