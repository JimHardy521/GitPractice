[**Problem 25 - 1000th Digit Fibonacci Number**](https://projecteuler.net/problem=25)

![](/files/PythonGeneral/25.png)

```python
List = [1,1]

while len(str(List[-1]))<=1000:
  List.append(List[-1] + List[-2])

Print(len(List))

```