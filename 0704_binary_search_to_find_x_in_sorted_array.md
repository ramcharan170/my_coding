# #704 - Binary Search to find X in sorted array

- **Striver's A2Z Topic:** 4.1: BS on 1D Arrays
- **Date:** Wed, Oct 14, 2026
- **Blueprint Day:** Day 2

## Description & Notes

Its just basic Binary Search Implementation.
Take low , Take high=nums.size()-1; 

Most Important In the loop  Dont forget to include the condition low<=high 
This is the Code for Checking:
int search(int* nums, int numsSize, int target) {
    int low=0;
    int high=numsSize-1;
    while(low<=high){
        int mid=(high+low)/2;
        if(nums[mid]==target)return mid;
        else if(
            nums[mid]<target
        ){
            low=mid+1;
        }
        else high=mid-1;
    }
    return -1;}
