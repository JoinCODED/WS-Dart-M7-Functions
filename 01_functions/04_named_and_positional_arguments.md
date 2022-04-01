Their are two different ways of declaring function arguments, the first one we used was with `positional arguments`, and the way positional arguments works, is that we declare them within the parenthesis and when we call the function, dart knows that the first argument passed will be `name` and the second argument will be `burgers`.

```dart
void main() {
    whoAteBurger("Salem", 5);
}
// positional arguments
String whoAteBurger(String name, int burgers) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Each argument is identified by it's position within the parenthesis.

This function only has two arguments, but what if we have 8 or 10 arguments, it will be a hassle to memorize all the positions to be able to pass the arguments correctly, and this is were named arguments came in handy.

So how do named arguments work?

To define a named argument we simply wrap our arguments in a set of curly braces:

```dart
void main() {
    whoAteBurger("Salem", 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

We got an error, because we passed positional arguments to our function that expects named arguments. to fix this by adding the name of the argument before each value:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

And now we can position our argument the way we want and it will still work, for example:

```dart
void main() {
    whoAteBurger(burgers: 5, name: "Salem");
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Hmm, we got an error, let's fix it in the next lesson.
