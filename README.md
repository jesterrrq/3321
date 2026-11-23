n = int(input())

dp = [0] * (n + 1)
dp[n] = 1

for nuts in range(n, 0, -1):
    if nuts % 9 == 0:
        continue

    ways = dp[nuts]
    if ways == 0:
        continue

    dp[nuts - 1] += ways
