# 11-02-26
from typing import List

class Solution:
    def containsDuplicate(self, nums: List[int]) -> bool:
        seen = set()

        for num in nums:
            if num in seen:
                return True
            seen.add(num)
        return False

        #
        class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        lookup={}
        for i in range(len(nums)):
            if nums[i] in lookup:
                return [lookup[nums[i]],i]
            else:
                lookup[target-nums[i]]=i
