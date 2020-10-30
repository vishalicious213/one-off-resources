# mutateTheArray

Given an integer n and an array a of length n, your task is to apply the following mutation to a:

* Array a mutates into a new array b of length n.
* For each i from 0 to n - 1, b[i] = a[i - 1] + a[i] + a[i + 1].
* If some element in the sum a[i - 1] + a[i] + a[i + 1] does not exist, it should be set to 0. For example, b[0] should be equal to 0 + a[0] + a[1].

Example
```
For n = 5 and a = [4, 0, 1, -2, 3], the output should be mutateTheArray(n, a) = [4, 5, -1, 2, 1].

b[0] = 0 + a[0] + a[1] = 0 + 4 + 0 = 4
b[1] = a[0] + a[1] + a[2] = 4 + 0 + 1 = 5
b[2] = a[1] + a[2] + a[3] = 0 + 1 + (-2) = -1
b[3] = a[2] + a[3] + a[4] = 1 + (-2) + 3 = 2
b[4] = a[3] + a[4] + 0 = (-2) + 3 + 0 = 1

So, the resulting array after the mutation will be [4, 5, -1, 2, 1].
```

```python
def mutateTheArray(n, a):
```

## Tests
```
Input:
n: 5
a: [4, 0, 1, -2, 3]

Expected Output:
[4, 5, -1, 2, 1]
```
```
Input:
n: 1
a: [9]

Expected Output:
[9]
```
```
Input:
n: 4
a: [1, 2, 3, 4]

Expected Output:
[3, 6, 9, 7]
```
```
Input:
n: 9
a: [-9, -8, 7, 7, 7, 6, -6, 4, 6]

Expected Output:
[-17, -10, 6, 21, 20, 7, 4, 4, 10]
```
```
Input:
n: 10
a: [6, -5, -5, 5, 10, 5, 1, 8, 6, -2]

Expected Output:
[1, -4, -5, 10, 20, 16, 14, 15, 12, 4]
```
```
Input:
n: 10
a: [1, 10, 10, -6, 5, -3, -7, 10, 9, 10]

Expected Output:
[11, 21, 14, 9, -4, -5, 0, 12, 29, 19]
```
```
Input:
n: 4
a: [-6, -5, -7, -1]

Expected Output:
[-11, -18, -13, -8]
```
```
Input:
n: 8
a: [-4, -5, 0, -6, -5, -4, -7, 9]

Expected Output:
[-9, -9, -11, -11, -15, -16, -2, 2]
```
```
Input:
n: 1
a: [-5]

Expected Output:
[-5]
```