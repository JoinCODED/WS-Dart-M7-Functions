The next method we have is the `.map` method. We use it to take a collection and transform all of its items and return a new collection.

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    final pricesOnDiscount = prices.map((price) => price - discount);
    print(pricesOnDiscount);
}
```

Output:

```
(5, 20, 10)
```

Let's try to declare a type for our variable `pricesOnDiscount`:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    final List<int> pricesOnDiscount = prices.map((price) => price - discount);
    print(pricesOnDiscount);
}
```

We got an error:

```
 A value of type 'Iterable<int>' can't be assigned to a variable of type 'List<int>'
```

That's because the `.map` method returns an `Iterable`, not a list. We need to convert it back to a `list` using the `.toList()` method:

```dart
void main() {
    const prices = [10, 25, 15];
    const discount = 5;
    final List<int> pricesOnDiscount = prices.map((price) => price - discount).toList();
    print(pricesOnDiscount);
}
```
