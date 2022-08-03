Named arguments are required by default unlike positional arguments, this is why you got an error with this code:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

The error tells us that the arguments `name` and `burgers` can't be `null`.

To solve this, we have 3 possible options:

1. Declare nullable types by adding a question mark after each argument as we learned before:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String? name, int? burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

But this doesn't seem like a good solution, we don't want our function to run if it doesn't have all needed arguments.

1. Use default values. Default values replace the passed argument if it's `null`.

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

You can use default values if the arguments are optional, but what if our code can't run without all arguments provided?

3. Mark arguments as **required**. By adding the required keyword before each argument, Dart will make sure not to compile unless you provide it with the correct arguments:

```dart
void main() {
    print(whoAteBurger(name: "Salem", burgers: 5));
}
// named arguments
String whoAteBurger({required String name,required int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```
