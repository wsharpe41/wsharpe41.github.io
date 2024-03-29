---
layout: page
title: US Climate Policy
description: Simple dashboard visalualizing GHG goals and reality in US States
img: assets/us_climate_viz/national_sector.png
importance: 3
category: work
---

This project is a simple dashboard which shows various state and US national climate goals and compares them to reality. It is a work in progress and will be updated as new data becomes available. This was developed in Python primarily using Dash, Plotly, and Flask. A live version of the dashboard can be spun up using the associated GitHub repo here: https://github.com/wsharpe41/climate-legislation-viz. I also used this data for the capstone project of the Google Data Analytics course in the form of a notebook. This version has increased analysis and can be found here: https://www.kaggle.com/code/willsharpe/us-ghg-breakdown-capstone .
<br>
<h3>National Data</h3>
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
<br>
<br>
<h3>State Data</h3>

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
