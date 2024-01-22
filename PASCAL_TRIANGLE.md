```py
n = 4
l = [1]
for i in range(n):
    res = [1]
    for j in range(1, len(l)):
        res.append(l[j - 1] + l[j])
        print(*res)
    res.append(1)
    l = res.copy()
print(l)
```
