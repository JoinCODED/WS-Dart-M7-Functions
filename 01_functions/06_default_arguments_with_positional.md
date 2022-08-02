You can also use default arguments with positional arguments but with a slightly different syntax.

```dart
void main() {
    print(whoAteBurger("Salem"));
}
// positional arguments
String whoAteBurger(String name, [int burgers = 0]) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

We can also separate our arguments so that some of them are positional and some are named:

```dart
void main() {
    print(whoAteBurger("Salem",burgers: 5));
}
// mixed arguments
String whoAteBurger(String name, {required int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```
