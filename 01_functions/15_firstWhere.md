The `firstWhere` method is used to find an element within a list, and it works just like `where`, but it only returns the first element that matches the condition:

```dart
void main() {
    const prices = [10, 25, 20, 5, 18, 30];
    final price = prices.firstWhere((price) => price > 15);
    print(price);
}
```

Output

```
25
```

Another example:

```dart
void main() {
    const names = ["Omar", "Laila", "Zainab", "Salem", "Ahmad"];
    final findOmar = names.firstWhere((name) => name == "Omar");
    print(findOmar);
}
```

Output:

```
Omar
```

We can add a second argument to the `firstWhere` method that gets executed if we don't find any item that matches the condition:

```dart
void main() {
    const names = ["Omar", "Laila", "Zainab", "Salem", "Ahmad"];
    final findMohammed = names.firstWhere((name) => name == "Mohammed",orElse: () => "This name is not within the list");
    print(findMohammed);
}
```

Output:

```
This name is not within the list
```
