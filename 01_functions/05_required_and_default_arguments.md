Named arguments by default are not required unlike positional arguments, this is why you got an error with this code:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

And the error tells you that the argument `name` and `burgers` can't be `null`.

To solve this, we have 3 possible options:

1. Declare nullable types, by adding a question mark after each argument as we learned before:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String? name, int? burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

But this doesn't seem like a good solution, we don't want our function to run if it doesn't have all arguments it needs.

2. Use default values, by providing default values, they replace the passed argument if it was `null`.

```dart
void main() {
    print(whoAteBurger(name: "Salem"));
}
// named arguments
String whoAteBurger({String name = '', int burgers = 0}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Because we omitted the `burgers` argument, it will resolve to 0 by default and we will get this output:

```
My name is Salem and I would like to order 0 burgers
```

So you can use default values if the arguments are optional, but what if our code can't run without all arguments provided?

3. Mark arguments as **required**, by adding the required keyword before the argument, dart will make sure to not compile unless you provided it with the correct arguments:

```dart
void main() {
    print(whoAteBurger(name: "Salem", burgers: 5));
}
// named arguments
String whoAteBurger({required String name,required int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```
