We created a function and assigned it to a variable:

```dart
void main() {

final sayHello = (name) => "Hello, $name";
print(sayHello("Salem"));
}
```

We can also pass a function as an argument to another function:

```dart
void main() {

final sayHello = (name) => "Hello, $name";
welcome(sayHello,"Salem");
}

void welcome(String Function(String) greet, String name){
    print(greet(name));
    print("Welcome");
}
```

Output:

```
Hello, Salem
Welcome
```

We created a function called `welcome`. It takes two arguments, the first one is a `Function` that takes a `String` as an argument and returns a `String`, and the second one is a `String` name. Then, we called the `welcome` function and passed the `sayHello` argument to it.

What's the point?
This could've been done with one simple function, I agree. In the upcoming lessons, it's going to make sense.
