# #496 - Next Greater Element I

- **Striver's A2Z Topic:** 9.3: Monotonic Stack & Queue
- **Date:** Mon, Oct 26, 2026
- **Blueprint Day:** Day 14

## Description & Notes

The next Greater element.<br>
Brute Force:<br>
Its just start iterating from the element in the array. and find the next Element through another loop in it <br>
```cpp
for(i=0;i<n;i++){
    for(j=i+1;j<n;j++){
        if(el>curr_el)
        nge of curr_el=el; }}
        
**The monotonic Stack approach**:
```
Imagine an array, if We want the next greater Element then we need to get a hold of the elements to the **right** not the **left**. <br>
So start the Pushing of elements in to the stack from the right. <br>

1. for the last there are no elements right, so the nge is -1,
**So basically we are trying to iterate the array from right to left.**<br>
upon iterating whatever Elemnts that are less than the current Element will be popped out. Only the Element greater than the current Element will be used for future use also. <br>

Imagine: <br>
```cpp
arr={1,3,2,6}; 
nge of 2=6;
nge of 3, In this Situation we just pop out 2 as 2 is less than 3; 
for nge of 1 we just give 3 as Even though 2 is greater than 1 It is left of 3. and doesnot contribute in the nge;

**The Code for This Problem is:**
vector<int> nge(vector<int> &arr){
    int n=arr.size();
    create array nge 
    vector<int>nge(n);    
    stack<int>st;
    st.push(n-1); Here we deal with Indexes for Easy use.
    for(int i=n-1;i>=0;i++){
        if(st.empty()) nge[i]=-1;
        while(arr[st.top()]<arr[i]){
            st.pop();}
        }
        else   nge[i]= nums[st.top()];}
        st.push(i); We just push This Element also in the end, For the next elements.
        return nge;
```

```cpp
    }
```
