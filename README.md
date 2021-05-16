# visualization-learning
A new start

**《大数据时代的可视化与协同创新》**

大数据时代：  
4V  volume velocity variety value  
更多，更杂，更好（相关性）  

数据可视化：   
商务智能大众化；人和数据交互式分析（提供用户友好界面）  
What：把数据转换为图形图像的方式，帮助人们理解大量的和复杂的数据    
·分类：科学可视化（科研数据；已有结构）、信息可视化（抽象数据；缺乏结构）、可视分析（新兴；集成了算法）  
·目的：理解数据（可视化---通过交互图形利用人类视觉&领域知识<如乒乓球赛策略> v.s.数据挖掘---通过算法利用强大算力）  
·特点：信（准确）达（清晰易用）雅（美感）  

可视化与设计：  
Metaphor  
1）钟表：时间（表盘位置）+车流量（柱状图高度）+车速（颜色）-->选择出行时间和路径  
2）向日葵：主题盘+用户组（某种联系的组合，如关系、地理位置）+扩散路径（时间等值线+情感色）--->社交媒体上的热门话题、转推时间和对象、情感态度  
3）河流：话题（一条河流）+时间（水平轴）+话题热度（宽度）+话题的分裂合并（河流交错）+[原因（其他可视化）]---> 研究领域主题演变  

存在的问题&机遇：  
1）大数据噪音（完整性&精确性）  
2）大数据本身的性质（规模&复杂度）：需要跨领域大众合作  
3）“在位分析”（不依赖数据库）  
4）异构数据（类型多元）  


**《A Tour through the Visualization Zoo》**
Spatial position ---> accurate decoding of numerical data（角度、长度、面积、体积、颜色饱和度）  
Position coding? P2  

-Goal:  
·sophisticated and unusual techniques (complex data sets)  
·exotic&useful forms (time-series data-->statistical data--->maps-->hierarchies--->networks)  
共性： data properties<---mappings---> visual attributes (positions, size, shape, color)  
用不同的视觉元素，以最好的方式，展现数据特征  
-Tools: 
Protovis(开源语言 for 基于web的数据可视化）


-Contents:  
1.Time-series data   
1)domains: finance, science, public policy  
2)Methods  
·index charts (relative changes<--selected index point)  
·stacked graphs (summation of values)--> limitations:negative numbers; data can’t be summed; interpret trends individually---> interactive search & filtering?   
·small multiples （多小图分别展示）  
·horizon graphs （多维度数据，增加图片信息量；需要更多时间解读）  

2.Statistical data  
1）可视化在统计数据中的应用：探索性数据分析（transformation&model choice）--> histogram, box and whisker plot（箱线图）  
2）Other Methods:  
·茎叶图:(alternative for histogram): histogram’s empty bar--> both overall and specific data  
·Q-Q (quantile-quantile 分位数) plots：require statistical knowledge  
·SPLOM(Scatter Plot Matrix 散点矩阵图): for multivariate data--> correlations between any pair  
·Parallel Coordinates（平行坐标图）: for multivariate data--->parallel axes+connect points( one poly-line is a single observation)  

3.Maps  
基于制图学（3D->2D）  
1）Methods  
· Flow Maps（流向地图）: for multivariate information(use points, directions, line thickness, color, distortion--->movement of a quantity in space & time)  
· Choropleth Maps（分级统计图; forlium包）: use varying color-->communicate data from different places; TAKE CARE: should use normalized data rather than raw data, perception of shades influenced by map regions（视觉错觉？）  
· Graduated Symbol Maps(alternative for Choropleth Maps) :use symbols rather than color shades--->可一次包含更多信息(circles, pie charts...)  
· Cartograms（变形地图）:  不再以地图上的地理位置划分，适当扭曲---> many types e.g. Dorling cartogram  

4.Hierarchies（数据层次结构）  
Micro&macro observations; explore organization  
· Node（节点）-link diagrams: (adjacency) different tree-layout algorithms  
I)the Reingold Tilford algorithm:长得像决策树  
II)the dendrogram (or cluster) algorithm：环形,use space efficiently（笛卡尔&极坐标系）  
III)Indented tree: used in operating system  
· Adjacency Diagrams:（space filling : arcs or bars instead of link between parent and child; adjacency）  
I)Node-link（I）的替代版，solid areas instead of link--->多了一维度，面积大小可表示...  
IV)Sunburst layout:  （笛卡尔&极坐标系）  
· enclosure diagrams: (space filling; containment instead of adjacency)  
I)Tree map: native rectangle 切割--> squarified tree maps (readability & size estimation better?)  
II)Packing circles: effectively reveals hierarchy & size compare vs wasted space(than rectangle subdivision)  

5.Networks  
Explore relationship; 可以说hierarchy是networks 的一种形式; Mathematical term for network: graph  
Challenge: effective layout --->techniques e.g. 最小化边缘交叉数  
· Force-directed Layouts:模仿物理系统（带点互斥小球，弹簧连接）  
· Arc diagrams: 半圆连线作为link; good ordering of nodes (seriation)--->cliques and bridges  
·Matrix Views: color&saturation--->values; seriation matters(e.g. community-detection algorithms) ; no crossings even for large networks ; quick spot clusters&bridges vs path-following difficult  
  
总结：  
1、根据Goal，一般展现的数据特征有Macro和Micro两部分，不同的作图法侧重不同点；  
2、可以多种图混搭，可以增加信息容纳量（map上加饼状图）；  
3、基本构图规律(除了时间序列数据)：  
·单个数据单元：点（位置、颜色）；块（面积、位置、颜色、颜色饱和度）-->可方可圆可扇形  
·组合方式：连线（直线、弧线）-->直形、树形、环形；拼接-->方形、环形、聚集；依托已有形状（Map、Matrix等）  

**《A brief history of data visualization》（Lecture）**  
Main idea: factors; computational tools; research-->future  
