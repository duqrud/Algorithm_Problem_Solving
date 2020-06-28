# 완주하지 못한 선수(collections)

```python
import collections

def solution(participant, completion):
    answer = collections.Counter(participant) - collections.Counter(completion)
    print(type(answer))
    return list(answer.keys())[0]
```

