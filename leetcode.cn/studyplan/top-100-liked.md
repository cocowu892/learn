287.寻找重复数
---------------

给定一个包含 n+1个整数的数组 nums其数字都在[1，n〕范围内(包括1 和 n)，可知至少存在一个重复的整数。假设 nums 只有 一个重复的整数 ，返回 
这个重复的数你设计的解决方案必须 不修改 数组 nums 且只用常量级 0(1)的额外空间。

解答
--------------------
class Solution:
    def findDuplicate(self, nums: List[int]) -> int:
        backup=list.copy(nums)
        list.sort(backup)
        for i in range(len(nums)+1):
            if backup[i]==backup[i+1]:
                return backup[i]
