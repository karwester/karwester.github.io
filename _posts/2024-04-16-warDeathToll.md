---
layout: post
title: War Death Toll
date: 2024-04-16 01:11:00-0400

inline: false
---
I've been looking into ways to visualise war information. Most of the graphs I found cover only a short period of time, 200-300 years, and I wanted to have a broad view of all the recorded wars. The key statistic collected about wars is death toll. For more recent wars, it is usually divided into combatant and civil deaths, but for more distant wars there is no such data.

My starting point was Wikipedia graph showing death toll.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="https://upload.wikimedia.org/wikipedia/commons/3/36/Wars_by_Death_Toll_Chart.jpg" title="Wars by Death Toll Chart" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    There are some issues with this graph: the distances between values on the y axis seem a bit off.
</div>

My data came from [Wikipedia](https://en.wikipedia.org/wiki/List_of_wars_by_death_toll). The page is frequently updated so some numbers may no longer match. The challenge was to fit all the wars with over 1M deaths in one graph in a readable way. The 2WW had the highest number of deaths (~80M) followed by Taiping Rebellion (~70M). And a digression here: Casualties data usually comes from various historical sources and these do not necessairly agree with each other. The high range of Taiping rebellion is 70M in the Wikipedia table I used for analysis, however, in the Wikipedia page on Taiping Rebellion the figure is only 20M (the lower range in Wikipedia table). This may be the largest difference between the low and high values for death toll. I don't have any scientific articles to quote but google research suggests Chinese scholars tend to agree with the higher numbers. The numbers are estimated based on populations size before and after the rebellion (which lasted 13 years) and many deaths might have been dure to famine and plague rather than direct combat.

The Wikipedia graph above does a good job in showing wars and their names but:

1. The distances between numbers look a bit off (the distance between 10M and 20M seems too wide. I eventually figured it's because y axis is a on a log scale but the bottom 0-3M part is cut off).
2. With something as impactful as war one might want to avoid log scale to show the true impact of war. This is a hard one. On the one hand, you want to be accurate and express the true intensity of a war, on the other, you want to make it readable and may have limited space to fit the graph. To truly illustrate the impact of WW2 the best approach might actually be to stretch y axis so you need to scroll. The physical act of having to scroll would be akin to what xx did here to show impact of climate change.
3. The cut off point will always be arbitrary, in this case it's 3M deaths, and some of the big recent wars like the Vietnam War are not shown. I will see if I can include a few more wars while keeping it readable.
4. Small issue, but WW1 is displayed twice.

So, this was my first attempt to fit all over 1M deaths wars in one graph (using the higher value of the death toll range). This is not good at all because the y scale doesn't scale in any way, the data is ordered but they don't follow any meaningful patter that would correspond to increase in numbers. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/deathTollHighRangeAD.png" title="Wikidata war stats" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    Managed to fit all over 1M deaths wars but the y scale is meaningless.
</div>

 Here is my second attempt using the brokenaxes package and geometric mean of the death toll, like in the original graph. Again, I'm not entirely happy to what breaking the axis or using a log scale does to the perception of war size but I don't see a better alternative to fitting all the wars in one graph.
 
 <div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/over1_5MdeathToll.png" title="Wikidata war stats" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    Not entirely happy with chopping the scale but this is the best version so far.
</div>
 
 Some questions related to this graph:
 1. How different would it look if I used arithmentic mean instead of geometric?
 2. Should Reconquista be included as a war?
 3. WW2 death toll seems to include Second Sino-Japanese death toll...
 4. Bubble size is repating information from y axis. Can I come up with a better graph, maybe death toll, start date and duration?
 
 All code can be found in this [Jupyter notebook](https://github.com/karwester/wikiWar/blob/main/warDeathToll.ipynb). 


---
What's next? I think I should look into the low range of death toll and see how it changes the view of the deadliest wars.



