We create a function and we assigned it to a variable:

```dart
void main() {

final sayHello = (name) => "Hello, $name";
print(sayHello("Salem"));
}
```

We can also pass a function as an argument to an another function:

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

We created a function called `welcome` that takes 2 arguments, the first one is a `Function` that takes a `String` as an argument and return a `String`, and the second argument is a `String` name, then we called the `welcome` function and passed it the `sayHello` argument that we did before.

But whats the point?, this could have been done with one simple function, I agree, but in the upcoming lessons it gonna make sense.
