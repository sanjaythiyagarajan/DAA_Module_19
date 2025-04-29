# EX 1B Merge Sort
## DATE: 22/02/25
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm

1. Start

2. Read an integer n (number of elements).

3. Read n elements into the array arr.

4. Print the given array.

5. Call mergesort(arr, 0, n-1):

   If left < right:

       a) Find middle = (left + right) // 2
   
       b) Recursively sort the right half: mergesort(arr, middle + 1, right)

       c) Merge the two halves (left to middle, middle+1 to right) using the merge procedure.

6. In merge(arr, left, middle, right):

   a) Create two temporary arrays L and R.

   b) Copy data into L and R.

   c) Compare elements from L and R and merge them back into arr in sorted order.

7. Print the sorted array.

8. End

## Program:

Program to implement Merge Sort

Developed by: SANJAY T

Register Number: 212222110039

```PY
def merge(arr,left,middle,right):
    n1 = middle - left + 1
    n2 = right - middle
    L = [0] * n1
    R = [0] * n2
    for i in range(n1):
        L[i] = arr[left + i]
    for j in range(n2):
        R[j] = arr[middle + 1 + j]
    i = j = 0
    k = left
    
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i+=1
        else:
            arr[k] = R[j]
            j+=1
        k+=1
    while i < n1:
        arr[k] = L[i]
        i+=1
        k+=1
    while j < n2:
        arr[k] = R[j]
        j+=1
        k+=1
        
def mergesort(arr,left,right):
    if left < right:
        middle = (left + right)//2
        mergesort(arr, middle+1, right)
        merge(arr, left, middle, right)
        
def print_sort(arr):
    for i in range(len(arr)):
        print(arr[i],end=' ')

n = int(input())
arr = [int(input()) for _ in range(n)]

print("Given array is")
print_sort(arr)
mergesort(arr,0,n-1)
print("\n\nSorted array is")
print_sort(arr)
```

## Output:

![image](https://github.com/user-attachments/assets/15f6bb7c-9d1c-4b0e-8219-d29e151de2ac)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
