```py
def runningSum(self, nums: List[int]) -> List[int]:
    out = []
    total = 0
    for i in range(len(nums)):
        total += nums[i]
        out.append(total)
    return out
```


```py
def maxVowels(self, s: str, k: int) -> int:
        maximum = -inf
        letters =  {'a','e','i','o','u'}
        for i in range(len(s) - k):
            start = s[i]
            vowels = 0

            if start in letters:
                vowels += 1

            for j in range(1,k):
                slide = s[i+j + 1]
                if slide in letters:
                    vowels += 1
            
            maximum = max(maximum, vowels)
            
        return maximum
```