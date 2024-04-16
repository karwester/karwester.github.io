---
layout: post
title: War Death Toll
date: 2024-04-16 01:11:00-0400

inline: false
---
I've been looking into ways to visualise war information and into previous examples of that. Most of the graphs I found cover only a short period of time, 200-300 years and I wanted to have a  broad view of all the recorded wars. The key statistic collected about wars is death toll, it can be divided into combatant and civil deaths, but only for the more recent wars where there was an effort to accurately collect this data.

My starting point was Wikipedia graph showing death toll.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="https://upload.wikimedia.org/wikipedia/commons/3/36/Wars_by_Death_Toll_Chart.jpg" title="Wars by Death Toll Chart" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    There are some issues with this graph: the distances between values on the y axis seem a bit arbitrary.
</div>

My data came from [Wikipedia](https://en.wikipedia.org/wiki/List_of_wars_by_death_toll). The page is frequently updated so some numbers may no longer match. The challenge was to fit all the wars with over 1M deaths the scale in a readable way. The 2WW had the highest number of deaths (~80M) followed by Taiping Rebellion (~70M). And a digression here: Casualties data usually comes from various historical sources and these do not necessairly agree with each other. The high range of Taiping rebellion is 70M in the Wikipedia table I used for analysis, however, in the Wikipedia page on Taiping Rebellion the figure is only 20M (the lower range in Wikipedia table). This may be the largest difference between the low and high values for death toll. I don't have any scientific articles to quote but google research suggests Chinese scholars tend to agree with the higher numbers. The numbers are estimated based on populations size before and after the rebellion (which lasted 13 years) and many deaths might have been dure to famine and plague rather than combat.

The Wikipedia graph above does a good job in showing wars and their names clearly but the distances between numbers are a bit off (the distance between 10M and 20M is too wide). Here is my attempt to address this problem while showing all wars with over 1M casualties.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/deathTollHighRangeAD.png" title="Wikidata war stats" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    Wikidata war data is very patchy, not really suitable for any in-depth analysis.
</div>

 All code can be found in this [Jupyter notebook](https://github.com/karwester/wikiWar/blob/main/warDeathToll.ipynb). 


---
What's next? I think I should look into the low range of death toll and see how it changes the view of the deadliest wars.



