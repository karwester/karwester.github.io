---
layout: post
title: Approaches To Fitting Plot Data
date: 2024-04-17 02:20:00-0400

inline: false
---
I've been trying to find a good way of displaying overlapping and scattered data points in a plot and came up with 2, maybe 3 approaches. One of them was used in my previous post to show war death toll.

Another one is using Python brokenaxes package. It deals well with white space on the graph but not so well with overlapping data points. My approach was to stretch the graph vertically and adding broken axes. Still, when the data points became too close to each other broken axes did not do so well. My best graph was for wars with over 5M deaths.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/brokenAxesDeathToll.png" title="Wars by Death Toll Chart USing Brokenaxes Package" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    I tried running this for wars with deaths over 1M instead of 5M and the graph became too busy.
</div>

The third approach would be to split the graph into 2 and display the busy portion as a separate graph.

 All code can be found in this [Jupyter notebook](https://github.com/karwester/wikiWar/blob/main/approachesToFittingOutliersOnPlots.ipynb). 


---
What's next? I'm curious about BC wars and want to know more about Taiping rebellion. In general, the graphs give you the idea of how many big wars happened in Asia. This was not something discussed in great deatail during my Europe-focused history lessons.



