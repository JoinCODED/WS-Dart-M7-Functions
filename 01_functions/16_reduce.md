The last method we will learn is the `reduce` method, which is used to combine all items inside a list into one item.

```dart
void main() {
    const numbers = [1, 2, 3, 4];
    final sum = numbers.reduce((number, element)=> number + element);
    print(sum);
}
```

The `reduce` method requires two arguments: The first one is called `total`, which is the initialValue, or the previously returned value of the function, and the second one is called `currentValue`, which is the value of the current element as shown below:

```dart
array.reduce((total, currentValue) => `the logic that we want to apply`)
```

In our example, the **total** (number) in the `reduce` method will be 0. The **currentValue** (element) will take the first element in the list, which is `1`. Then, the `number` and `element` will be combined , and the result will be `1`.

```dart
numbers.reduce((0, 1)=> 0 + 1) //  the returned value is 1
```

It's not clear yet? let's get into their brain of Dart:

At the first call, the first argument `number`, which represents the initial value of `reduce`, will be 0 by default if we don't assign a value to it.
The second argument `element`, which represents the `currentValue`, will be assigned to 1.
Then, the `reduce` method will apply an operation to them based on the logic we set, which, in our case, is addition.
The result of this iteration will be 1, and it will be stored in `number`.

In the next iteration, `number` will be 1, and `element` will take the second element in the list, which is 2. The two values will be combined, and result in 3, which will be stored in `number`.

```dart
numbers.reduce((1, 2)=> 1 + 2) //  the returned value is 3
```

Then, `number` will be 3, and `element` will take the third element in the list, which is 3. The two values will be combined, they will result in 6, and will be stored in `number` again.

```dart
numbers.reduce((3, 3)=> 3 + 3) //  the returned value is 6
```

The final iteration will happen, and the result will be 10.
