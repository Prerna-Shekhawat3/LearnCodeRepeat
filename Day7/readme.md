
# 1759. Count Number of Homogenous Substrings

    class Solution(object):
      def countHomogenous(self, s):
          res=0
          l=r=0
          for r in range(len(s)):
              if s[l]==s[r]:
                  res+=r-l+1
              else:
                  res+=1
                  l=r
  
          return res %(10**9+7)



        
