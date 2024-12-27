---
layout: post
title: Arithmetic or geometric? Which mean is best for estimating death toll ranges?
date: 2024-05-23 02:20:00-0400

inline: false
---
When I posted one of the previous versions of the death toll graphs on Reddit, a few people commented that I should have used arithmetic instead of geometric mean to calculate mean death toll from a range. The original plot I was trying to improve on used a geometric mean and, after some research, I found that geometric mean is often preferred when there are interdependencies between data points, for example when displaying population growth or interest rates. I still wasn't entirely sure though which one of the two is best for giving a reasonable indication of a death toll range.

I came across [this] (https://www.reddit.com/r/AskHistorians/comments/bblmka/why_is_geometric_mean_used_to_estimate_war_death/) explanation which makes a lot of sense to me. The key points are:
- Death toll ranges are not independent data points drawn from a sample
- We don't want the average, we want a value indicative of a range
- Death toll could be viewed as a multiplication of factors (population size, duration, etc). If we produce artificial low and high confidence ranges and their means, arithmetic means from the two can be massively different. Geometric means from low and high confidence ranges will be similar. This assumes we have equally good reasons to believe the low and high value in a range.

So, these arguments are convincing and annoyingly I need to redo my most recent chart where I used the arithmetic mean. Still, I wanted to see what difference it would make to use arithmetic vs. geometric means for wars with the largest ranges.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/arithmGeom.png" title="Wars with top range discrepancies" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    In general GM is always smaller than AM.
</div>

Looking at the graph I was puzzled by the gap in death toll ranges for wars as recent as WW1. Is this just a data problem or do we actually have so little understanding about these numbers?

Here is a short summary of what I found for the 5 wars annotated in the plot:

1. Taiping rebellion (1851-1864), 20-80M deaths, named the worst war of the 19th-c.
Most of the sources available online quote 20M or at most 30M figures but Chinese historians tend to give higher numbers relying on census count and projections of population growth from that time. Based on the [resources] (https://www.reddit.com/r/WarCollege/comments/kfbiv6/why_was_the_taiping_rebellion_so_deadly_both_in/)  I’ve read the higher numbers (50M and over) are more accurate. 
2. An Lushan Rebellion (755-763), 13-36M, An Lushan purportedly killed two thirds of China's population or sixth of the world's population.

The higher value of the range was popularised by Steven PInker who quoted it from what looks like a pop science book by Matt White. I haven’t read the book but Pinker seems to be making an argument about how, in general, the world is becoming more peaceful. Using the higher number for a war that took place a long time ago works well to support his argument. There is a [whole discussion] (https://www.reddit.com/r/AskHistorians/comments/11h1z6v/comment/jasollt/) about it on Reddit which puts the high number of deaths into question.

While reading about it, I got interested in Pinker’s claim about the war situation improving over time and found a cool graph and a [counter-argument] (https://arxiv.org/pdf/1505.04722v1) based on fat tails theory. If you rescale with regards to current population size An Lushan is the most deadly conflict ever.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/an_lushan.png" title="One of the two rescaled graphs by Cirillo and Taleb" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    An Lushan as the most deadly war ever?
</div>

But [another paper] (https://www.fooledbyrandomness.com/violencenobelsymposium.pdf) by the same authors shows quite a different picture. Which one is right? What is going on here? What do the big unannotated bubbles represent?


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/anlushan2.png" title="Second of the 2 rescaled death toll graphs by Cirillo and Taleb" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    I'm at a losss about which one of the two graphs is correct.
</div>


3. WW1 (1914-1918), 17-40M

I think the 40M number is conflating casualties with death toll, 40M is the number of dead and wounded, about 20M is the number of dead. I should probably update this number on the wiki page I took the data from. While reading up about these numbers, I was shocked to learn that the Turkish government still [denies Armenian genocide] (https://www.mfa.gov.tr/controversy-between-turkey-and-armenia-about-the-events-of-1915.en.mfa).


4. Conquests of Timur (1370-1405)

I didn’t find much about the accuracy of different death toll figures for this one but Timur is considered second in history after Gengis Khan in terms of the number of Muslims killed even though he was a Muslim himself and called himself ‘Sword of Islam’ (also famous for decapitating the victims). There is a whole separate discussion about Genghis Khan and the 40M death toll that's attributed to him.

https://www.reddit.com/r/AskHistorians/comments/cdc0wi/how_did_historians_arrive_at_the_figure_of_forty/

add graph of chinese revolts


 All code can be found in this [Jupyter notebook](https://github.com/karwester/wikiWar/blob/main/longestAndDeadliestWarsContinued.ipynb). 


---
What's next? I've been curious about how reporting arithmetic vs. geometric mean of ranges affects the perception of death toll.



