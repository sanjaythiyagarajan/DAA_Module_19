# EX 1C Quick Sort
## DATE: 25/02/25
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of string values.

## Algorithm

1. Start

2. Read an integer n (number of elements).

3. Read n elements into array arr.

4. Call quickSort(arr, 0, n):

5. If the number of elements (end - start) is more than 1:

6. Find the pivot position by calling partition(arr, start, end).

7. Recursively sort the left part: quickSort(arr, start, pivot_index).

8. Recursively sort the right part: quickSort(arr, pivot_index + 1, end).

9. In partition(arr, start, end):

10. Choose the first element as the pivot.

11. Set two pointers i (start+1) and j (end-1).

12. Move i right while arr[i] <= pivot.

13. Move j left while arr[j] >= pivot.

14. If i <= j, swap arr[i] and arr[j].

15. If i > j, swap pivot arr[start] with arr[j] and return j as the pivot's final position.

16. After sorting, print the sorted array.

17. End


## Program:

Program to implement implement quick sort using the last element as pivot on the list of string values.

Developed by: SANJAY T

Register Number: 212222110039

```PY
def quickSort(alist, start, end):
    if end - start > 1:
        p = partition(alist, start, end)
        quickSort(alist, start, p)
        quickSort(alist, p + 1, end)
 
def partition(alist, start, end):
    pivot = alist[start]
    i = start + 1
    j = end - 1
    #print("Pivot: ",pivot)
    while True:
        while (i <= j and alist[i] <= pivot):
            i = i + 1
        while (i <= j and alist[j] >= pivot):
            j = j - 1
 
        if i <= j:
            alist[i], alist[j] = alist[j], alist[i]
        else:
            alist[start], alist[j] = alist[j], alist[start]
            return j

arr = []
n=int(input())
for i in range(n):
    arr.append(input())
quickSort(arr, 0, n)
print("Sorted array is:")
for i in arr:
    print(i)
```

## Output:

![image](https://github.com/user-attachments/assets/2dbddd18-1b45-4b93-9411-0885928f27be)


## Result:
Thus the python program to implement quick sort using tha last element as pivot on the list of string values is successfully executed.
