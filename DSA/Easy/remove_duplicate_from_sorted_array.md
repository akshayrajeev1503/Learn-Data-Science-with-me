## Remove duplicates from sorted array
> Need to modify the input array in place
> Solution: Check previoud and current element, if same -> replace it with new pointer
```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        if not nums:
            return 0
        j = 1  # Pointer for next unique position
        for i in range(1, len(nums)):
            if nums[i] != nums[i-1]:
                nums[j] = nums[i]
                j += 1
        return j
```
