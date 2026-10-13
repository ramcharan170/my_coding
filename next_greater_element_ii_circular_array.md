# Next Greater Element II (Circular array)

- **Striver's A2Z Topic:** 9.3: Monotonic Stack & Queue
- **Date:** Tue, Oct 13, 2026
- **Blueprint Day:** Day 1

## Description & Notes

Here first we take the double sized array. 
we first initialize all the values of the output to -1. 
and then we start iterating one by one in the array.
Here we deal with the indexes rather than Elements.

We check the stack is empty or not and then if the nums[stack.top()]<nums[curr_index] the output[stack.top()]=nums[curr_index]
For the Element finding of the Last element we iterate the array through Second Time but we actually add the elements into  the stack only for the first iteration.
So by the last the one thats left is the greatest Element and that has the output default value of -1. Rest of all the values Has the greatest Element value. 

Code:
vector<int> nextGreaterElements(vector<int>& nums) {
        vector<int>nums2(nums);
        sort(nums2.begin(), nums2.end());
        stack<int>st;
        int n=nums2.size();

        vector<int>output(n,-1);
        for(int i=0;i<2*n;i++){
            int curr_index=i%n;
            while(!st.empty()&&nums[st.top()]<nums[curr_index]){
                output[st.top()]=nums[curr_index];
                st.pop();
            }
This is the main Logic Check multiple times..
            if(i<n){
                st.push(curr_index);
            }
        }
        return output;
        
        
    }
