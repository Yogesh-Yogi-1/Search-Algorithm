# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
Developed by:V. Yogesh
RegisterNumber: 23013930

def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k=eval(input())
n=len(array)
array.sort()
res=linearSearch(array,n,k)
if(res==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",  res)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Developed by:V. Yogesh
RegisterNumber: 23013930

def binarySearch(array, k, low, high):
    while low<=high:
        mid=low+(high)
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array = eval(input())
k=eval(input())
n=len(array)
array.sort()
res=binarySearch(array,k,0,len(array)-1)
if(res==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",  res)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Developed by: V. Yogesh
RegisterNumber: 23013930

def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
           return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
            return BinarySearch(array,k,mid+1,high)
    else:
        return -1
array = eval(input())
k=eval(input())
array.sort()
res=BinarySearch(array,k,0,len(array)-1)
if(res==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",  res)
```
## Sample Input and Output
## OUTPUT
![output](/Screenshot%202023-12-13%20205619.png)
![output](/Screenshot%202023-12-13%20205805.png)
![output](/Screenshot%202023-12-13%20205848.png)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.