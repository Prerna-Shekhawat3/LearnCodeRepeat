
# *Two Sum* #

    class Solution(object):
      def twoSum(self,num, target):
          for i in range(0,len(num)-1):
              for j in range(i+1,len(num)):
                  if num[i]+num[j]==target:
                      return [i,j]
  
          
# *Reverse words of a String* #

    class Solution(object):
    def twoSum(self,num, target):
        for i in range(0,len(num)-1):
            for j in range(i+1,len(num)):
                if num[i]+num[j]==target:
                    return [i,j]

        
# *Palindrome Number* #

    class Solution(object):
    def isPalindrome(self,x):
        org_x=x
        rem=0
        new_x=0
        while(x>0):
            rem=x%10
            x=x//10
            new_x=new_x*10+rem
        if org_x==new_x:
            return True
        else:
            return False


        
