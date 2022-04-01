Let's clean the code from the previous lesson:

```dart
void main() {
    whoAteBurger("Salem", 5);
}

void whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

The function we created does one thing, prints a statement, but we also can create functions that returns a value.

Let's modify our function to return the string instead of printing it so we can do other things with this string.

Right now, we have the `void` keyword in front of our function name, which means that this function does not return anything, so let's change it to `String` because we will return a string!

```dart
void main() {
    whoAteBurger("Salem", 5);
}

String whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

As soon as we changed it we got an error, because we told dart this function will return a `String` but we did not return anything just yet. Let's add a return statement:

```dart
String whoAteBurger(String name, int burgers) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Now, this function returns a string, but we are not using it, and if we run the code, we will get nothing printed.

In order to use the returned value:

```dart
void main() {
    final angryOrder = whoAteBurger("Salem", 5);
    print(order.toUpperCase());
}
```

Output:

```
MY NAME IS SALEM AND I WOULD LIKE TO ORDER 5 BURGERS
```
