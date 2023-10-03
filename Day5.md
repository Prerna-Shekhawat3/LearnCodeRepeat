
# 1572. Matrix Diagonal Sum

## Approach-1 ##
    class Solution(object):
    def diagonalSum(self, mat):
        sum=0
        for i in range(len(mat)):
            for j in range(len(mat)):
                if i+j==(len(mat)-1):
                    sum+=mat[i][j]
                elif i==j:
                    sum+=mat[i][j]

        return sum

## Approach-2 ##
       
    class Solution(object):
        def diagonalSum(self, mat):
            sum=0
            rows=len(mat)
            cols=len(mat[0])

        for i in range(rows*cols):
            row=i//cols
            col=i%cols

            if row==col:
                sum+=mat[row][col]

            elif row+col==(rows-1):
                sum+=mat[row][col]

        return sum


# 1512. Number of Good Pairs

        
    def good_pair(arr):
        count = {}
        res = 0

    for num in arr:
        print(f"Num {num}")
        if num in count:
            res += count[num]
            print(f"{num} {res} {count[num]}")
            count[num] += 1
        else:
            count[num] = 1

    return res
        
