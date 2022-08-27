<h1> Matplotlib-Squarify </h1>
Webscrapping and plotting using matplotlib-squarify:

Data Visualization is a powerful technique to analyze a large dataset through graphical representation. Python provides various modules that support the graphical representation of data. The widely used modules are Matplotlib, Seaborn, and Plotly.

A treemap in Python is a visualization of data that splits a rectangle into sub-parts.

Pure Python Implementation of the squarify treemap method.

First install Squarify else it will throw an error Module not found.

` pip install squarify `

`pip install requests`

<h1>Figure Dimensions</h1>


One thing I struggled with  matplotlib is that I never knew how to control the actual dimensions of the plot I was creating.

Knowing the actual size of your plot (in pixels), is actually pretty important. For example, knowing the "pixel size" of your plot is essential to secure that the text in your visual doesn't look too small, or too big; or that you don't create unnecessary huge figures.

So here's how this works:

* When you create a figure the figsize parameter specifies the dimensions of your figure in inches.
* The dpi parameter denotes the dots per inch of your figure, where a higher dpi results in a higher resolution.

As a result, the dimensions of the figure (in pixels) will be the dpi times the width and height of the plot. For example, the following code creates a 1500 x 1500 sized picture since we assign a dpi of 400 and a figsize = (15, 7).


```

norm = matplotlib.colors.Normalize(vmin = min(scored), vmax = max(scored))
colors = [matplotlib.cm.Greens(norm(value)) for value in scored]

fig, ax = plt.subplots(figsize = (15,7), dpi = 400)

squarify.plot(sizes = scored, label = names, color = colors)

```
