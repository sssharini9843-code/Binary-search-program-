def binary_search_step_by_step(arr, target):
low = 0
high = len(arr) - 1
step = 1

print(f"Searching for {target} in sorted list: {arr}")

while low <= high:
mid = (low + high) // 2
print(f"Step {step}: Range [{low}-{high}], Middle Index: {mid} (Value: {arr[mid]})")
time.sleep(1.0)

if arr[mid] == target:
print(f" Match found at index {mid}!")
return mid
elif arr[mid] < target:
print(f"   {target} is larger than {arr[mid]}. Searching RIGHT half.")
low = mid + 1
else:
print(f"   {target} is smaller than {arr[mid]}. Searching LEFT half.")
high = mid - 1
step += 1

print(" Element not found.")
ret
# Example (Must be sorted)
sorted_data = [10, 20, 30, 40, 50, 60, 70, 80, 90]
binary_search_step_by_step(sorted_data, 70)

Output:
Searching for 70 in sorted list: [10, 20, 30, 40, 50, 60, 70, 80, 90]
Step 1: Range [0-8], Middle Index: 4 (Value: 50)
70 is larger than 50. Searching RIGHT half.
Step 2: Range [5-8], Middle Index: 6 (Value: 70)
Match found at index 6!


