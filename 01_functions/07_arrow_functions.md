As we always say, there is a shorter way.

Arrow functions, aka Fat arrow functions, is another way of writing functions. Let's declare a function the old way first:

```dart
void main() {

}

int sum(int x, int y) {
        return x + y;
}
```

Because this function contains only one line:

```dart
    return x + y;
```

We can define it as follows:

```dart
int sum(int x, int y) => x + y;
```

The above function does exactly the same thing as the previous one but is written in the arrow notation.

In conclusion, if you have a function body with only one statement, use the arrow notation.
