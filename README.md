# About

There have been recreations in Python, R, Highcharts of plots in Cole Nussbaumer Knaflic ‘s book [Storytelling With Data](https://www.storytellingwithdata.com/book/downloads). Here I try to reproduce them using Tableau and giving my understanding of those plots.

# Principles

I will not reproduce those charts 100% the same as the original one, eg. tracking exactly the same color, layout, fonts, etc. Instead, I will try to capture the author’s thinking and adjust them based on my ideas and gives some tricky usage of Tableau.

# Figures & Analysis

## Figure 3.13

<p align="center">
<img src="./images/3.13_ori.png" width="65%" >
</p>

### Defects

1. Bad alignment: centering is messy for words
2. The selected 3 are not emphasized, unimportant words in the title, header, and annotation arrow are bold instead.
3. The scales are inclined, which increases the difficulty of reading.

### Improvements

<p align="center">
<img src="./images/3.13_swd.png" width="65%" >
</p>
<p align="center">
<img src="./images/3.13_my.png" width="65%" >
</p>

### My modifications

1. Change the language in the description and make the bold words less.
2. Change the color of the selected bars so that people can first notice these instead of texts that are also black and bold.

### Tricks

1. To adjust the space between the title and the description in Tableau, we can insert one row in the between, select its size to adjust the space, and paint it white.
2. The texts in the right column are added in the dashboard.
3. Separating “Survey shows that” and the following words makes it easier to read.
4. If there are not any explanations in the right columns, we can make the headers of the chosen 3 blue to emphasize them. However, it is not easy to do so in Tableau.

## Figure 3.15

<p align="center">
<img src="./images/3.15_ori.png" width="65%" >
</p>
#### Defects

1. Various colors and shapes are confusing.
2. The index of our services is not emphasized. 
3. Negative data are not necessary, which can be shifted to positive.

### Improvements

<p align="center">
<img src="./images/3.15_swd.png" width="65%" >
</p>
<p align="center">
<img src="./images/3.15_my.png" width="65%" >
</p>

#### My modifications
1. I don’t know how to adjust the distance between bars for different headers, so I just use the divided line.
2. Strangely, the legend is under the title. I put the legend aside.

#### Tricks

1. In Tableau, the rankings are labeled to every bar. To only label our service, we need to first choose “Never Show” in right-click -> Mark Label, then choose “Always Show” one by one.


