

# 1535. Find the Winner of an Array Game

    class Solution(object):
    def getWinner(self, arr, k):
        current_max = arr[0]
        consecutive_wins = 0

        for i in range(1, len(arr)):
            if arr[i] > current_max:
                current_max = arr[i]
                consecutive_wins = 1
            else:
                consecutive_wins += 1

            if consecutive_wins == k:
                return current_max

        return current_max

# 744. Find Smallest Letter Greater Than Target

    class Solution(object):
    def nextGreatestLetter(self,letters, target):
        res=None
        for letter in letters:
            if letter>target:
                res=letter
                break

        return res if res else letters[0]

# 34. Find First and Last Position of Element in Sorted Array

    class Solution(object):
    def searchRange(self, nums, target):
        first,last=-1,-1

        for i in range(len(nums)):
            if nums[i]==target:
                if first==-1:
                    first=i
                last=i
        
        return([first,last])

        
