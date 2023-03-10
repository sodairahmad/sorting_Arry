# sorting_Arry


A = [9,1,2,3,8,10,76,87,33,12]
def sortArray(A):
    if len(A) <= 1:
        return A 
    middle = len(A) // 2 
    left = sortArray(A[: middle])
    right = sortArray(A[middle:])
    merged = []
    while left and right:
        if left[0] <= right [0]:
            merged.append(left.pop(0))
        else:
            merged.append(right.pop(0))
                  
    merged.extend(right if right else left)
    return merged 
print(sortArray(A))


# END>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>..............................................>>>>>>>>>>>>>>>>




left = [9,1,2,3,8,10]
lis = [4,5,6,7,22,9,1,2,3,8,10,99]


def sort(lis):
    mid = len(lis) // 2 
    left = sorted(lis[:mid])
    right = sorted(lis[mid:])
    
    merged = []
    while min(len(left), len(right)) > 0 :
        if left[0] <= right[0]:
            insert = left.pop(0)
            merged.append(insert)
            
        elif left[0] >= right[0]:
            insert = right.pop(0)
            merged.append(insert)
            
    if len(left) > 0:
        for x in left:
            merged.append(x)
            
    if len(right) >0:
        for x in right:
            merged.append(x)
            
    return merged

print(sort(lis))
    
    
#print(merging(left, right))
 
 
#END.>>>>>>>>>>>>>>>>>>>>>>>>>......................................>>>>>>>>>>>>>>>>>>>>>>>>>>>>>



