Let's start by declaring a function:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    print("My name is $name and I ate $burgers burgers");
}
```

Suppose we want to use the above print statement multiple times but with different variables, for example:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    print("My name is $name and I ate $burgers burgers");
    const name2 = "Yanal";
    const burgers2 = 1;
    print("My name is $name2 and I ate $burgers2 burgers");
}
```

We have code duplication. The two print statements are almost identical, this is our biggest indication that we need to use a function instead:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    print("My name is $name and I ate $burgers burgers");
    const name2 = "Yanal";
    const burgers2 = 1;
    print("My name is $name2 and I ate $burgers2 burgers");
}

void whoAteBurger() {

}
```

Let's move our print statement inside the `whoAteBurger()` function body:

```dart
void whoAteBurger() {
    print("My name is $name and I ate $burgers burgers");
}
```

Oops! we got two errors, the `name` and `burgers` are undefined. The reason is that we defined those variables in the main method, but the `whoAteBurger` function doesn't know about them. We need to find a way to pass those variables to our function.

First, we need to prepare our function to be ready to accept two arguments:

```dart
void whoAteBurger(String name, int burgers) {
    print("My name is $name and I ate $burgers burgers");
}
```

Our errors went away, we declared two arguments by writing their type and name, and we separate them by a comma.

Now, we can replace the print statements in the main function with our `whoAteBurger` function:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    whoAteBurger(name, burgers);
    const name2 = "Yanal";
    const burgers2 = 1;
    print("My name is $name2 and I ate $burgers2 burgers");
}
```

We called our function and passed the variables to it that it needs, which are `name` and `burger`. We can do the same for the other print statements:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    whoAteBurger(name, burgers);
    const name2 = "Yanal";
    const burgers2 = 1;
    whoAteBurger(name2, burgers2);
}
```

Output:

```
My name is Laila and I ate 25 burgers
My name is Yanal and I ate 1 burger
```

When we call `whoAteBurger` with `name` and `burger`, they are set as function arguments:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    whoAteBurger(name, burgers);
}

void whoAteBurger("Laila", 25) {
    print("My name is Laila and I ate 25 burgers");
}
```

We got rid of the code duplication, but one other benefit is that if we want to update our print statement we can do it in one place instead of multiple places:

```dart
void whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

As you can see, it changed on both function calls, hence our code is more maintainable now.

We can also pass the arguments directly without declaring variables for them:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    whoAteBurger(name, burgers);
    const name2 = "Yanal";
    const burgers2 = 1;
    whoAteBurger(name2, burgers2);
    whoAteBurger("Salem", 5);
}
```

Output:

```
My name is Laila and I would like to order 25 burgers
My name is Yanal and I would like to order 1 burger
My name is Salem and I would like to order 5 burgers
```

You can pass variables, expressions, or literals as long as they are in the correct type and order.
