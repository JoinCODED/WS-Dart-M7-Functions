Until now, we've learned and used named functions. We can also declare anonymous functions. Let's see how:

```dart
void main() {

(name) => "Hello, $name";

}
```

This function takes a `string` as an argument and returns a string. The only difference between this function and the functions we wrote before is that this one has no name, but since it has no name, how can we use it?

We can assign this anonymous function to a variable:

```dart
void main() {

final sayHello = (name) => "Hello, $name";
print(sayHello("Salem"));
}
```

We created a variable that stores a reference to our anonymous function, and by calling this variable, we can call the anonymous function.

The way we called our variable is different, we called it with parentheses. Let's try to remove those parentheses:

```dart
void main() {

final sayHello = (name) => "Hello, $name";
print(sayHello);
}
```

Output:

```
Closure `main_closure`
```

Closure is another name of an anonymous function.
