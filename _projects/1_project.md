---
layout: page
title: Low-Cost PM Composition
description: Graduate Thesis on using low-cost air sensors and ML to predict PM composition. Thesis available on request.
img: assets/thesis/software_arch.PNG
importance: 1
category: work
related_publications: Sharpe-willjsh-MEng-CEE-2023-thesis
---

# Abstract
<p>Particulate matter (PM) is a serious threat to human health and contributes to
millions of premature deaths a year globally. Access to source attribution and compositional data of PM can have many benefits from easier regulation to enabling a better understanding of the negative health effects associated with PM. Acquiring compositional data for ambient PM generally has a high associated cost and is done using complex instrumentation, manual postprocessing, and labor intensive lab work. 
These approaches produce very high quality data, but have low spatiotemporal resolution
and a high cost. 
This work explores a novel method to generate basic compositional
data for ambient PM with low-cost, easily deployable apparatuses in concert with a
simple fully connected neural net. 
Simulated effects of thermal denuders as well as
dryers/humidifiers are used to perturb aerosols before they enter simulated low-cost
optical particle counters (OPCs). This provides information on the volatility and
hygroscopicity of the aerosols. These OPC outputs are processed programmatically
and fed into a neural net to classify what category an incoming aerosol belongs to.</p>
<p>
This method is run for both compound-derived categories which mimic real PM sources
(Sea Salt, Biomass Burning, Dust, and Urban Smog), and property-derived aerosols
which present more idealized conditions. The results of this method are near-perfect
classification for single mode aerosol distributions and over 90% correct classification
for two mode aerosol distributions. The results on the property-derived aerosols have
shown robustness to changing aerosol properties, as well as to changing apparatus
and ambient conditions. This work provides proof of concept for future real world
experiments to verify this method and presents an experimental setup for this purpose.
Having access to compositional data for ambient PM should allow access to PM
sources at a very high spatiotemporal resolution for a relatively low price. This basic
source attribution could provide the data needed for better informed regulation as
well as future scientific work.
</p>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/thesis/software_arch.PNG" title="Model" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    High level overview of simulation model.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/thesis/compound_derived_double.png" title="Compound Derived" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/thesis/property_derived_all.png" title="Property Derived" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model categorization confusion matrix for all bimodal flows, showing an overall accuracy of greater than 94%.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/thesis/lab_setup.png" title="Lab Setup" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Cartoon representation of labratory setup built to verify simulation model.
</div>
