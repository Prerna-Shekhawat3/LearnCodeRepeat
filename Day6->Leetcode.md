

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

# 14. Longest Common Prefix

    class Solution:
        def longestCommonPrefix(self, v):
            ans=""
            v=sorted(v)
            first=v[0]
            last=v[-1]
            for i in range(min(len(first),len(last))):
                if(first[i]!=last[i]):
                    return ans
                ans+=first[i]
            return ans 
        
    strs = ["flower","flow","flight"]
    s=Solution()
    print(s.longestCommonPrefix(strs))

# 706. Design HashMap

    
    class HashMap:
    
        def __init__(self):
            self.MAX=1000
            self.arr=[[] for _ in range(self.MAX)]
    
        def hashFunction(self,key):
            return key % self.arr
    
        def put(self,key,value):
            h=self.hashFunction(key)
            for i ,(k,v) in enumerate(self.arr[h]):
                if k == key:
                    self.arr[h][i]=(key,value)
                    return
                
            self.arr[h].append((key,value))
                
                
        def get(self,key):
            h=self.hashFunction(key)
            for (k,v) in self.arr[h]:
                if k==key:
                    return v
            return -1
        
    
        def remove(self,key):
            h=self.hashFunction(key)
            for i ,(k,v) in enumerate(self.arr[h]):
                if k ==key:
                    self.arr[h].pop(i)
                    return
