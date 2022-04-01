Functions are the way to organize our code and make it more reuseable.

So far, we have been adding our code in the main method, but as our code goes larger, we want to organize our code and break it into smaller blocks.

Just like we used variables to store values and reference them multiple times, we can use functions to encapsulate a block of code and reuse multiple times.

Let's create our first function:

```dart
void main() {

}

void helloWorld() {
    print("Hello World!");
    print("My first function");
}
```

In the code above, we declared our main function, we started by declaring the return type (more on that later), then the function name `helloWorld` a set of parenthesis and a set of curly braces, and within the curly braces is what we call a function body, where we write all the code we want to execute when this function is called.

Let's call our function in the main method by typing it's name and a set of parenthesis:

```dart
void main() {
helloWorld();
}

void helloWorld() {
    print("Hello World!");
    print("My first function");
}
```

Output:

```
Hello World!
My first function
```

Call the function again and let's see what happens:

```dart
void main() {
helloWorld();
helloWorld();
}

void helloWorld() {
    print("Hello World!");
    print("My first function");
}
```

Output:

```
Hello World!
My first function
Hello World!
My first function
```

We defined a simple function with a set of instruction, in our case they are print statements, and whenever we call our function, those set of functions will be executed.
