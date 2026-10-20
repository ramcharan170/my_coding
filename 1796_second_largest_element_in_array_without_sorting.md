# #1796 - Second Largest Element in Array without sorting

- **Striver's A2Z Topic:** 3.1: Arrays - Easy
- **Date:** Tue, Oct 20, 2026
- **Blueprint Day:** Day 8

## Description & Notes

Its just basic Problem. 
but the optimal solution is the  one to Think. 
For this problem what is the basic one is that take an array separate the numbers and then find the largest and second largest. 
But the optimal approach is to check in the loop itself if the given character is a number or not. If its a number execute further steps in the loop or else, move to next iteration using "continue".

we can find the second and largest in the same iteration not in separate ones.
when we are updating the largest don't forget to update the second also. 
second=largest
largest=d; 
Code:

int secondHighest(string s) {
        int largest=-1;
        int second=-1;
        for(char c:s){
            if((c-'0') < 0 || (c-'0')>9) continue;
            int d=c-'0';
            if(d>largest){
                second=largest;
                largest=d;
            }
            else if(d<largest && d>second){
                second=d;
            }
        }
        return second;
    }
