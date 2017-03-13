---
title       : Starbucks worldwide locations
subtitle    : 
author      : Danish Khan
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [quiz,bootstrap]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides

---  &radio2
## Do you know what is the meaning of the Starbucks logo?

1. A mermaid which is half woman and half fish.
2. _A creature from Greek mythology called a siren (half woman, half bird)._

*** =image
<img
src=https://upload.wikimedia.org/wikipedia/en/d/d3/Starbucks_Corporation_Logo_2011.svg>

*** .hint
Where did the modern Olympic games held?

*** .explanation
Let’s go all the way back to 1971, to when Starbucks was first coming to be. In a search for a way to capture the seafaring history of coffee and Seattle’s strong seaport roots, there was a lot of poring over old marine books going on. Suddenly, there she was: a 16th century Norse woodcut of a twin-tailed mermaid, or Siren. There was something about her – a seductive mystery mixed with a nautical theme that was exactly what the founders were looking for. A logo was designed around her, and our long relationship with the Siren began.
Reference: https://www.starbucks.com/blog/so-who-is-the-siren

--- # Slide 3
## Dataset
* Starbucks dataset is downloaded from www.kaggle.com
* Shiny app is developed using Leaflet and Plotly.
* Data cleansing is done and required columns are extracted for plotting and mapping.

```r
dim(read.csv('starbucks_clean_dataset.csv'))
```

```
## [1] 25598    15
```

--- Slide 4
## Map using Leaflet
* Leaflet is used to mapped store locations.
* <b>leafletOutput()</b> is used in the ui.R and <b>renderLeaflet()</b> is used in the server.r.
* Lat and Long columns are used to identify physical location.
* Address is used as labels to popup when a user clicks on the Starbucks icon.

--- Slide 5
## Plot locations using Plotly
* Plotly is used to plot store locations against countries.
* <b>PlotlyOutput()</b> and <b>renderPlotly()</b> are used in the ui.r and server.r respectively.

