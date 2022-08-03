Functions are a way to organize our code and make it reusable.

So far, we have been adding our code in the primary method, but as our code gets larger, we want to organize it and break it into smaller blocks.

Just like we used variables to store values and reference them multiple times, we can use functions to encapsulate a block of code and reuse it multiple times.

Let's create our first function:

```dart
void main() {

}

void helloWorld() {
    print("Hello World!");
    print("My first function");
}
```

In the code above, we declared our main function. we created another function by declaring the return type (more on that later), the function name `helloWorld`, parentheses, and curly braces. Between the curly braces is what we call a function body, where we write all the code we want to execute when this function is called.

Let's call our function in the main method by typing its name and parentheses:

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

We defined a simple function with a set of instructions, which are print statements. Those print statements will be executed whenever we call our function `helloWorld()`.
