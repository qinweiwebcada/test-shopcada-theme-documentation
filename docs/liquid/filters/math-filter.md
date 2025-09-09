# Math Filter

### abs

Returns the absolute value of a number.

`abs` will also work on a string that only contains a number.

```
{{ -17 | abs }} // 17
{{ 4 | abs }} // 4
{{ "-19.88" | abs }} / 19.88
```

### at\_least

Limits a number to a minimum value.

```
{{ 4 | at_least: 5 }} // 4
{{ 4 | at_least: 3 }} // 5
```

### at\_most

Limits a number to a maximum value.

```
{{ 4 | at_most: 5 }} // 4
{{ 4 | at_most: 3 }} // 3
```

### ceil

Rounds an input up to the nearest whole number. Liquid tries to convert the input to a number before the filter is applied.

```
{{ 1.2 | ceil }} ==> 2
{{ 2.0 | ceil }} ==> 2
{{ 183.357 | ceil }} ==> 184
{{ "3.5" | ceil }} ==> 4
```

### divided\_by

Divides a number by another number. The result is rounded down to the nearest integer (that is, the floor) if the divisor is an integer.

```
{{ 16 | divided_by: 4 }} // 4
{{ 20 | divided_by: 7 }} // 2
{{ 20 | divided_by: 7.0 }} // 2.857142857142857
```

### floor

Rounds an input down to the nearest whole number. Liquid tries to convert the input to a number before the filter is applied.

```
{{ 1.2 | floor }} // 1
{{ 183.357 | floor }} // 183
{{ "3.5" | floor }} // 3
```

### minus

Subtracts a number from another number.

```
{{ 16 | minus: 4 }} // 12
{{ 183.357 | minus: 12 }} // 171.357
```

### modulo

Returns the remainder of a division operation.

```
{{ 24 | modulo: 7 }} // 3
{{ 183.357 | modulo: 12 }} // 3.357
```

### plus

Adds a number to another number.

```
{{ 16 | plus: 4 }} // 20
{{ 183.357 | plus: 12 }} // 195.357
```

### round

Rounds a number to the nearest integer or, if a number is passed as an argument, to that number of decimal places.

```
{{ 2.7 | round }} // 3
{{ 183.357 | round: 2 }} // 183.36
```

### times

Multiplies a number by another number.

```
{{ 24 | times: 7 }} // 168
{{ 183.357 | times: 12 }} // 2200.284
```

