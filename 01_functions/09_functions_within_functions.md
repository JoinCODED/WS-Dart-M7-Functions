So far, we've declared our functions outside the main function, but Dart also supports declaring functions within a function:

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

Now, `sum` and `main` share the variable `a`. Please note that `sum` here is called an `inner function`.
