---
layout: page
title: Climate Policy Visualization
description: Class Project to visualize effects of various climate policies on global enivronmental indicators
img: assets/global_policy/ecodata.PNG
redirect:
importance: 3
category: work
---

<p>This project attempts to correlate various Global Environmental Indicators to acceptance of international environmental actions. Data for this project was taken from https://www.kaggle.com/datasets/ruchi798/global-environmental-indicators. This data consists of many CSVs which have yearly time series data on different environmental indicators such as CO2 emissions or hazardous waste production for each country. This environmental indicator data was processed to show yearly percent change instead of yearly total amounts for each country to give a better idea of the time series trends. This dataset also contains information on various international environmental agreements which indicates the year which each country accepted each agreement. With the yearly trends and the data on agreement acceptance we were able to create a visualization showing change in time of relevant indicators versus the acceptance of legislation to show a correlation between the two.
</p>
<br>
<p>To create these visualizations various tableau workbooks were created, which are stored in the tableau_workbooks folder as well as publically available at https://public.tableau.com/app/profile/will.sharpe. These visualizations are maps with the outline of each country indicating whether or not it has accepted the environmental agreement and the fill color of the country representing the value or change of the environmental indicator of concern. We created one tableau workbook for each of six agreements: Basel Convention, UN Convention to Combat Desertification, Paris Agreements, Kyoto Protocol, UNFCCC, and the World Heritage Convention.
</p>
<br>
<p>
To show all of the visualization in a simple manner we used Flask to create a webpage. This webpage consists of a homepage with an overall map with a tab for each agreement. To install and run this project you can create a GitHub Codespace with Python and Flask installed and then run the web_app.py script to spin up a local version of the webpage.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/global_policy/Paris.PNG" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Example visualization showing yearly percent change in various GHGs with country outline indicating whether or not the country has accepted the Paris Agreement.
</div>

