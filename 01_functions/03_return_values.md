Let's clean the code from the previous lesson:

```dart
void main() {
    whoAteBurger("Salem", 5);
}

void whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

The function we created does one thing, prints a statement, but we also can create functions that return a value.

Let's modify our function to return the string instead of printing it.

Right now, we have the `void` keyword just before our function name, which means that this function does not return anything. Let's change it to `String` because we will make it return a string!

```dart
void main() {
    whoAteBurger("Salem", 5);
}

String whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

As soon as we changed it, we got an error because we told Dart this function will return a `String`, but we did not return anything just yet. Let's add a return statement:

```dart
String whoAteBurger(String name, int burgers) {
   return "My name is $name and I would like to order $burgers burgers";
}
```

Now, this function returns a string, but we are not using it. If we run the code, we will get nothing printed.

We can use the returned value as follows:

```dart
void main() {
    final angryOrder = whoAteBurger("Salem", 5);
    print(angryOrder.toUpperCase());
}
```

Output:

```
MY NAME IS SALEM AND I WOULD LIKE TO ORDER 5 BURGERS
```
