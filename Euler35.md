[**Problem 35 - Circular Primes**](https://projecteuler.net/problem=35)

![](/files/PythonGeneral/35.png)

```python
import math
max = 1000000

primeList = []

circularPrimeList = []

def isPrime(current_number):
  isPrime = True
  for i in range(2, int(current_number**0.5 + 1)):
    if current_number % (i) == 0:
      isPrime = False
  return isPrime

def isCircularPrime(primeList, number):
    number = str(number)
    for i in range(0, len(number)):
        rotatedNumber = number[i : len(number)] + number[0:i]
        if int(rotatedNumber) not in primeList:
            return False
    return True

for i in range(2,max):
  if isPrime(i) == True:
    primeList.append(i)

for i in primeList:
  if isCircularPrime(primeList, i) == True:
    circularPrimeList.append(i)
print(circularPrimeList)

```