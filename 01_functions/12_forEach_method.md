Now that we know how to declare functions and anonymous functions, we can learn some methods that works on collection which are in fact anonymous functions, so let's get started with our first method which is the `forEach` method:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
}
```

We have here a list of prices, and a discount amount of `5`, and we want to apply this discount on all our list elements, we learned to do this in a `for` loop before:

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

And we can accomplish the same thing using the `forEach` method:

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

And for the anonymous function, we can use any name we want:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    prices.forEach((anyName)=> print(anyName - discount));
}
```

And you can use a regular function expression with a function body instead of the arrow function:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    prices.forEach((anyName) {
        print(anyName - discount);
    });
}
```
