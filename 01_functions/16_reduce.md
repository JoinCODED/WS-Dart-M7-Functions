The last method we will learn is the `reduce` method, which is used to combine all items inside a list into one item.

```dart
void main() {
    const numbers = [1, 2, 3, 4];
    final sum = numbers.reduce((number, element)=> number + element);
    print(sum);
}
```

The way this code works, is that reduce takes the first element `1` and assigns it to the `number` variable and then combine this value with all other `element`s using the combine logic that we wrote after the `=>` `number + element`.

It's not clear yet? let's get in the brain of dart:

at the first call, `number` is assigned the value of `1` and element is the value of `2`, then the logic we wrote `number + element` will result to `3`, the `3` will be stored on the `value` variable and on the second iteration the `element` will be assigned to the next number of the list which is `3`, the logic will run again to sum `3` and `3` and store the result in `number` and assign `element` the next value, so at this point `number` is `6` and `element` is `4`, the last iteration happens and the final result will be `10`.
