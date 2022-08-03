There are two different ways of declaring function arguments. The first one we used was with `positional arguments`. The way positional arguments work is by declaring the arguments between the parentheses.

When we call the `whoAteBurger` function, Dart knows that the first argument passed will be `name` and the second argument will be `burgers`.

```dart
void main() {
    whoAteBurger("Salem", 5);
}
// positional arguments
String whoAteBurger(String name, int burgers) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Each argument is identified by its position between the parentheses.

This function only has two arguments. However, what if we have 8 or 10 arguments? It will be a hassle to memorize all the positions to be able to pass the arguments correctly, and this is were named arguments came in handy.

How do named arguments work?

To define a named argument, we simply wrap our arguments in curly braces:

```dart
void main() {
    whoAteBurger("Salem", 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

We got an error because we passed positional arguments to our function that expects named arguments. To fix this, we have to add the name of the argument before each value:

```dart
void main() {
    whoAteBurger(name: "Salem", burgers: 5);
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Now, we can position our argument the way we want and it will still work, for example:

```dart
void main() {
    whoAteBurger(burgers: 5, name: "Salem");
}
// named arguments
String whoAteBurger({String name, int burgers}) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

<!-- You said that the code will work above, then, you tell them that we got error? This will frustrate the students and they won't trust you anymore 😛 -->

Hmm, we got an error, let's fix it in the next lesson.
