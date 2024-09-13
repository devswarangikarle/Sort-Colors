# Sort-Colors

Given an array nums with n objects colored red, white, or blue, sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white, and blue.
We will use the integers 0, 1, and 2 to represent the color red, white, and blue, respectively.
You must solve this problem without using the library's sort function.

class Solution:
    def sortColors(self, nums: List[int]) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        freq=[0]*3
        for x in nums: freq[x]+=1
        count=0
        for x in range(3):
            nums[count:count+freq[x]] = [x]*freq[x]
            count+= freq[x]

        
