## Longest Common Prefix

> Example 1:
Input: strs = ["flower","flow","flight"]
Output: "fl"

> Example 2:
Input: strs = ["dog","racecar","car"]
Output: ""
Explanation: There is no common prefix among the input strings.


```python
class Solution:
    def longestCommonPrefix(self, strs: List[str]) -> str:

        if not strs:
            return ""

        first = strs[0]

        for i, ch in enumerate(first):
            for word in strs[1:]:
                if i == len(word) or word[i] != ch:
                    return first[:i]
        return first
```
