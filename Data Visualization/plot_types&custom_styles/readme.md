In this course, you've learned how to create many different chart types. Now, you'll organize your knowledge, before learning some quick commands that you can use to change the style of your charts.
在本课程中，您学习了如何创建许多不同的图表类型。现在，您将组织您的知识，然后学习一些可用于更改图表样式的快速命令。

# What have you learned?

<img src="https://storage.googleapis.com/kaggle-media/learn/images/LPWH19I.png" height="500" width="1000" usemap="#plottingmap" />
<map name="plottingmap">
  <area shape="rect" coords="262,342,402,476" href="https://www.kaggle.com/alexisbcook/hello-seaborn" title="EXAMPLE: sns.lineplot(data=my_data)">
  <area shape="rect" coords="8,75,154,200" href="https://www.kaggle.com/alexisbcook/bar-charts-and-heatmaps" title="EXAMPLE: sns.swarmplot(x=my_data['Column 1'], y=my_data['Column 2'])">
   <area shape="rect" coords="8,200,154,350" href="https://www.kaggle.com/alexisbcook/bar-charts-and-heatmaps" title="EXAMPLE: sns.regplot(x=my_data['Column 1'], y=my_data['Column 2'])">
   <area shape="rect" coords="8,350,154,500" href="https://www.kaggle.com/alexisbcook/bar-charts-and-heatmaps" title='EXAMPLE: sns.lmplot(x="Column 1", y="Column 2", hue="Column 3", data=my_data)'>
      <area shape="rect" coords="229,10,393,160" href="https://www.kaggle.com/alexisbcook/bar-charts-and-heatmaps" title="EXAMPLE: sns.scatterplot(x=my_data['Column 1'], y=my_data['Column 2'], hue=my_data['Column 3'])">
     <area shape="rect" coords="397,10,566,160" href="https://www.kaggle.com/alexisbcook/line-charts" title="EXAMPLE: sns.heatmap(data=my_data)">
     <area shape="rect" coords="565,10,711,160" href="https://www.kaggle.com/alexisbcook/line-charts" title="EXAMPLE: sns.barplot(x=my_data.index, y=my_data['Column'])">
     <area shape="rect" coords="780,55,940,210" href="https://www.kaggle.com/alexisbcook/scatter-plots" title="EXAMPLE: sns.jointplot(x=my_data['Column 1'], y=my_data['Column 2'], kind='kde')">
     <area shape="rect" coords="780,210,940,350" href="https://www.kaggle.com/alexisbcook/scatter-plots" title="EXAMPLE: sns.kdeplot(data=my_data['Column'], shade=True)">
   <area shape="rect" coords="780,360,1000,500" href="https://www.kaggle.com/alexisbcook/scatter-plots" title="EXAMPLE: sns.histplot(a=my_data['Column'])">
</map>


由于不总是很容易决定如何最好地讲述数据背后的故事，我们将图表类型分为三大类来帮助实现这一点。

- **趋势** - 趋势被定义为一种变化模式。
  - `sns.lineplot` - **折线图**最适合展示一段时间内的趋势，并且可以使用多条线来展示多个组中的趋势。

- **关系** - 你可以使用多种不同类型的图表来理解数据中变量之间的关系。
  - `sns.barplot` - **条形图**用于比较不同组之间的数量。
  - `sns.heatmap` - **热图**可以用于在数字表格中查找颜色编码的模式。
  - `sns.scatterplot` - **散点图**展示两个连续变量之间的关系；如果进行颜色编码，还可以展示与第三个[分类变量](https://en.wikipedia.org/wiki/Categorical_variable)的关系。
  - `sns.regplot` - 在散点图中包含一条**回归线**可以更容易地看到两个变量之间的线性关系。
  - `sns.lmplot` - 当散点图中包含多个颜色编码的组时，这个命令用于绘制多条回归线。
  - `sns.swarmplot` - **分类散点图**展示了一个连续变量与一个分类变量之间的关系。

- **分布** - 我们可视化分布是为了展示一个变量中可能出现的值及其出现的概率。
  - `sns.histplot` - **直方图**展示单个数值型变量的分布。
  - `sns.kdeplot` - **KDE图**（或**二维KDE图**）展示单个数值型变量（或两个数值型变量）的估计平滑分布。
  - `sns.jointplot` - 这个命令用于同时显示二维KDE图及每个单独变量对应的KDE图。


