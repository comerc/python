[Задача Иосифа Флавия](https://ru.wikipedia.org/wiki/%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0_%D0%98%D0%BE%D1%81%D0%B8%D1%84%D0%B0_%D0%A4%D0%BB%D0%B0%D0%B2%D0%B8%D1%8F)

https://www.geogebra.org/m/ExvvrBbR

Решение №1

```py
n, k = int(input()), int(input())
l = list(range(1, n + 1))
i = 0
while len(l) > 1:
    i = (i + k - 1) % len(l)
    del l[i]
print(l[0])
```

Решение №2

```py
n = int(input())
k = int(input())
res = 0
for i in range(1, n+1):
    res = (res + k) % i
print(res + 1)
```

Решение №3

```py
n = list(range(1, int(input()) + 1))
k = int(input())
i = 0
while len(n) > 1:
    i += k - 1
    if i >= len(n):
        i %= len(n)
    n.pop(i)
print(*n)
```
