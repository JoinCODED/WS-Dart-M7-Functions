Our next method is used to filter items within a list, and it's called the `where` method.

```dart
void main() {
    const prices = [10, 25, 20, 5, 18, 30];
}
```

We want to get a list that contains all prices which are more than `15` using the `where` method:

```dart
void main() {
    const prices = [10, 25, 20, 5, 18, 30];
    final highPrices = prices.where((price) => price > 15);
    print(highPrices);
}
```

Output:

```
(25, 20, 18, 30)
```

The `where` method works just like `.map`, but we usually write a condition that if evaluated to `true`, it will keep the element, and if evaluated to `false`, it will discard the element.
