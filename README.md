# This is a journal of me learning javascript

# Dated 18 jul, 2026:

## 05:43AM
I am currently following supersimpledev's JavaScript tutorial. 


Done watching 2hrs out of 22, did the challenge question 4i4j.


This will take some time, cs50W will probably be paused for more than just a weeks.


But i am learning a lot, notes are below.



## Notes :

### Floating point rounding error:

In the IEEE 754 representation of floating numbers, the mantissa field has a finite no of bits.  
So, when representing decimal numbers like 0.1, 0.2 etc which has non terminating(infinitely recurrent) binary representations it rounds them and stores the nearest representable value.  

These rounding and approximations causes error in resultants during arithmetic operations like:

    0.1 + 0.2 = 0.30000000000000004 rather than exactly 0.3.


### Best practice when calculating money :

Use integers.  
Calculate as cents/paise instead of dollar/rupees.  
Because using float can cause errors.

### Type coercion:

Javascript can implicitly convert data types.

```JavaScript
x = 'hello' + 5 ;
```
If we print x we get a **string** 'hello5'. 

### Template strings:

```javascript
`hello`;
```
Features:
1. Interpolation
```JavaScript
`the price is : ${2+2}`;
```
2. Multiline Strings
```JavaScript 
`This is a 
multi line string.
it does not need escape characters to
add new line.`;
```

### Why do we add `<script>` towards the end of `<body>` tag?
1. The browser loads the page from top to bottom. If we place script at the top the browser will stop loading and execute it.
It will increase the loading time.

2. The DOM availability: By placing the script at the end we ensure that all the objects are parsed before the script utilizes the DOM.


# Dated 19 jul. 2026:

## Notes:

### Naming conventions: camelCase

When naming a variable capitalize every first letter of a word except in the first word.

eg:
        variableOne, cartQuantity, totalAmount.


### Ways to declare variables:


1. ***const***: Used when variable type and value should not be changed. Used by default.

2. ***let***: Used when const can not be used or when variables can later be changed.

3. ***var***(Not recommended): It was used in all JavaScript code before 2015.



### Equality 

1. Loose equality(==): Converts the data types first before comparing their values.

```Javascript  
5=='5' //this is true because the string '5' is converted to number 5 before comparing

```

2. Strict equality(===): Doesn't perform type coersion.

```Javascript  
5=='5' //this is False because no type coersion happens.
```

