---
layout: page
title: US Climate Policy
description: Simple dashboard visalualizing GHG goals and reality in US States
img: assets/us_climate_viz/national_sector.png
importance: 3
category: work
---

This project is a simple dashboard which shows various state and US national climate goals and compares them to reality. It is a work in progress and will be updated as new data becomes available. This was developed in Python primarily using Dash, Plotly, and Flask.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/us_climate_viz/national_sector.png" title="National GHG Sectors" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    National GHG Emissions by Sector
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/us_climate_viz/national_by_state.png" title="State GHGs" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    National GHG Emissions by State
</div>

The above images show some of the national level data on the dashboard for years 1990 to 2021 with all numbers in millions of metric tons of CO2 equivalent. You can see that electrical power is the largest source national, and Texas produces far and away the most emissions for the entire time frame. The dashboard itself is interactive and allows you to get precise values, and filter out certain states on these charts.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/us_climate_viz/ca_goals.png" title="CA Goal v Actual" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Proposed GHG Goals vs Actuality by State
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/us_climate_viz/GHGs_by_sector_state.png" title="GHG by Sector State" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    State GHG Emission Sector Breakdown
</div>

The above images show some of the state level data on the dashboard for years 1990 to 2020 with all numbers in millions of metric tons of CO2 equivalent. The data shown uses California as an example. This data is available for all 50 states and can be selected in the dashboard. The first chart shows the actual GHG emissions change versus the change associated with each climate goal in that state. The chart assumes a linear progression towards the goal, which admittedly is less generous than what state plans likely assume. The second chart shows the sector breakdown of GHG emissions for the state. The dashboard itself is interactive and allows you to get precise values.

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
