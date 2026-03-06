# Data-structure-partical-program-7
def linear(arr, key):
    for i in range(len(arr)):
        if arr[i] == key:
            return i
    return -1

def binary(arr, key):
    low = 0
    high = len(arr)-1
    while low <= high:
        mid = (low+high)/2
        if arr[mid] == key:
            return mid
        elif arr[mid] < key:
            low = mid+1
        else:
            high = mid-1
    return -1

arr = [10,20,30,40,50]
print linear(arr,30)
print binary(arr,30)
