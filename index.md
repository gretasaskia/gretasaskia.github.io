---
layout: page
title: Wikiwomen
subtitle: An analysis on gender bias
cover-img: /assets/img/landscape_wiki2.png
---

Throughout history, women have been marginalized in many communities and in the last few years, gender bias against women has become even more visible in internet applications and online search. In Wikipedia, women are more linked to men than vice versa[^1] and Google Translate has a tendency towards male defaults[^2]. **Gender bias that appears online is in fact a reflection of the gender bias in our society.** Therefore, we would like to investigate whether there exists a gender bias against women when people play the game of  Wikispeedia. In Wikispeedia, people are asked to navigate from a given source article to a certain target article on Wikipedia. The Wikispeedia dataset[^3] provides human navigation paths on a subset of Wikipedia that can be used to investigate whether there exists gender bias against women when users navigate from a given source article to a target article, where the target article relates to women.
{: .text-justify}

## The men and the women of Wikispeedia

Wikipedia’s vast collection of articles has been a source of much amusement for many of its users. Wikipedia has grown so big that users have found a way to entertain themselves within the site itself with navigating from one article to another in the shortest possible time. Evidently, a big portion of the articles concern people. You can find articles about all kinds of people, big and small, famous and not so famous. But unfortunately, as in the real world, there is a bias against women. In the Wikispeedia dataset that we investigated, the first thing that struck us was that only a small portion of the articles about people are in fact about women. 
{: .text-justify}

{% include plot1.html %}

The second thing that struck us was the unequal amount of articles about women and men within each of the dataset's categories. The only category where the number of articles about women came close to being the same as the number of articles about men was in the category for *Actors, models and celebrities*. This unequal distribution is very sad to see, because women play just as big of a role in society as men: There are and have been female politicians, scientists, leaders, artists, engineers and so on (and although there have not been any female presidents of the United States, we hope that changes soon 🙂).
{: .text-justify}

{% include plot2.html %} 

In each category, there are A LOT of articles about men. Sadly, it doesn’t come as a surprise to see the striking comparison of the number of articles about men and the number of articles about women. Men have dominated all aspect of the society for such a long time. In the following years, this will hopefully change for the better.
{: .text-justify}

{% include plot3.html %} 

Since there exist more articles about men than women in the dataset, it is therefore clear that more paths lead to target articles about men! But are people even able to find the target article and finish the game? As it turns out, the fraction of paths that lead to women and are unfinished is higher than the fraction of paths that lead to women and are finished. And as for the men, the reverse is true.

{% include piechart2.html %}

Then, we can see that a higher fraction of men articles are found (i.e., finished) compared to those of women.

{% include piechart.html %} 

## But do the paths that lead to target articles about women differ in any way from the paths that lead to target articles about men? 
The paths that people navigate through when playing Wikispeedia differ in many ways, such as the length of the path itself and how long it takes the player to finish the game, if he indeed finishes. Some players find their paths difficult and need to take a step back with a backclick but some paths are easier. By comparing these factors that describe a path, it is possible to find out whether there exists a gender bias against women when people play the game of Wikispeedia. 
{: .text-justify}

In relation to these factors that describe a path, we have defined a few metrics that we will use to compare the two groups of paths with women and men target articles. They are the following: 
{: .text-justify}
- Success rate: The fraction of successful paths to a certain target article.
- Playtime: The duration of a game of a finished path.
- Path deviation: The difference between the length of the path that it took a player to go from a source article to a target article and the shortest possible length of the same path.
- Number of back clicks: The number of back clicks a player takes in a path.
- Difficulty rating: The difficulty rate a player rates a successful finished path.
- In-degree: The number of articles that lead to a target article.
{: .text-justify}

### Out of all these six characteristics of a path, four of them turn out to indicate that the two groups of men and women paths are significantly different!
In the following radar chart, we can see the geometric mean values of each of these four metrics. Every one of these values indicate that there exists a gender bias against women.
{: .text-justify}
- The success rate of finishing a path with a target article about a man is higher than the success rate of women. 
- People tend to be longer to navigate a path towards a women article than towards a man article.
- The paths leading to an article about a woman are longer than those leading to men.
- People find paths leading to articles about women more difficult than those leading to men.
{: .text-justify}

{% include radarplot_realvalues.html %} 

### But wait, can we really say that there exists a gender bias against women based on the previous results?
No, these previous results compare paths leading to a man article to a path leading to a woman article **without any restrictions**. In order for us to tell with any certainty if there is a difference between the two groups, we need to match a man path with a woman path where both paths begin with the same source article and do the comparison on that. 
{: .text-justify}

RESULTS 

### Are there any more features we have to take into account for our comparison?
Yes, in fact there are. The paths also have to be restricted on the shortest path length, that is, we can only compare a woman path with a men path that begin with the same source article and have the same shortest possible length of a path.
{: .text-justify}

RESULTS 

### Hang on a second, we have not yet looked at the categories of our target articles!
Comparing a path leading to Albert Einstein and a path leading to Celine Dion seems counterintuitive since they are not a part of the same category. Einstein is a scientist and Celine Dion is a singer.

...

After matching finished paths on source, shortest path and category, we are left with these 12 paths:

| Source      | Target      | Gender      | Path length | Path deviation | Playtime |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| Ganesha     | Elizabeth_II_of_the_United_Kingdom | female | 7 | 4 | 71 |
| Ganesha    | Mao_Zedong  | male | 4 | 1 | 133 |
| Margaret_Sanger | William_and_Mary | female | 9 | 6 | 1474 |
| Margaret_Sanger | James_I_of_England | male | 6 | 3 | 96 |
| Nintendo | Condoleezza_Rice | female | 4 | 1 | 73 |
| Nintendo | Osama_bin_Laden | male | 4 | 1 | 116 |
| Philippines | Margaret_Thatcher | female | 4 | 1 | 60|
| Philippines | Osama_bin_Laden | male | 4 | 1 | 48 |
| Space_Race | Elizabeth_I_of_England | female | 7 | 4 | 1860 |
| Space_Race | Richard_III_of_England | male | 9 | 6 | 392 |
| Spacecraft_propulsion | Helen | female | 8 | 4 | 210 |
| Spacecraft_propulsion | William_Ewart_Gladstone | male | 6 | 2 | 100 |
    



## Conclusions

## References

[^1]: Wagner, C., Garcia, D., Jadidi, M., & Strohmaier, M. (2021). It’s a Man’s Wikipedia? Assessing Gender Inequality in an Online Encyclopedia. Proceedings of the International AAAI Conference on Web and Social Media, 9(1), 454-463. https://doi.org/10.1609/icwsm.v9i1.14628.
[^2]: Prates, M.O.R., Avelar, P.H. & Lamb, L.C. (2020) Assessing gender bias in machine translation: a case study with Google Translate. Neural Comput & Applic 32, 6363–6381. https://doi.org/10.1007/s00521-019-04144-6.
[^3]: https://snap.stanford.edu/data/wikispeedia.html.

