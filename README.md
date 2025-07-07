# Bootcamp Codes
- ✅ Armstrong Number
- ✅ Strong Number
- ✅ Perfect Number
- ✅ Prime Number
- ✅ Palindrome Number
- ✅ Spy Number
- ✅ Magic Number
## Armstrong Number
- **Armstrong Number**: Sum of its digits powered by the number of digits equals the number itself.
```
num = int(input("Enter a number: "))
temp = num
digits = 0

# Count digits
while temp > 0:
    digits += 1
    temp //= 10

temp = num
sum_of_powers = 0

while temp > 0:
    digit = temp % 10
    sum_of_powers += digit ** digits
    temp //= 10

if sum_of_powers == num:
    print("Armstrong Number")
else:
    print("Not an Armstrong Number")
```
## Strong Number
- **Strong Number**: Sum of factorials of digits equals the number.
```
num = int(input("Enter a number: "))
temp = num
sum_fact = 0

def factorial(n):
    f = 1
    for i in range(1, n+1):
        f *= i
    return f

while temp > 0:
    digit = temp % 10
    sum_fact += factorial(digit)
    temp //= 10

if sum_fact == num:
    print("Strong Number")
else:
    print("Not a Strong Number")
```
## Perfect Number
- **Perfect Number**: Sum of all its proper divisors equals the number.
```
num = int(input("Enter a number: "))
sum_divisors = 0

for i in range(1, num):
    if num % i == 0:
        sum_divisors += i

if sum_divisors == num:
    print("Perfect Number")
else:
    print("Not a Perfect Number")
```
## Prime Number
- **Prime Number**: A number greater than 1 with no divisors other than 1 and itself.
```
num = int(input("Enter a number: "))

if num <= 1:
    print("Not a Prime Number")
else:
    is_prime = True
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        print("Prime Number")
    else:
        print("Not a Prime Number")
```
## Palindrome Number
**Palindrome Number**: A number that reads the same backward. 
```
num = int(input("Enter a number: "))
temp = num
rev = 0

while temp > 0:
    digit = temp % 10
    rev = rev * 10 + digit
    temp //= 10

if rev == num:
    print("Palindrome Number")
else:
    print("Not a Palindrome Number")
```
## Sky Number
- **Spy Number**: A number whose sum of digits equals the product of its digits.
```
num = int(input("Enter a number: "))
temp = num
sum_digits = 0
prod_digits = 1

while temp > 0:
    digit = temp % 10
    sum_digits += digit
    prod_digits *= digit
    temp //= 10

if sum_digits == prod_digits:
    print("Spy Number")
else:
    print("Not a Spy Number")
```
## Magic Number
- **Magic Number**: A Magic Number is a number in which the recursive sum of digits equals 1.
```
num = int(input("Enter a number: "))
temp = num

# Function to find sum of digits
def digit_sum(n):
    total = 0
    while n > 0:
        total += n % 10
        n //= 10
    return total

# Keep summing digits until single digit
while temp > 9:
    temp = digit_sum(temp)

if temp == 1:
    print("Magic Number")
else:
    print("Not a Magic Number")
```
