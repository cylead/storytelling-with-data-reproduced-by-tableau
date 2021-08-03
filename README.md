## About

There have been recreations in Python, R, Highcharts of plots in Cole Nussbaumer Knaflic's book [Storytelling With Data](https://www.storytellingwithdata.com/book/downloads). Here I try to reproduce them using Tableau and giving my understanding of those plots.

## Principles

I will not reproduce those charts 100% the same as the original ones, eg. tracking exactly the same color, layout, fonts, etc. Instead, I select some before-and-after showcases, follow the author’s thinking process, adjust them based on my ideas, and gives some tricky usage of Tableau.

## Main problems of visualizations

The role of visualization is to simplify the data and convey insights to the audience. So anything below that may hinder achieving this goal will become a defect:
1. Bad alignment.
2. Various colors.
3. Unnecessary gridlines, bolding, font types, font sizes, inclined characters, character shapes, etc.
4. Not enough focus on the data you are interested in.
5. Inappropriate chart type.

## Table of Contents

* [Figure 3.13](#fig3.13)
* [Figure 3.15](#fig3.15)
* [Figure 3.19](#fig3.19)
* [Figure 5.2](#fig5.2)
* [Figure 5.12](#fig5.12)

## Figures & Analysis

### Figure 3.13<a name="fig3.13"></a>

#### Bad plot

<p align="center">
<img src="./images/3.13_ori.png" width="65%" >
</p>

#### Purpose analysis

The task is to select the most important attributes, so we should let the audience first recognize those selected ones and then learn why we select them. 
Idea visual process: look at the plot -> notice the chosen bars -> read the descriptions -> other details


#### Defects

1. Bad alignment: centering is messy for words
2. The selected 3 are not emphasized, unimportant words in the title, header, and annotation arrow are bold instead.
3. The scales are inclined, which increases the difficulty of reading.

#### Improvements

<p align="center">
<img src="./images/3.13_swd.png" width="65%" >
</p>
<p align="center">
<img src="./images/3.13_my.png" width="65%" >
</p>

#### My modifications

* Change the language in the description and make the bold words less.
* Change the color of the selected bars so that people can first notice these instead of texts that are also black and bold.

#### Tricks

* To adjust the space between the title and the description in Tableau, we can insert one row in the between, select its size to adjust the space, and paint it white.
* The texts in the right column are added in the dashboard.
* Separating “Survey shows that” and the following words make it easier to read.
* If there are not any explanations in the right columns, we can make the headers of the chosen 3 blue to emphasize them. However, it is not easy to do so in Tableau. One way is to drop the headers in the sheet and add them in the dashboard.

#### Figure 3.15<a name="fig3.15"></a>

#### Bad plot

<p align="center">
<img src="./images/3.15_ori.png" width="65%" >
</p>

#### Purpose analysis

* The task is to compare our services with others in different aspects, so we should let the audience first recognize the metrics of our service and then compare with others. 
* Idea visual process: look at the plot -> notice the metrics of our service-> judge whether they are good or bad -> other details

#### Defects

1. Various colors and shapes are confusing.
2. The index of our services is not emphasized. 
3. Negative data are not necessary, which can be shifted to positive.
4. The scattering chart type is not the best choice for comparing numeric values in this case.

#### Improvements

<p align="center">
<img src="./images/3.15_swd.png" width="65%" >
</p>
<p align="center">
<img src="./images/3.15_my.png" width="65%" >
</p>

#### My modifications

* It's a bit difficult to adjust the distance between bars for different headers([here is a way to do it](#bar_gap_trick)), so I just use the divided line.
* Strangely, the legend is under the title instead of the bar plot. I put the legend aside.

### Tricks

* In Tableau, the rankings are labeled to every bar. To only label our service, we need to first choose “Never Show” in right-click -> Mark Label, then choose “Always Show” one by one.

### Figure 3.19<a name="fig3.19"></a>

#### Bad plot

<p align="center">
<img src="./images/3.19_ori.png" width="65%" >
</p>

#### Purpose analysis

* The task is to compare the received and processed ticket volumes and shows how it changes over time. 
* Idea visual process: look at the plot -> notice the difference between the curves -> wonder when and why the change happens -> other details


#### Defects
1. Unnecessary gridlines, out border.
2. Extra digits after decimal on the scale.
3. Unnecessary data point marker types.
4. Inclined date headers.
5. It does not show that at a certain time things changed, the processed tickets are much less than they received.

#### Improvements

<p align="center">
<img src="./images/3.19_swd.png" width="65%" >
</p>
<p align="center">
<img src="./images/3.19_my.png" width="65%" >
</p>

#### My modifications
* Add the title which shows that the plot is about ticket volume.

#### Tricks

* To make room for the text in the dashboard, we can use another text object or blank object as the blank. 

### Figure 5.2<a name="fig5.2"></a>

#### Bad plot

<p align="center">
<img src="./images/5.2_ori.png" width="55%" >
</p>

#### Purpose analysis

* The task is to compare marriage rates in different groups of people and explore how the rates change over time.
* Idea visual process: look at the plot -> notice the different groups -> compare the  marriage rates between these groups / learns the trends of those rates -> other details


#### Defects

1. Bar charts are not appropriate for time series.
2. Legend colors’ change with time is confusing.
3. Unnecessary bold “ PEW RESEARCH CENTER”.
4. Should better focus on one education type. 

#### Improvements

<p align="center">
<img src="./images/5.2_swd.png" width="55%" >
</p>
<p align="center">
<img src="./images/5.2_my.png" width="55%" >
</p>

Note: Another improved chart is Figure 5.10. It requires extra information so I don't put it here. 

#### Tricks
* The title is added in the dashboard using the Text Objects, whose place can be easily adjusted.

### Figure 5.12<a name="fig5.12"></a>

#### Bad plot

<p align="center">
<img src="./images/5.12_ori.png" width="55%" >
</p>

#### Purpose analysis

* The task is to show the difference in the customer segment distribution between the US population and our customers. And also focus on the sum of segment 3 to 5.

* Idea visual process: look at the plot -> notice two groups of people-> compare the summed data of segment 3 to 5 -> other details

#### Defects

1. Various colors make people confused.
2. The left headers are not aligned.
3. The dotted line in the middle is a bit strange and unnecessary.

#### Improvements

<p align="center">
<img src="./images/5.12_swd.png" width="55%" >
</p>
<p align="center">
<img src="./images/5.12_my.png" width="55%" >
</p>

#### Tricks <a name="bar_gap_trick"></a>
* The colors in Tableau’s stacked bar chart are next to each other. To make the distance between them, I insert blank percentage (0.5%) between the segments data in the tables.

