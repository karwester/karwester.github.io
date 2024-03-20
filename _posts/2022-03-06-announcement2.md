---
layout: post
title: Wikidata and war history
date: 2024-03-19 16:11:00-0400
inline: false
---
The topic of war has been on my mind lately, so I figured it was time to brush up on my SPARQL and check out how complete Wikidata war data is for analysis. History has always been my Achilles heel and I have no memory for dates, but diving into global war stats seemed like a worthwhile learning experience.

First, I created a query to get all instances of war (I tried getting both wars and the associated info in one query but it timed out). I then wrote a script to get properties for each war instance, I still got some time-outs and had to rerun it to get all the data. Finally, I loaded the data into a [notebook](https://github.com/karwester/wikiWar).  

Unfortunately, the data about wars in Wikidata is very incomplete, too incomplete for any decent analysis. The war concept is very subjective and includes all sorts of conflicts, the definition of war is subjective. If anything, my analysis shows how incomplete the Wikidata is. There are many missing wars, even wars that you can find on Wikipedia, which are not on Wikidata. Not so surprising, given it's run by volunteers who probably need to manually add this information.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
      <a>
        {% include figure.html path="assets/img/warsFromWikiData.png" title="Wikidata war stats" class="img-fluid rounded z-depth-1" %}
      </a>
    </div>
</div>
<div class="caption">
    Wikidata war data is very patchy, not really suitable for any in-depth analysis.
</div>

---
While Wikidata is a cool place to get data on anything and I'm planning to use it again, it didn't work so well in this case. Since then I've come across a [great analysis](https://ourworldindata.org/war-and-peace) of global war data by OurWorldInData. The authors explain how complex getting data on war is and do a great job of presenting what we know so far. Most of their analysis relies on data from 1800 and later, so it would be interesting to investigate wars in older times.


<!-- ***

A little bit about me. I love watching TV; I like Football and Basketball; I love the UFC MMA. Hopefully, that doesn't scare you. :smirk:

#### A Small Bucket List (Will grow in the future)
<ul>
    <li>Attend a UFC match.</li>
    <li>Visit the 7 modern and ancient wonders of the world.</li>
</ul>

Also, has anyone actually worn a hoodie and feel warm? Not me.

***

Did I mention I love quotes related to life? Here's one that sticks with me.

> "If you love it, you’ll teach yourself. If you don’t love it, others will teach you"
>
> —Yukitaka Yamaguchi

Thanks for reading!

Best,

Spencer -->
