
# OutLine

- [OutLine](#outline)
- [Practice for Python language with difficulty 8 kyu](#practice-for-python-language-with-difficulty-8-kyu)
- [1. Quadrants](#1-quadrants)
- [2. Even or Odd](#2-even-or-odd)

# Practice for Python language with difficulty 8 kyu
All the questions are from [Codewars](https://www.codewars.com).

# 1. Quadrants
Task
Given a point in a Euclidean plane (x and y), return the quadrant the point exists in: 1, 2, 3 or 4 (integer). x and y are non-zero integers, therefore the given point never lies on the axes.

**Examples**
```
(1, 2)     => 1
(3, 5)     => 1
(-10, 100) => 2
(-1, -9)   => 3
(19, -56)  => 4
```

**Reference**
![image](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1a/Cartesian_coordinates_2D.svg/300px-Cartesian_coordinates_2D.svg.png)
*Quadrants*

There are four quadrants:

First quadrant, the quadrant in the top-right, contains all points with positive X and Y
Second quadrant, the quadrant in the top-left, contains all points with negative X, but positive Y
Third quadrant, the quadrant in the bottom-left, contains all points with negative X and Y
Fourth quadrant, the quadrant in the bottom-right, contains all points with positive X, but negative Y

More on quadrants: [Quadrant (plane geometry) - Wikipedia](https://en.wikipedia.org/wiki/Quadrant_(plane_geometry))

**Task Series**
Quadrants (this kata)
Quadrants 2: Segments

**Solution:**
```python
def quadrant(x, y):
    if x>0 and y>0:
        return 1
    elif x<0 and y>0:
        return 2
    elif x<0 and y<0:
        return 3
    elif x>0 and y<0:
        return 4
```

**The better solutions:**
```python
# by @mkm7_, @A_Richardz, ...
def quadrant(x, y):
    if x >= 0:
        if y >= 0:
            return 1
        else: return 4
    elif x<0:
        if y < 0:
            return 3
        else: return 2
```

```python
# by @Mercy Madmask, @farruxnabilloyev, @Abdulla2005
def quadrant(x, y):
    return 1 + 2*(y<0) + (x*y<0)
```

# 2. Even or Odd
Create a function that takes an integer as an argument and returns `"Even"` for even numbers or `"Odd"` for odd numbers.

**Solution:**
```python
def even_or_odd(number):
    if (number % 2)==0:
        return "Even"
    else: 
        return "Odd"
```

**The better solutions:**
```python
# by @ksolademi, @laoris, ...
def even_or_odd(number):
	return 'Odd' if number % 2 else 'Even'
```

```python
# by @spirAde, @kinetic, ...
def even_or_odd(number):
  return 'Even' if number % 2 == 0 else 'Odd'
```