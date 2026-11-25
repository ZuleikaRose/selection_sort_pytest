

def selection_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        # Assume the current position holds the minimum element
        min_idx = i
        
        # Iterate through the unsorted portion to find the true minimum
        for j in range(i + 1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
                
        # Swap the found minimum element with the first unsorted element
        if min_idx != i:
            arr[i], arr[min_idx] = arr[min_idx], arr[i]
            
    return arr

# Example usage
numbers = [64, 25, 12, 22, 11]
sorted_numbers = selection_sort(numbers)
print("Sorted list:", sorted_numbers)
