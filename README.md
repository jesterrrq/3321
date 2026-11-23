from functools import lru_cache

@lru_cache(None)
def f(n):
    if n <= 13:
        return 1
    return 2 * (n - 3) * f(n - 2)

print(f(int(input())))
