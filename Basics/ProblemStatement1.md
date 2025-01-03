## Basics: Problem Statement - 1
Given a number n, check whether it is even or odd. Return true for even and false for odd.
## Possible Solution in JS - 1

We can check the remainder when divided by 2. If the remainder is 0, the number is even; otherwise, it is odd.

```
function isEven(n) { 
    return (n % 2 == 0); 
}
    let n = 101;
    if (isEven(n)) {
        console.log("true");
    } else {
        console.log("false");
    }
```
## Possible Solution in JS - 2

Using Bitwise AND operator : The last bit of all odd numbers is always 1, while for even numbers it’s 0. So, when performing bitwise AND operation with 1, odd numbers give 1, and even numbers give 0.

Ex:5 (101)  -> 101
                    &  001
                       =
                       001 , so this we can say it is an odd number.

```
function isEven(n) {
 if ((n & 1) === 0) {
        return true;
    } else {
        return false;
    }
}
let n = 101;
if (isEven(n)) {
    console.log("true");
} else {
    console.log("false");
}
```

## Possible Solution in JS - 3

Using Bitwise Shift operator


```
function isEven(n) {
    if (n == (n >> 1) << 1) 
       return true;
    else 
       return false;
}
let n = 4;
if (isEven(n)) {
    console.log("true");
} else {
    console.log("false");
}
```


