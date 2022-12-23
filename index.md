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

The second thing that struck us was the unequal amount of articles about women and men within each of the dataset's categories. The only category where the number of articles about women came close to being the same as the number of articles about men was in the category for *Actors, models and celebrities*. This unequal distribution is very sad to see, because women play just as big of a role in society as men: There are and have been female politicians, scientists, leaders, artists, engineers and so on (and although there have not been any female presidents of the United States, we hope that changes soon).
{: .text-justify}

{% include plot2.html %} 

In each category, there are A LOT of articles about men. Sadly, it doesn’t come as a surprise to see the striking comparison of the number of articles about men and the number of articles about women. Men have dominated all aspect of the society for such a long time. In the following years, this will hopefully change for the better.
{: .text-justify}

{% include plot3.html %} 

Additionally, a higher fraction of the paths that lead to target articles about men are finished than those of the paths that lead to target articles about women! And for the unfinished paths, the women have the "victory" as the fraction of unfinished paths that lead to women articles is higher than those for men articles.
{: .text-justify}

{% include piechart.html %} 

## But do the paths that lead to target articles about women differ in any way from the paths that lead to target articles about men? 
The paths that people navigate through when playing Wikispeedia differ in many ways, such as the length of the path itself and how long it takes the player to finish the game, if he indeed finishes. Some players find their paths difficult and need to take a step back to the previous article with a backclick but some paths are easier. By comparing these characteristics that describe a path, it is possible to find out whether there exists a gender bias against women when people play the game of Wikispeedia. 
{: .text-justify}

These characteristics of navigation paths can be described in the following way: 

- *Success rate*: The fraction of successful paths to a certain target article.
- *In-degree*: The in-degree of a target article describes the number of other articles that have a link to it. If it is high for a certain article, then it is easier to access it compared to an article that has a lower in-degree.
- *Playtime*: The duration of a game of a finished path.
- *Path deviation*: The difference between the length of the path that it took a player to go from a source article to a target article and the length of the shortest possible path between the source and target article.
- *Number of back clicks*: The number of back clicks a player takes in a path.
- *Difficulty rating*: The difficulty rate a player rates a successful finished path, on the scale 1 (easy) to 5 (brutal).
{: .text-justify}

### Out of all these six characteristics of a path, five of them turn out to indicate that the two groups of men and women paths are indeed different!
The following radar chart shows the geometric mean values of each of these five metrics. Every one of these values indicate that there exists a gender bias against women.
{: .text-justify}

- The success rate of finishing a path with a target article about a man is higher than the success rate of women. 
- The in-degree for target articles about men is higher than the in-degree for target articles about women, thus there are more possibilites to reach the men than the women.
- People tend to take longer to navigate a path towards a woman article than towards a man article.
- The paths leading to an article about a woman are longer than those leading to men.
- People find paths leading to articles about women more difficult than those leading to men.
{: .text-justify}

{% include radarplot_naive.html %} 

### But wait, can we really say that there exists a gender bias against women based on the previous results?
 
<p align="center">
<img src="assets/img/no.gif" alt="No"/>
</p>

Well no, these previous results compare paths leading to a man article to a path leading to a woman article **without any restrictions**. In order for us to tell with any certainty if there is a difference between the two groups, we need to match a man path with a woman path where both paths begin with the same source article and do the comparison on that. 
{: .text-justify}

Taking this into account, only four out of the six characteristics show that the paths of the two groups are different. These are the success rate, the playtime, the path deviation and the in-degree, i.e., the ones fully colored on the barplot below. The other ones, those colored in a slightly more transparent way, do not indicate a difference between the paths of the groups since their confidence intervals overlap and thus the result can not be considered significant.
{: .text-justify}

{% include src_match.html %} 

### Are there any more features we have to take into account for our comparison?
Yes, in fact there are. The paths also have to be restricted on the shortest path length, that is, we can only compare a woman path with a men path that begin with the same source article and have the same shortest possible length of a path.
{: .text-justify}

Now, only one characteristic indicates a difference between the two groups, namely the success rate of path. 
{: .text-justify}

{% include shpath_match.html %} 

### Hang on a second, we have not yet looked at the categories of our target articles!
Comparing a path leading to Albert Einstein and a path leading to Celine Dion seems strange since they are not a part of the same category. Einstein is a scientist and Celine Dion is a singer! However, the possible matches we are able to do taking this into account is very limited with our amount of data. But, just because they are in different categories doesn't mean they are not equally popular or known. Thus, we can shift our attention to the in-degree of an article. Even though Einstein and Celine Dion have a completely different line of work, they might be equally popular (since they are both quite amazing).
{: .text-justify}

### In-degrees to the rescue!
Matching pairs on the same source, shortest path lenght and a similar in-degree provides us with enough data to see if there is a difference between the paths towards the two groups of articles. As before, we only see a difference in the success rate of the two groups, and a difference that points to a gender bias against women as well.
{: .text-justify}

{% include degree_match.html %} 

## Conclusion
Narrowing down, we still see a difference in our characteristics that suggests that there exists a gender bias against women in Wikispeedia. This gender bias has indicated itself in not only the way Wikispeedia is constructed as well as in the way its players play it. Wikispeedia's dataset is constructed with a much smaller amount of data that refers to articles about women and the way that the articles are connected discriminate against women. Overall, there must be some confounding factor that leads to a difference in the success rate, even though this time we did not find it. When provided with a larger amount of data, our results will be even more concrete. 
{: .text-justify}

## References

[^1]: Wagner, C., Garcia, D., Jadidi, M., & Strohmaier, M. (2021). It’s a Man’s Wikipedia? Assessing Gender Inequality in an Online Encyclopedia. Proceedings of the International AAAI Conference on Web and Social Media, 9(1), 454-463. https://doi.org/10.1609/icwsm.v9i1.14628.
[^2]: Prates, M.O.R., Avelar, P.H. & Lamb, L.C. (2020) Assessing gender bias in machine translation: a case study with Google Translate. Neural Comput & Applic 32, 6363–6381. https://doi.org/10.1007/s00521-019-04144-6.
[^3]: https://snap.stanford.edu/data/wikispeedia.html.

