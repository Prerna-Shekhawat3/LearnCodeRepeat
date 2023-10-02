
## *2038. Remove Colored Pieces if Both Neighbors are the Same Color* ##
    
    class Solution(object):
        def winnerOfGame(self, colors):
            curr=0
            nex=0
            prev=0
            flag1=0
            flag2=0
            for i in range(1,len(colors)-1):
                curr=colors[i]
                nex=colors[i+1]
                prev=colors[i-1]
                if curr=='A' and prev=='A' and nex=='A':
                    flag1+=1

                elif curr=='B' and prev=='B' and nex=='B':
                    flag2+=1  

            return  flag1  > flag2 
    
## *13. Roman to integer* ##

    class Solution(object):
    def romanToInt(self, s):
        roman_to_int = {
            'I': 1,
            'V': 5,
            'X': 10,
            'L': 50,
            'C': 100,
            'D': 500,
            'M': 1000
        }
        
        total = 0
        prev_value = 0
        
        for char in reversed(s):
            value = roman_to_int[char]
            
            if value < prev_value:
                total -= value
            else:
                total += value
            
            prev_value = value
        
        return total

