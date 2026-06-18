```js
function isAnagram(s, t) {
  if (s.length !== t.length) {
    return false;
  };
  const counts = {};
  for (let i = 0; i < s.length; i++) {
    counts[s[i]] = (counts[s[i]] || 0) + 1;
  };
  for (let i = 0; i < t.length; i++) {
    if (!counts[t[i]]) {
      return false;
    };
    counts[t[i]] -= 1;
  };
  return true;
};
```

```py
# sorted sol
def isAnagram(self, s: str, t: str) -> bool:
  if len(s) != len(t): return False
  s_sort = sorted(s)
  t_sort = sorted(t)
  for i in range(len(s_sort)):
    if s_sort[i] == t_sort[i]:
      pass
    else:
      return False
  return True

# freq counter sol
  def isAnagram(self, s: str, t: str) -> bool:
    if len(s) != len(t): return False
    count = {}
    for i in range(len(s)):
      count[s[i]] = (count.get(s[i]) or 0) +1
    for i in range(len(t)):
      if not count.get(t[i]):
        return False
      else:
        count[t[i]] -= 1
    return True
```