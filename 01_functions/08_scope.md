What is a scope?

A scope is a block of code that is written inside curly braces:

```dart
void main() {
// scope A
}

sum(int y,int x){
// scope B
}
```

If we define a variable in scope A, it will be only accessible within scope A, and can't be called or accessed in other scopes.

```dart
void main() {
    // scope A
const name = "salem";
print(name); // this is valid, because i'm using `name` in the same scope that i defined it in
}

sum(int y,int x){
// scope B
print(name); // this will give an error, because `name` was defined in scope A and i'm using it in scope B
}
```

Let's add a third scope:

```dart
void main() {
// scope A
const a = 8;
if (a > 5){
    const b = 3;
    // scope C
    print(b); // this is valid, because i defined `b` in Scope C and used it in Scope C
    print(a); // this is also valid, because the scope C inherits all variables from the parent scope A
}

}

sum(int y,int x){
// scope B
}
```

In conclusion, as long as we are trying to use a variable within the same scope or the parent scope, we will have no errors.

We can define multiple variables with the same name as long as they are in different scopes, for example:

```dart
void main() {
// scope A
const a = 8;
if (a > 5){
    const a = 3;
    // scope C
    print(a); // this will print `3` because Dart will look for the definition in the closest scope possible
}
}
```

Those are all local scopes because they are within the main function.

We also have a global scope that lives outside the main function:

```dart
// global scope
const c = 6;
void main() {
// scope A
const a = 8;
if (a > 5){
    const a = 3;
    // scope C
    print(a); // this will print `3` because Dart will look for the definition in the closest scope possible
}
}
```

Because the variable `c` is defined in the global scope, it can be accessed anywhere.
