Let's start by declaring a function:

```dart
void main() {
    const name = "Laila";
    const burgers = 25;
    print("My name is $name and I ate $burgers burgers");
}
```

Suppose we want to do this print statement multiple times but with different variables, for example:

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

We have code duplication, the two print statements are almost identical, this is our biggest indication that we need to use a function instead:

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

After we declared a function, let's move our print statement inside the function body:

```dart
void whoAteBurger() {
    print("My name is $name and I ate $burgers burgers");
}
```

Oops, we got two errors, the `name` and `burgers` are undefined, the reason is that we defined those variables in the main method, but this function `whoAteBurger` does not know about them, we need to find a way to pass those variables to our function.

First, we need to prepare our function to be ready to accept two arguments:

```dart
void whoAteBurger(String name, int burgers) {
    print("My name is $name and I ate $burgers burgers");
}
```

Our errors went away, we declared two argument by writing their type and name, and we separate them by a comma.

Now we can call our function in the main method and replace the print statements:

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

We called our function and passed it the variables that it needs, which are `name` and `burger`. We can do the same for the other print statement:

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
My name is Yanal and I ate 1 burgers
```

So when we call `whoAteBurger` with `name` and `burger`, they are set as a function arguments:

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

We got rid of the code duplication, but one other benefit is that if we want to update out print statement we can do it in one place instead of multiple places:

```dart
void whoAteBurger(String name, int burgers) {
    print("My name is $name and I would like to order $burgers burgers");
}
```

As you can see, this changed on both function calls, hence our code is more maintainable now.

We can also pass the arguments directly without declaring a variables for them:

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
My name is Yanal and I would like to order 1 burgers
My name is Salem and I would like to order 5 burgers
```

So you can pass variables, expressions or literals as long as they are in the correct type and order.
