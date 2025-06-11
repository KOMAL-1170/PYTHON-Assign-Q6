# PYTHON-Assign-Q6
import random

# Function to check if a number is prime
def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# Create list of 100 random numbers between 100 and 900
numbers = [random.randint(100, 900) for _ in range(100)]
print("Random Numbers:\n", numbers)

# (i) All odd numbers
odd_numbers = [num for num in numbers if num % 2 != 0]
print("\nOdd Numbers:", odd_numbers)
print("Count of Odd Numbers:", len(odd_numbers))

# (ii) All even numbers
even_numbers = [num for num in numbers if num % 2 == 0]
print("\nEven Numbers:", even_numbers)
print("Count of Even Numbers:", len(even_numbers))

# (iii) All prime numbers
prime_numbers = [num for num in numbers if is_prime(num)]
print("\nPrime Numbers:", prime_numbers)
print("Count of Prime Numbers:", len(prime_numbers))

