[**Problem 42 - Coded Triangle Numbers**](https://projecteuler.net/problem=42)

![](/files/PythonGeneral/42.png)

```python
TNumbers = [1, 3, 6, 10, 15, 21, 28, 36, 45, 55, 66, 78, 91, 105, 120, 136, 153, 171, 190, 210]

def wordValue(word):
    word = word.upper()
    total = sum((ord(char) - ord('A') + 1) for char in word)
    return total

with open('words.txt', 'r') as file:
    content = file.read()
    words = content.split(',')
    

wordList = [word.strip('"') for word in words]

tWords = 0

for word in wordList:
  if wordValue(word) in TNumbers:
    tWords +=1 

print(tWords)
```

Gives an output of 162