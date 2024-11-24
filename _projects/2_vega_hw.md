---
name: Vega Lite HW6
tools: [Python, HTML, vega-lite]
image: assets/pngs/global_heatmap.png
description: two graphs
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Plot 1

<vegachart schema-url="{{ site.baseurl }}/assets/json/global_heatmap.json" style="width: 100%"></vegachart>

From assignment 5: "This first visualization is a heatmap of all the ufo apperance around the world The color scale is based on the duration is seconds for how long the ufo was spotted. The scale is using log to show the varied differences as it would not be as significant with the polarity of large values and close to 0 values. The heatmap was created to see how the ufo sightings are generally distributed across the world. The color blue wasn't chosen, but the default value was fitting as the longer a ufo was sighting it was lighter, contrasting against the dark background of the app. If I had more time I would've changed the scaling to make it resemble the country borders even more." In this assignment I changed the interactivity to include dropdown. The dropdown is able to select the ufo sightings per state and shows the states coordinates. This allows for an analysis specific to each state and a more specific breakdown.


## Plot 2

<vegachart schema-url="{{ site.baseurl }}/assets/json/ufos_trail.json" style="width: 100%"></vegachart>

From assignment 5: "This second visualization is a trail graph showing how many how long ufos were spotted over time by state. Each color represents a state and it is quite messy because of the amount of states. I choose states because I thought it was interesting how different each state could be. Why would a certain state have more ufo sightings than another? A trial is also interesting to use over a line as a trail can incorporate weights. However, when scaled to log the trails are unlegible so the linear scaling is better to show the disparity.If I had more time I would also figure out how to scale it better." I changed the interactivity to not clutter the shapes. The user will be able to choose the shape of the cylinder and the graph would show the appearances over time in every state per shape.


We can use a vegachart HTML tag like so:

```
myJekyllDir2 = './'
trail.save(myJekyllDir2+"ufos_trail.json")
```

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/Evimess/evimess.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}
</div>

