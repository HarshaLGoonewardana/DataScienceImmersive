# Data Visualization with Matplotlib

## Table of Contents
- [High Level Overview of Matplotlib](00-Matplotlib_at_a_High_Level.ipynb)
- [Visualization with Matplotlib and Pandas](01-Viz_in_Matplotlib_and_Pandas)
- [How to make XKCD-style Plots](xkcd_plots.ipynb)

## Creating a Custom ‘Presentation’ Style Sheet in Matplotlib 

In order to create a custom style with large fonts and the like:

```
import matplotlib
matplotlib.get_configdir()
```
Now, go to that directory, and create a new subdirectory (if it doesn’t already exist) called `stylelib`. Inside that directory, create a new file (using a text editor of your choice) called `presentation.mplstyle`. Inside that file, save these configuration settings:
```
axes.titlesize : 24
axes.labelsize : 20
lines.linewidth : 3
lines.markersize : 10
xtick.labelsize : 16
ytick.labelsize : 16
```

You may want to restart your kernel. Now, run a simple plotting command:

```
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline


df = pd.DataFrame({'a':[1,2,3],'b':[3,4,5]})

df.plot();
```

You will see a basic plot. To use a matplotlib style, run this command:

```
plt.style.use('fivethirtyeight')
df.plot();
```

and you will see your plot is in a new style!

Now, we can layer on the `presentation` style we just created, like so:
```
plt.style.use(['fivethirtyeight','presentation']) 
df.plot();
```

Your plot should still be in the FiveThirtyEightStyle, but now it also has presentation-ready title and label sizes! Enjoy.

Source: https://matplotlib.org/users/style_sheets.html
