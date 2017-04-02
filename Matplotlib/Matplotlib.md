# Matplotlib

This serves as a cheat sheet for Matplotlib, a 2d plotting library for Python.

Not a total beginner? Jump straight down to the [examples](#examples)

## Index
[Prepare Data](#prepare)
[Create Plots](#plots)
[Examples](#examples)

## Prepare Data <a name="prepare"></a>

NumPy is probably your best friend for that. Check out my CheatSheet [here](https://github.com/juliangaal/python-cheat-sheet/blob/master/NumPy/NumPy.md)

## Creating Plots <a name="plots"></a>
| Operator    | Description     | Documentation |
| :------------- | :------------- | :----------- |
| *Figure*       |        |    |
| fig = plt.figures()      | a container that contains all plot elements | [link](http://matplotlib.org/api/figure_api.html) |
| *Axes*       |   |   |
| fig.add_axes()       |Initializes fig for later ax addition| |
| a = fig.add_subplot(222)|A subplot is an axes on a grid system <br/> row-col-num, see [examples](#examples) | [link](http://matplotlib.org/api/figure_api.html#matplotlib.figure.Figure)|
| fig, b = plt.subrows(nrows=3, nclos=2)|Adds subplot| [link](http://matplotlib.org/api/pyplot_api.html#matplotlib.pyplot.subplot)|

## Examples

### Basics
```python
import matplotlib.pyplot as plt

x = [1, 2.1, 0.4, 8.9, 7.1, 0.1, 3, 5.1, 6.1, 3.4, 2.9, 9]
y = [1, 3.4, 0.7, 1.3, 9, 0.4, 4, 1.9, 9, 0.3, 4.0, 2.9]
plt.scatter(x,y, color='red')

w = [0.1, 0.2, 0.4, 0.8, 1.6, 2.1, 2.5, 4, 6.5, 8, 10]
z = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
plt.plot(z, w, color='lightblue', linewidth=2)

c = [0,1,2,3,4, 5, 6, 7, 8, 9, 10]
plt.plot(c)

plt.ylabel('some numbers')
plt.xlabel('some more numbers')
plt.show()
```
![alt-text](/img/plot.png)

### Subplotting Examples
```python
import matplotlib.pyplot as plt

x = [0.5, 0.6, 0.8, 1.2, 2.0, 3.0]
y = [10, 15, 20, 25, 30, 35]
z = [1, 2, 3, 4]
w = [10, 20, 30, 40]

fig = plt.figure()
ax =  fig.add_subplot(111)
ax.plot(x, y, color='lightblue', linewidth=3)
ax.scatter([2,3.4,4, 5.5],
               [5,10,12, 15],
               color='darkgreen',
               marker='^')
ax.set_xlim(0, 6.5)

ax2 =  fig.add_subplot(222)
ax2.plot(z, w, color='lightgreen', linewidth=3)
ax2.scatter([3,5,7],
               [5,15,25],
               color='red',
               marker='*')
ax2.set_xlim(1, 7.5)

plt.savefig('mediumplot.png')
plt.show()
```
![alt-text](/img/mediumplot.png)

### Advanced

Taken from [official docs](http://matplotlib.org/api/pyplot_api.html)
```python
import matplotlib.pyplot as plt
import numpy as np


np.random.seed(0)

x, y = np.random.randn(2, 100)
fig = plt.figure()
ax1 = fig.add_subplot(211)
ax1.xcorr(x, y, usevlines=True, maxlags=50, normed=True, lw=2)
ax1.grid(True)
ax1.axhline(0, color='black', lw=2)

ax2 = fig.add_subplot(212, sharex=ax1)
ax2.acorr(x, usevlines=True, normed=True, maxlags=50, lw=2)
ax2.grid(True)
ax2.axhline(0, color='black', lw=2)

plt.show()
```
![alt-text](/img/advancedplot.png)

| Operator    | Description     | Documentation |
| :------------- | :------------- | :----------- |
| Figure       |        |    |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |
| Item One       | Item Two       | Item Three   |



Classic example: gdp per capita and life expectancy
```python
# gdp_cap on the x-axis, life_exp on the y-axis
plt.plot(gdp_cap, life_exp)

# Display the plot
plt.show()
```
result:

### Customization
label
xticks
title

.text
.grid (True/False)

*common arguments for matplotlib diagrams*
size
color
alpha (opacity)
