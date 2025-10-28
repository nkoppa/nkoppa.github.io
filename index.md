---
title: "Nisha Koppa"        
layout: default
# description: "" 
---



<link rel="stylesheet" href="/assets/css/custom.css?v=3"> 

<img src="/assets/img/me.jpg" alt="Nisha Koppa" width="320" 
     style="border-radius: 50%; display: block; margin: 0 auto 2rem; height:auto;
            border: 4px solid #d7bac8; box-shadow: 0 6px 14px rgba(0,0,0,0.12);">


# **About Me**

Hello! My name is Nisha. If you just stumbled across this, here’s a little bit about me:

I’m a 3rd year PhD student in [Environmental Studies](https://www.colorado.edu/envs/) at the University of Colorado Boulder. I also hold a Masters degree in [Economic Development](https://www.lusem.lu.se/study/masters-programmes/global-development-population-and-economic-change-masters-programme) from Lund University, Sweden and a Bachelors (Research) in [Economics](https://snu.edu.in/programs/bsc-research-in-economics/) from India. 

As part of my PhD, I work on something that touches everyone: **Food**. Specifically,I study how climate change and policy decisions ripple through global food systems — from government trade interventions to the everyday choices of farmers. My work spans three themes: the role of trade policy during climate shocks, how path-dependent institutions lock in agricultural practices, and how farmers adapt on the ground. Put together, I intend to explore how we can make our food systems resilient and what holds them back.  

# **Publications**

## **Academic Papers**

**Geospatial assessment of flood-tolerant rice varieties to guide climate adaptation strategies in India** *N. Koppa, G. Amarnath* *Climate*, 9(10), 151 (2021). [Link](https://doi.org/10.3390/cli9100151)  

**Statistical downscaling differences strongly alter projected climate damages** *S. Miller, N. Ormaza-Zulueta, N. Koppa, A. Dancer*  *Communications Earth & Environment*, 6(1), 145 (2025). [Link](https://doi.org/10.1038/s43247-025-01145-7)  

**Review of Existing Platforms, Gaps and Challenges in CIS delivery in Zambia** *G. Amarnath, N. Alahacon, N. Koppa, T. Sharma, N. Ngowenani, …*  *Accelerating Impacts of CGIAR Climate Research for Africa* (2022). [Link](https://www.climate.cgiar.org/)  

## **Earth Data Science Projects** 

#### **1. Map of CU Boulder** 

<embed type="text/html" src="assets/img/CU.html" width="400" height="400">

#### **2. Warming in Death Valley National Park (1990–2024)**

![Annual Average Temperature in Death Valley National Park (1990–2024)](assets/img/death_valley_temp.png)

Death Valley National Park in eastern California is famous for record heat, extreme aridity, and below-sea-level basins. Stark landscapes—salt flats, dunes, badlands, and spring-fed oases—host desert-adapted species living near thermal limits. That makes the park a clear setting to examine recent warming. As seen from the fugure above, from 1990 to 2024, annual average temperature in Death Valley rose by **~0.125 °C per year** (**~1.25 °C per decade**). Most of the warmest years occur after 2015. A simple OLS fit explains **~75%** of year-to-year variation, indicating a strong upward trend. [<a href="{{ '/assets/img/climate-coding-portfolio-assignment-2.html' | relative_url }}"
   target="_blank" rel="noopener">View full workflow</a>]


#### **3. Species Migration**

#### **Exploring Swainsons Thrush (Catharus ustulatus) Migration in the 2023 using Global Biodiversity Information Facility (GBIF)**

![Swainson’s Thrush](assets/img/Swainson.jpeg)

Swainson’s Thrush (Catharus ustulatus) — Photo credit: [Birds of the World](https://birdsoftheworld.org/bow/species/swathr/cur/introduction)



**Background**

Swainson’s Thrush (scientific name Catharus ustulatus), is a small to medium-sized **migratory songbird** in the thrush family (Turdidae). It is known for its olive-brown back, buff-colored underparts, a distinct pale eye-ring, and a slightly spotted breast. The species is distributed widely across northern North America for breeding, and winters in Central and South America. ([Audubon.org](https://www.audubon.org/field-guide/bird/swainsons-thrush))


As a classic Nearctic–Neotropical migrant, Swainson’s Thrush travels thousands of kilometers each year. Spring migration typically occurs from mid-March to early June, while fall migration spans late July to early November. Inland birds tend to follow interior routes through the central U.S. into Central America, whereas coastal populations use a more Pacific flyway. These birds rely on forested stopover habitats along their route for rest and refueling, making them particularly sensitive to habitat changes across a vast geographic range ([E-bird Status and Trends](https://science.ebird.org/en/status-and-trends/species/swathr/range-map))

Although Swainson's Thrush is still considered one of the most common birds of northern spruce-fir forests, populations are declining even where abundant, particularly in Alaska and the Northeast ([Birds of the world](https://birdsoftheworld.org/bow/species/swathr/1.0/introduction?printable). While the reasons are not known yet, the Swainson’s Thrush faces growing threats from habitat loss, window strikes during nocturnal flights, and potential climate-related shifts in food availability. As different populations use distinct migration corridors, conservation strategies must account for their migratory connectivity — protecting not just breeding grounds, but also critical stopover and wintering habitats.([Humpel et al., (2020)](https://www.nature.com/articles/s41598-020-62132-6))


**Data and Methods**

*Data*

For this analysis, I use the species observation data from the Global Biodiversity Information Facility (GBIF). The Global Biodiversity Information Facility (GBIF) is a free, global database that brings together information about where and when different species have been observed. These records come from many sources—like research projects, birdwatching apps, museum collections, and citizen science initiatives. Each record usually includes the species name, the exact location (with coordinates), the date of the observation, and who collected the data. Because the data are standardized and easy to access, GBIF is widely used to study species distributions, biodiversity patterns, and migration routes. This data was directly downloaded to my computer using the pybif package from python (note: I used the already provided notebook to get this data). 

*Method*
For this small project, I used bird observation data for Swainson’s Thrush from the GBIF website, which included the locations and months when each bird was seen. I turned this data into a geospatial data frame so I could work with the coordinates. I also loaded a map of North American ecoregions (this was downloaded using the sample notebook provided) and made the shapes simpler so the map would plot faster. Using a spatial join, I matched each bird sighting to the ecoregion where it happened. Then, I grouped the data by ecoregion and month to count how many birds were seen in each place and time. To make the results fair, I normalized the counts to account for differences in region size and how often people reported sightings. Finally, I created an interactive map that lets you explore where Swainson’s Thrushes were found throughout the year, showing their migration routes and important habitats. For this analysis, I used the python software, and employed several packages like os, pathlib, calendar, zipfile, getpass, glob, geopandas, pandas, hvplot.pandas, cartopy.crs, and panel. 

Please find my full code for this analysis in my [repository](https://github.com/earthlab-education/02-migration-nkoppa/blob/main/notebooks/Swainsons_portfolio.ipynb)

**Map and Plot**

The interactive migration map provides a spatial and temporal perspective of Swainson’s Thrush movements across North American ecoregions during the year 2023. After normalizing observation counts, the visualization accounts for differences in sampling effort and ecoregion area, enables a more accurate comparison of habitat use. Results indicate that Swainson’s Thrush predominantly occupies northern forested ecoregions during the breeding season, with a marked southward shift in distribution during autumn migration. The identification of key stopover and breeding habitats highlights the species’ reliance on a diversity of ecological regions throughout its annual cycle. These findings can be important for conserving a network of habitats along migratory routes to support population connectivity and long-term species persistence.

The interactive migration map below shows Swainson’s Thrush movement patterns across North America. You can zoom, pan, and interact with the data directly below:

<iframe src="assets/img/Swainsons_Thrush_Migration_2023.html" width="100%" height="600px"></iframe>

*References*

1. Audubon. 2025. “Swainson’s Thrush – *Catharus ustulatus*.” *Audubon Field Guide*. National Audubon Society.  
[https://www.audubon.org/field-guide/bird/swainsons-thrush](https://www.audubon.org/field-guide/bird/swainsons-thrush)
2. eBird. 2025. “Swainson’s Thrush — Status and Trends.” Cornell Lab of Ornithology.  
[https://science.ebird.org/en/status-and-trends/species/swathr/range-map](https://science.ebird.org/en/status-and-trends/species/swathr/range-map)
3. Humpel, M., P. D. Taylor, I. Maggini, and D. R. Norris. 2020. “Migratory Connectivity and Conservation of Swainson’s Thrush (*Catharus ustulatus*) Using Automated Radio Telemetry.” *Scientific Reports* 10: 6364.  
[https://www.nature.com/articles/s41598-020-62132-6](https://www.nature.com/articles/s41598-020-62132-6)
4. Mack, D. E., and W. Yong. 2020. “Swainson's Thrush (*Catharus ustulatus*), Version 1.0.” In *Birds of the World*, edited by A. F. Poole. Cornell Lab of Ornithology.  
[https://doi.org/10.2173/bow.swathr.01](https://doi.org/10.2173/bow.swathr.01)
6. U.S. Geological Survey. 2004. “Stopover Ecology of Western Avian Populations.” *USGS Fact Sheet 2004–3090*.  
[https://pubs.usgs.gov/fs/2004/3090/](https://pubs.usgs.gov/fs/2004/3090/)
7. GBIF.org. (21 October 2025.) GBIF Occurrence Download. [https://doi.org/10.15468/dl.c96k9k](https://doi.org/10.15468/dl.c96k9k)




# **Contact Information**
[Email](mailto:nisha.koppa@colorado.edu) . [Linkedin](https://www.linkedin.com/in/nisha-koppa-44a642120/) . [Github](https://github.com/nkoppa) 
