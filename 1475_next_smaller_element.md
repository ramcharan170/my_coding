# #1475 - Next Smaller Element

- **Striver's A2Z Topic:** 9.3: Monotonic Stack & Queue
- **Date:** Tue, Oct 20, 2026
- **Blueprint Day:** Day 8

## Description & Notes

it is similar to the next greater Element in the stack operation. 
But the problem comes here is association with the same number Twice. 
It can be solved with the mapping of the index to the number we preferred I mean (the next smaller Element).

The code: vector<int> finalPrices(vector<int>& prices) {
        stack<int>st;
        vector<int>output;
        unordered_map<int,int>map;
        for(int i=prices.size()-1;i>=0;i--){
            int current=prices[i];
            while(!st.empty()&& st.top()>current ){
                st.pop();
            }
            if(!st.empty()){
                map[i]=st.top();
            }
            else{
                map[i]=0;
            }
            st.push(current);
        }
        for(int i=0;i<prices.size();i++){
            output.push_back(prices[i]-map[i]);
        }
        return output;
    }
Check This. out.
