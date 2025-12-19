---
layout: page
title: Research
permalink: /research/
description: 
nav: true
nav_order: 2
display_categories: #[work, fun]
horizontal: false
---
# **Methane inverse modeling**
<div class="row justify-content-sm-left"> <div class="col-sm-5 mt-3 mt-md-0"> {% include figure.html path="assets/img/methane.png" title="Methane emissions from the top 15 countries (East et al. 2025)" class="img-fluid" %} </div></div>
*Figure: East et al., 2025, Nat. Comm., Figure 3*  


Methane is the second most important greenhouse gas behind carbon dioxide and is responsible for about ~1/3 of global warming since preindustrial times. Methane is emitted from both anthropogenic (human-caused) and natural sources. Atmospheric methane can be remotely sensed from satellite instruments that measure sunlight reflected off Earth's surface. In my research, I use satellite measurements, high-resolution flux inversions, and chemical transport modeling to estimate the magnitude, sources, and timing of methane emissions.


Check out the interactive Worldwide Methane Emissions dashboard, built around data from my research at [worldwidemethaneemissions.com](https://worldwidemethaneemissions.com/).

**Relevant publications:** [East et al. 2025 *Nat. Comm.*](https://doi.org/10.1038/s41467-025-67122-8), [East et al. 2024 *Geophys. Res. Lett.*](https://doi.org/10.1029/2024GL108494)



# **Climate impacts on air quality**

<div class="row justify-content-sm-left"> <div class="col-sm-10 mt-3 mt-md-0"> {% include figure.html path="assets/pdf/fig4.pdf" title="Future ozone pollution" class="img-fluid" %} </div></div>
*Figure: East et al., 2024, Earth's Future, Figure 4*  

Climate change is projected to influence future surface-level air quality by changing concentrations of PM<sub>2.5</sub> and O<sub>3</sub> (ozone), two air pollutants that are harmful to human health. However, the magnitude and even the sign of that impact are uncertain. In my research, I use a model that couples economic drivers of GHG emissions, climate, and 3-D atmospheric chemistry to project climate's impact on air quality under multiple potential scenarios. My research quantifies the uncertainty in these projections and attributes it among known uncertainties in climate projections (GHG emissions scenario, natural variability, and climate model response uncertainty). I also examine the projected influence of climate on extreme O<sub>3</sub> pollution events, and find that moderate levels of climate change could bring 8.5 million U.S. residents into non-compliance with existing air quality standards by 2050.

**Relevant publications:** [East et al. 2024 *Earth's Future*](https://doi.org/10.1029/2023EF003941), [East et al. 2022 *Environ. Res. Lett.*](https://doi.org/10.1088/1748-9326/ac8d17)

Media: ["Ozone: An unseen health threat makes a comeback with climate change" (AAMC News)](https://www.aamc.org/news/ozone-unseen-health-threat-makes-comeback-climate-change);
["Climate Change Will Make Air Pollution Worse. Here’s How." (NC State News)]("https://news.ncsu.edu/2024/06/climate-change-and-ozone/) 



# **Satellite chemical data assimilation**
<div class="row justify-content-sm-left"> <div class="col-sm-10 mt-3 mt-md-0"> {% include figure.html path="assets/pdf/East2022ACPfig1.pdf" title="Chemical data assimilation and NOx emissions inversion framework" class="img-fluid" %} </div></div>
*East et al., 2022, ACP, Figure 1*  

I developed and applied an inverse modeling framework that uses satellite observations of NO<sub>2</sub>, an air pollutant that can be viewed from space using sunlight reflected off Earth's surface, to estimate emissions of NO<sub>X</sub>, a related air pollutant. The framework uses 3D-variational satellite chemical data assimilation to update model simulations of air pollution to match observations. This is commonly used in weather forecasting to help models better match the real world; here, I'm applying it to atmospheric chemistry! I used the framework to estimate 2019 NO<sub>X</sub> emissions from around the Northern Hemisphere, and found that my emissions estimates help the model better reproduce concentrations of NO<sub>2</sub> and O<sub>3</sub> observed in the real world.

**Relevant publications:** [East et al. 2022 *Atmos. Chem. Phys.*](https://doi.org/10.5194/acp-22-15981-2022)


# **Air quality modeling in Latin America**
<div class="row justify-content-sm-left"> <div class="col-sm-10 mt-3 mt-md-0"> {% include figure.html path="assets/img/bogota_jde.jpeg" title="Air pollution in Bogota, Colombia" class="img-fluid" %} </div></div>
*Air pollution in the morning inversion layer over Bogotá during a research visit.*  

Poor air quality disproportionally impacts cities in low- and middle-income countries. In Bogotá, Colombia, a metropolitan area with over 10 million inhabitants, PM<sub>2.5</sub> levels regularly exceed air quality guidelines, harming human health. Although there is public interest to improve the city's air quality, the main sources of PM<sub>2.5</sub> weren't well understood. I used a modeling framework based on EPA's CMAQ model (a 3-D model of atmospheric chemistry and transport), to simulate urban air quality in Bogotá and reveal major emissions soures. We found that resuspended dust from unpaved roads is the largest local source of PM<sub>2.5</sub> and can contribute over 30% of the pollution across the city, and that paving roads can lead to PM<sub>2.5</sub> decreases of nearly 10 μg/m3 (that's a lot!) by 2030. This study was the first to use a comprehensive model to determine sector contributions to air pollution in Bogotá, and it demonstrated an approach to guide pollution management in developing cities facing comparable challenges.

**Relevant publications:** [East et al. 2021 *Sci. Total Environ.*](https://doi.org/10.1016/j.scitotenv.2021.145894)  

Media: ["Researchers Use Air Quality Models to Reflect Polluted Reality in Latin America" (NC State News)](https://news.ncsu.edu/2021/03/air-models-latin-america/) 

<!-- pages/projects.md -->
<div class="projects">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_projects = site.projects | where: "category", category -%}
  {%- assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.projects | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>
