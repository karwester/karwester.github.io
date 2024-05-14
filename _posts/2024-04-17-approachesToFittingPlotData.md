---
layout: post
title: Yet another (the best?) way of fitting death toll data
date: 2024-04-17 02:20:00-0400

inline: false
---
I've been trying to find a good way of displaying overlapping and scattered data points in a plot and came up with a couple of approaches. One option is to use log scale on whichever axis has outliers. The other one is to use the brokenaxes Python package. I don't love either of these approaches for displaying war data because in my view they obfuscate the magnitude to the most deadly wars but they are a compromise I will live with.

My (probably) final attempt at the death toll graph does 3 things:
- adds information about war duration by using bars rather than bubbles
- gives a zoomed in/zoomed out view without overrelying on brokenaxes
- highlights the number of big Chinese wars in history (this was not something discussed in great deatail during my Europe-focused history lessons at school.)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/deathToll2Plots.png" title="Wars by Death Toll (over 1.5M) Chart" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    Best attempt so far.
</div>

With any data that is so subjective in nature there will be questions about how accurate it is, especially for historical wars where the records may be less credible and available. My graph shows the absolute death toll numbers and it is interesting to compare it to death toll in relation to respective population. The standard in social sciences is to report cases and deaths per 100,000 to reflect the impact on population. It's worth noting, this measure compares war death toll in a specific region to the global population, not population in that region.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/ourworldindata_wars-long-run-military-civilian-fatalities-from-brecke1.0.png" title="Wars by Death Toll CHart from Max Roser" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    The source of data used for this graph is likely more accurate than Wikipedia.
</div>

 All code can be found in this [Jupyter notebook](https://github.com/karwester/wikiWar/blob/main/longestAndDeadliestWarsContinued.ipynb). 


---
What's next? I've been curious about how reporting arithmetic vs. geometric mean of ranges affects the perception of death toll.



