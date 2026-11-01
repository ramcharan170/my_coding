# 453: minimum moves to equal array elements.

- **Striver's A2Z Topic:** 1.1: Things to Know in C++ / Basics
- **Date:** Sun, Nov 1, 2026
- **Blueprint Day:** Day 20

## Description & Notes

In This problem we are required to increment the remaining n-1 values of array by one so that all the elements are Equal. <br>
Lets Check the following: **incrementing one by one of all n-1 values is relatively similar to decrementing the other Value **<br>

So if we check in that intution. What is the best possible value in the array we can decrement it so that all elements are Equal, <br>
Its the minimum value of the array.<br>

So the difference in the Each value to the minimum value are the steps taken by that particular value to reach that minimum value. <br>

```cpp
So just add up the relative difference of the other values to the minimum value. and return the sum.
```
