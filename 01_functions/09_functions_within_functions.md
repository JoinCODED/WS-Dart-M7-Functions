So far, we have declared our functions out side the main function, but dart also supports declaring functions within a function:

```dart
void main() {
// scope A
const a = 8;
sum(int y,int x) {
    // scope B
    return a + y + x;
}
sum(5,6);
}
```

And now, `sum` and `main` share the variable `a`!, please note that `sum` here is called an `inner function`.
