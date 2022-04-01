Like we always say, there is a shorter way.

Arrow functions, aka Fat arrow functions is an another way of writing functions, let's declare a function in the old way first:

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

We can define it like this:

```dart
int sum(int x, int y) => x + y;
```

This function does exactly the same thing as the previous one but written in the arrow notation.

As a conclusion, if you have a function body with only one statement, use the arrow notation.
