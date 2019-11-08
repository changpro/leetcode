# leetcode

## Noob的成长之路


### Two Sum
#### first solution(easy one):
```
class Solution(object):

    def twoSum(self, nums, target):

        if len(nums) < 2:

            pass

        r = []    

        for x in range(len(nums)): 

            minus = target - nums[x]

            if minus in r:

                return [x, nums.index(minus)]

            r.append(nums[x])

```

*整体思想：通过利用一个空数组将原数组中元素迭代，来验证target与原数组中元素的商是否已存在于另一数组，

*如否，则将该元素添加进另一数组。

*其中，时间复杂度为O(x^2).空间复杂度为O(1)



'''



#### second solution(using hash table)
```
d = {}

if len(nums)>1:

for i in enumerate(nums):

    if (target - num) in d :  

        return [d[target-num], i]

    d[num] = i        
```

**通过哈希查找，牺牲空间复杂度来换取更快的运行速度，其中，时间复杂度为O(n),空间复杂度为O（n）。**
