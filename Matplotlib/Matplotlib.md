# THIS GUIDE IS IN ITS VERY EARLY STAGES AND STILL IN DEVELOPMENT. not much thats helpful here right now

# Matplotlib

## Prepare Data

NumPy is probably your best friend for that. Check out my CheatSheet [here](https://github.com/juliangaal/python-cheat-sheet/blob/master/NumPy/NumPy.md)

## Basic Example

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
![alt-text](/img/basicplot.png)

| Header One     | Header Two     | Header Three |
| :------------- | :------------- | :----------- |
| Item One       | Item Two       | Item Three   |

| Header One     | Header Two     | Header Three |
| :------------- | :------------- | :----------- |
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
