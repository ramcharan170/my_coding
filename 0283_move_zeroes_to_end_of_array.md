# #283 - Move Zeroes to End of Array

- **Striver's A2Z Topic:** 3.1: Arrays - Easy
- **Date:** Mon, Oct 26, 2026
- **Blueprint Day:** Day 14

## Description & Notes

The Code: <br>
Just Check it once No need For detailed Explanation.<br>
```cpp
void moveZeroes(vector<int>& nums) {
        int j=0;
        for(int i=0;i<nums.size();i++){
            if(nums[i]!=0){
                swap(nums[i],nums[j]);
                j++;
            }
        }
```
