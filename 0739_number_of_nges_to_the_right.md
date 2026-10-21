# #739 - Number of NGEs to the right

- **Striver's A2Z Topic:** 9.3: Monotonic Stack & Queue
- **Date:** Wed, Oct 21, 2026
- **Blueprint Day:** Day 9

## Description & Notes

This problem is Same as the next greater Element. 
Same stack operations but here we deal with indexes and save the difference of indexes in the result array. 
The Code:
 vector<int> dailyTemperatures(vector<int>& temperatures) {
        vector<int>res(temperatures.size(),0);
        stack<int>st;
        for(int i=temperatures.size()-1; i>=0;i--){
            int curr_index=i;
            while(!st.empty()&&temperatures[st.top()]<= temperatures[curr_index]){
                st.pop();
            }
            if(!st.empty()){
                res[curr_index]=st.top()-curr_index;
            }
            st.push(curr_index);
        }
        return res;
Once check the Code.
