Now that we know how to declare functions and anonymous functions, we can learn some methods that work on a collection, which are anonymous functions.

Let's get started with our first method, the `forEach` method:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
}
```

Here, we have a list of prices and a discount amount of `5`, and we want to apply this discount to all our list elements.

We learned to do this in a `for` loop before:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    for(var price in prices) {
        print(price - discount);
    }
}
```

Output:

```
5
20
10
```

We can accomplish the same result using the `forEach` method:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    prices.forEach((price)=> print(price - discount));
}
```

Output:

```
5
20
10
```

Have you noticed something? `(price)=> print(price - discount)` this is an anonymous function that is passed as an argument to the `forEach` method!

For the anonymous function, we can use any name we want:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    prices.forEach((anyName)=> print(anyName - discount));
}
```

You can use a regular function expression with a function body instead of the arrow function:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    prices.forEach((anyName) {
        print(anyName - discount);
    });
}
```
