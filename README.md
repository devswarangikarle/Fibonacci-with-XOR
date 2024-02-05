# Fibonacci-with-XOR
You're to update the fibunacci series by changing the function to -    f(n) = f(n-1) xor f(n-2), for n>1  f(0) = a  f(1) = b   Given a, b and n, find f(n).   Input Given three integers, a, b and n ( 0&lt;= a, b &lt;= 105) (1&lt;= n &lt;= 109) Output Print f(n).

def fibonacci_xor_optimized(a, b, n):
    if n == 0:
        return a
    elif n == 1:
        return b

    remainder = n % 3

    if remainder == 0:
        return a
    elif remainder == 1:
        return b
    else:  # remainder == 2
        return a ^ b


a, b, n = map(int, input().split())


result = fibonacci_xor_optimized(a, b, n)
print(result)
