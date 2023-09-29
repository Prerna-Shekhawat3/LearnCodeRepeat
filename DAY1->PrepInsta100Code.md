


# Codes of Recursion

## Power of a number


    def main():
      num=int(input("NUM: "))
      pow=int(input("POW: "))
      print(f"{num} power {pow} is {power_num(num,pow)}")


    def power_num(num,pow):
      if pow==0:
        return 1
      return num*power_num(num,pow-1)

    if __name__=="__main__":
    main()
    


## Prime Number


    def main():
      num=int(input("NUM: "))
      print("Prime" if is_prime(num,iter=2)==True else "NOT Prime")

    def is_prime(num,iter):
      if num==iter:
        return True
      if num<2:
        return False
      if num%iter==0:
        return False
    return is_prime(num,iter+1)

    if __name__=="__main__":
      main()


## Largest num of array

    def main():
      arr=list(map(int,input().split()))
      print(arr)
      print(f"Largest of arr : {largest_num_arr(arr,larg=arr[0],iter=0)}")

    def largest_num_arr(arr,larg,iter):
      if iter==len(arr):
        return larg
      if arr[iter]>larg:
        larg=arr[iter]
      return largest_num_arr(arr,larg,iter+1)

    if __name__=="__main__":
      main()

##Approach2

    def main():
    arr=list(map(int,input().split()))
    print(arr)
    print(f"Largest of arr : {largest_num_arr(arr,n=len(arr))}")

    def largest_num_arr(arr,n):
    if n==1:
        return arr[0]
    return max(arr[n-1],largest_num_arr(arr,n-1))

    if __name__=="__main__":
    main()


## Smallest element of array


    def main():
    arr=list(map(int,input().split()))
    print(arr)
    print(f"Largest of arr : {smallest_num_arr(arr,n=len(arr))}")

    def smallest_num_arr(arr,n):
    if n==1:
        return arr[0]
    return min(arr[n-1],smallest_num_arr(arr,n-1))

    if __name__=="__main__":
    main()


## Reversing a number


    def main():
    num=int(input("NUM: "))
    print(f"Reversed num: {reverse_num(num)}")

    def reverse_num(num,sum=0):
    if num==0:
        return sum
    rem=num%10
    sum=sum*10+rem
    return reverse_num(num//10,sum)
  
    if __name__=="__main__":
    main()

### Approach2 
  
    def main():
    num=int(input())
    arr=list(str(num))
    arr=revrse_num(arr,l=len(arr)//2)
    s=''
    print(s.join(arr))

    def revrse_num(arr, l, n=0):
    if n == l:
        return arr
    arr[n], arr[-1*(n+1)] = arr[-1*(n+1)], arr[n]
    return revrse_num(arr, l, n + 1)

    if __name__=="__main__":
    main()


## Program to calculate length of string

    str=input()

    def cal_len_str(str):
    if str=="":
        return 0
    return 1+ cal_len_str(str[1:])

    print(cal_len_str(str))

# Array problems

## Find largest elemnt of array


    arr=list(map(int,input().split()))

    for i in range(1,len(arr)):
        max=arr[0]
        small=arr[0]
        if arr[i]>max:
            max=arr[i]
        elif arr[i]<small:
            small=arr[i]
    print(f"Max is {max} \nMin is {small}")
    
    

## Find smallest elemnt of array

    arr=list(map(int,input().split()))
    
    def smallest_ele(arr):
    
        for i in range(len(arr)-1):
    
            for j in range(len(arr)-1-i):
    
                if arr[j]>arr[j+1]:
                    arr[j],arr[j+1]=arr[j+1],arr[j]
    
        return arr

    print(f"Smallest ele of {arr} is {smallest_ele(arr)} {arr[0]}")



## Find Second Smallest Element in an Array

    
    import math
    arr=[1, 10, 20, -4, -23, 100]
    
    def second_largest(arr):
        first=math.inf
        second=math.inf
    
        for i in range(len(arr)):
            if arr[i]<first:
                first=arr[i]
    
        for i in range(len(arr)):
            if arr[i] != first and arr[i] < second:
                second=arr[i]
        return second
    
    print(arr)
    print(second_largest(arr))
