# 정곤이의 단조 증가하는 수(SW)

```python
T = int(input())
for t in range(1,T+1):
    N = int(input())
    arr = list(map(int, input().split()))
    result = -1
    arr2 = set()
    for i in range(N-1):
        for j in range(1+i, N):
            arr2.add(str(arr[i] * arr[j]))
    for a in arr2:
        for i in range(len(a)-1):
            if a[i] > a[i+1]:
                break
        else:
            if int(a) > result:
                result = int(a)
    print(f'#{t} {result}')
```

