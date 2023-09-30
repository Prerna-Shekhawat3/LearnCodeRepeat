


# Calculate the sum of elements in an array

    
    arr=list(map(int,input().split()))
    
    def sum_arr(arr):
        sum=0
        for i in range(len(arr)):
            sum+=arr[i]
        return sum
    
    print(f"Sum of {arr} is {sum_arr(arr)}")
    

# Reverse an Array


    arr=list(map(int,input().split()))
    
    def rev_arr(arr):
        n=len(arr)
        for i in range(len(arr)//2):
            arr[i],arr[n-i-1]=arr[n-i-1],arr[i]
        return arr
    
    print(f"Reverse of {arr} is {rev_arr(arr)}")

## Approach 2

    arr=list(map(int,input().split()))
    
    def rev_arr(arr,start,end):
        if start >= end:
            return 
        arr[start],arr[end]=arr[end],arr[start]
        rev_arr(arr,start+1,end-1)
    
    rev_arr(arr,start=0,end=len(arr)-1)
    print(f"Reverse of {arr} is {arr}")
    

# Sort first half in ascending order and second half in descending order in an array

    arr=list(map(int,input().split()))
    
    def sort_arr(arr):
        for i in range(len(arr)):
    
            for j in range(len(arr)-1-i):
    
                if arr[j]>arr[j+1]:
    
                    arr[j],arr[j+1]=arr[j+1],arr[j]
    
        return arr
    
    sort_arr(arr)
    print(arr[:len(arr)//2+1])
    reversed_arr = arr[(len(arr)//2)+1:]
    print(arr[:len(arr)//2+1]+reversed_arr[::-1])

## Approach 2

    arr=list(map(int,input().split()))
    
    def print_half_asc_dsc(arr):
        arr.sort()
        i=0
        n=len(arr)
        while i<n/2:
            print(arr[i],end=' ')
            i=i+1
    
        j=n-1
        while j>n/2:
            print(arr[j],end=' ')
            j=j-1
    
    print(print_half_asc_dsc(arr))



# Finding the frequency of elements in an array 

    arr=list(map(int,input().split()))
    
    def freq_ele(ele):
        
        for i in arr:
            count=1
            if i==ele:
                count+=1
        return count
    
    visited=[]
    for i in range(len(arr)):
            if arr[i] in visited:
                continue
            else:
                 visited.append(arr[i])
    
    for i in range(len(visited)):
        print(f'Freq of {visited[i]} is {freq_ele(arr[i])}')


# Sorting elements of an array by frequency

    from collections import Counter
    
    arr=list(map(int,input().split()))
    
    count=Counter(arr)
    
    sorted_arr=sorted(arr, key=lambda x:(count[x],x))
    
    print(" ".join(map(str,sorted_arr)))


# Find the Longest Palindrome in an Array

    arr=list(map(int,input().split()))
    
    
    def is_palin(ele):
        if str(ele)[::-1]==str(ele):
            return True
    
    def max_palin(arr):
        max_len=0
        for i in range(len(arr)):
            if is_palin(arr[i])==True:
                if max_len<len(str(arr[i])):
                    max_len=len(str(arr[i]))
    
        return max_len,arr[i]
    
    print(max_palin(arr))


# Counting Distinct Elements in an Array 

    dist=[]
    arr=list(map(int,input().split()))
    
    def f_count(ele):
        count=0
        for i in range(len(arr)):
            if arr[i]==ele:
                count+=1
    
        return count
    
    for i in range(len(arr)):
        if f_count(arr[i])==1:
            dist.append(arr[i])
    
    print(dist)





