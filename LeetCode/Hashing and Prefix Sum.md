
·       Two-sum, subarray sum = k, longest consecutive sequence

·       Prefix sums for range queries

```python
class Solution(object):

	def twoSum(self, nums, target):

         """
         :type nums: List[int]

         :type target: int

         :rtype: List[int]

         """

        seen = {}

        for i, num in enumerate(nums):

            complement = target - num

            if complement in seen:

               return (seen[complement], i)  # return indices

            seen[num] = i

        return None
```


```python
substring = []

        size = 0

        for char in s:

            if char in substring:

                if len(substring) > size : size = len(substring)

                substring = substring[substring.index(char)+1:]

                substring.append(char)

            else: substring.append(char)

        if size < len(substring): return len(substring)

        return size
```

