# #50 - Recursive Implementation of Pow(x, n)

- **Striver's A2Z Topic:** 7.1: Get a Strong Hold
- **Date:** Thu, Oct 22, 2026
- **Blueprint Day:** Day 10

## Description & Notes

This problem can be solved in a recursive Manner.   
First we take the n value.   
lets assume n is positive.   
The main Logic here is. **if n==0 we return 1**  
if n divisible by 2 then we simply square the x value and divide n by 2.  
if n is not divisible by 2 then we simply multiply the curr value with x and decrement the power in recursive manner.   

continue further in a recursive manner.   
**The Code:**  
 double mypow(double x, long long n){  
        if(n==0){  
        return 1;  
    }  
    if(n%2!=0){  
        return x* mypow(x,n-1);  
    }  
    else{  
        return mypow(x*x,n/2);**Here we are decrementing power and we are increasing  squaring  value. It results in same answer **  
    }  
     }  
    double myPow(double x, int n) {  
        long long  int N=n;  
        if(n< 0) {  
            N=-N;  
            return 1.0/mypow(x,N);  
        }  
        return mypow(x,N);  
    }  

**Note:**  
we have written Two functions here in case for negative values,   
Incase of negative values we simply take the whole  value /1 and we remove the negative value of N  
Read the Code carefully for clear understanding...  
