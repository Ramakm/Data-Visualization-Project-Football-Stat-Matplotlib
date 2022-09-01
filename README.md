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

Updated the Average Attendance in each club stadium statistics:

Extracted the table Data using the soup object again.

[{'Barcelona': '53,982'},
 {'Atlético Madrid': '46,728'},
 {'Real Betis': '41,715'},
 {'Real Madrid': '41,228'},
 {'Athletic Bilbao': '32,946'},
 {'Sevilla': '29,756'},
 {'Valencia': '27,349'},
 {'Real Sociedad': '26,827'},
 {'Espanyol': '16,778'},
 {'Osasuna': '16,753'},
 {'Elche': '15,847'},
 {'Levante': '14,961'},
 {'Villarreal': '14,293'},
 {'Cádiz': '14,055'},
 {'Granada': '13,381'},
 {'Mallorca': '12,434'},
 {'Alavés': '10,799'},
 {'Celta Vigo': '10,014'},
 {'Getafe': '8,702'},
 {'Rayo Vallecano': '8,035'},
 {'League total': '22,829'}]
 
 This time i have used a plotting object called pie.
 I have show the percentage of total 100% and which club has the maximum no of attendance out of them all. If Barcelona is showing 13% means
 They have the highest among the all club.  But its not showing the total from their club avg.
 Be clear on that.
 
 ```
plt.title("Average Attendence in Laliga Santander 2021-2022", color = "black", fontsize = "15", fontweight = "bold")
plt.pie(sizes, labels=labels, autopct = "%1.1f%%")
plt.show()
 
 ```
