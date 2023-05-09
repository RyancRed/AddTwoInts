# AddTwoInts
Adds 2 integers and outputs string sum

def add_strings(num1: str, num2: str) -> str:
    n1, n2 = len(num1), len(num2)
    if n1 < n2:
        num1 = '0' * (n2 - n1) + num1
    else:
        num2 = '0' * (n1 - n2) + num2
    carry, res = 0, ''
    for i in range(len(num1) -1, -1, -1):
        digit_sum = int(num1[i]) + int(num2[i]) + carry
        carry = 1 if digit_sum >= 10 else 0
        res += str(digit_sum - carry * 10)
    if carry:
        res += '1'
    return res[::-1]

num1 = '512'
num2 = '24'
result = add_strings(num1, num2)
print(result)
print("Abbas")_
