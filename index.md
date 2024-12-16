# Portfolio website for Chris Quinn

<div>
<img 
    src="https://avatars.githubusercontent.com/u/124209477?v=4"
    width="25%" 
    alt="Headshot of Christopher Quinn" 
    title="Headshot of Christopher Quinn">
</div>
I am a currently a 3rd-year PhD student in Environmental Studies at the University of Colorado Boulder. My doctoral research examines microclimate variation as a function of tree canopy in Boulder's urban forest, investigates urban forest management practices around the U.S. using mixed methods, and assesses historical and future climate change on public lands. I am interested in temporal and spatial patterns of ecosystem services, how land managers optimize for ES delivery, and the use of weather and climate change projection data in different decision-making contexts (e.g., natural resources, human health). My background includes sociology, public health (epidemiology), and health services research. 

More about me: 
  * [Current CV](https://drive.google.com/file/d/1fRQc1oAe1UGQX836tB3dbWLjDYeP7x3U/view?usp=sharing). 
  * [My Google Scholar page](https://scholar.google.com/citations?user=n7tuBC4AAAAJ&hl=en&authuser=1).
  * [LinkedIn](www.linkedin.com/in/christopher-quinn-268b76aa). 

At CU I am a member of the People, Environment, Economics, and Programming (PEEP) Lab, led by ENVS Assistant Professor Steve Miller. Find out more about our group at [www.peeplab.org](https://www.peeplab.org).

![Ponderosa pine trees on a sloping ridge](https://github.com/cmq879/cmq879.github.io/assets/124209477/7222af48-b920-4cc3-a768-6aed16ce7ae4 "Ponderosa pines trees in Colorado. Photo by C. Quinn")

## Earth Lab Fundamentals of Earth Data Science course, Fall 2024
### Assignment Posts

### "First" Map Post
A large public research university not far outside of Chicago's famed 
Loop, the [University of Illinois at Chicago was established in the 1960s](https://www.uic.edu/about/history/) 
near the interchange of two interstate highways and several different 
neighborhoods<sup>1</sup>. It's east campus adjacent to downtown Chicago includes 
a nearly complete list of the colleges one expects to find at a R1 
institution. The west side health campus houses several additional schools
and colleges, including the School of Public Health. 

I'm including this interactive map where you can scroll out and identify 
where the campus is relative to parts of the city you might have visited
if you've been to Chicago before. 

<embed type="text/html" src="imgs/uic.html" width="600" height="600">

I chose UIC for this map post because I studied and worked there for 10 
years , completing a B.A. in Sociology and M.S. in Epidemiology and 
working on health behavior-related community environment research at the
 Institute for Health Research and Policy.

<sup>1</sup> University of Illinois Chicago. History. https://www.uic.edu/about/history/



### Species Migration
##### Examining Migration of the Pacific Loon (Gavia pacifica) in 2023 using data from the Global Biodiversity Information Facility (GBIF)

The Pacific loon, *Gavia pacifica* (or *Colimbo pacífico* in Spanish) are one of five species of loons found in North America. Loons as a group are known for their distinctive and "haunting" calls, which include wails, hoots, and yodel sounds [(Committee to Protect Loons, n.d.)](https://loon.org/the-call-of-the-loon/). Male and female loons have a similar appearance, with black or dark gray heads and white-spotted or striped dark plumage.

Pacific loons are considered to be a medium- to long-distance migration species, breeding throughout Alaska and the northern Canadian provinces and spending winters off the Pacific coast of North America from southern Alaska through Baha California, Mexico and the Sea of Cortez [(Billerman et al., 2022)](https://www.allaboutbirds.org/guide/Pacific_Loon/maps-range). However, Pacific loons have been spotted throughout many parts of the U.S., including along the Atlantic coast and in the Northwestern Passages in Canada [(eBird, 2021)](https://ebird.org/species/pacloo). 

According to [Audubon.org](https://explorer.audubon.org/explore/species/1497/pacific-loon) (2024), the Pacific loon is a species of least concern in the International Union for the Conservation of Nature's (IUCN) threatened species ratings, with an estimated global population of about 840,000 individuals.

<footer>
    <a data-flickr-embed="true" data-footer="true" href="https://www.flickr.com/photos/mickthompson/19238537242/in/photolist-vj3wRY-2ovBQMc-b9j9ov-2j3jZHY-2ntaWdC-2oC6cDC-2nntnDC-HLwDEG-28kJ9Ly-4S5YCf-2iRcV9S-S2jQjR-2j3rboZ-2n4xgwt-2nnvPT4-284dNe6-Cg8B2p-Xnruj1-GDe29X-vhZQpu-28HdFvN-unJp9V-2nideZQ-2qfonJJ-qpkqQ2-NbwGEF-2nt9Ddg-PhHejN-2p6MXBb-Xnruhh-PhGWJ3-PhGUzU-ca4y95-PhHaUm-2p6LnBY-CfVufJ-21we98p-2f1Ncy5-zpZ35i-8UrVUs-4c2ozn-LaWqw5-2f1NbuG-H89Bjd-GmKeaf-Ciw2Gy-2nt9DfR-pVWECy-2nt3aDZ-2nt9CDf" title="Pacific Loon"><img src="https://live.staticflickr.com/65535/19238537242_f9b5c528f7_z.jpg" width="640" height="427" alt="Pacific Loon"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
    <p>Image credit: Flickr/Mick Thompson, CC by-NC 2.0</p>
</footer>

##### Data and Methods
###### Global Biodiversity Information Facility (GBIF)

The Global Biodiversity Information Facility (GBIF) website compiles a variety of species identification and observation data, including observations by citizen scientists. It is an important crowd-sourced tool for biodiversity research and has been used by researchers in scientific publications. GBIF compiles data from various species observation logging platforms like iNaturalist. To use GBIF you simply need to identify a species of interest and browse around the website to identify data for that species. You can download data directly from the website to your local machine, or for a reproducible workflow you can access GBIF data through python using the pygbif packages (specifically the occurrences and species functions). Other packages needed for this analysis include os, pathlib, calendar, zipfile, getpass, glob, geopandas, pandas, hvplot.pandas, cartopy.crs, and panel. Individual species data are accessible via a species key code that can be queried through python.  

In my analysis I examine movement of Gavia pacifica across ecoregions, which requires a global shapefile of ecoregions. I used one hosted at [https://storage.googleapis.com/teow2016/Ecoregions2017.zip](https://storage.googleapis.com/teow2016/Ecoregions2017.zip). Ecoregions are geographically contiguous areas of similar climate and habitat that are characterized by those factors as well as the plants and animal species that inhabit them. A step that helps with faster processing here is to simplify the ecoregion geodataframe geometry.

Given the spatial component to this analysis, only observations in GBIF with geographic coordinates were used. I also excluded single observations in an ecoregion and month due to the potential for species misidentification. I then normalized the occurrences by ecoregion and month to adjust for unequal sampling effort across different parts of the world. You can find the full code for this analysis in my [Jupyter notebook file in my project repository here.](https://github.com/earthlab-education/species-distribution-coding-challenge-cmq879/blob/main/notebooks/gavia_pacifica_migration.ipynb) 

#### Map and Plot

<embed type="text/html" src="imgs/gaviapac_migration_plot.html" width="800" height="800">

#### What the GBIF migration data tell us

According to GBIF-reported field observations in 2023, Gavia Pacifica overwinter in the Amazon region of South America, primarily in Brazil. However, the Pacific loon is known to overwinter off the Pacific coast of the U.S., so it is likely that these are mis-identifications of another species. 

It is important to keep in mind that when using crowd-sourced data such as that included in GBIF, there may not be 100% accuracy in identification. Therefore, it's possible that some observations are actually of different Gavia species, or even a different genus entirely. 

#### References

Natinoal Audubon Society. 2024. Field guide: Pacific Loon. https://explorer.audubon.org/explore/species/1497/pacific-loon 

Billerman S. M., B. K. Keeney, P. G. Rodewald, and T. S. Schulenberg (Editors) (2022). Birds of the World. Cornell Laboratory of Ornithology, Ithaca, NY, USA. https://birdsoftheworld.org/bow/home

eBird. 2021. eBird: An online database of bird distribution and abundance [web application]. eBird, Cornell Lab of Ornithology, Ithaca, New York. Available: http://www.ebird.org.

GBIF.org. (22 October 2024.) GBIF Occurrence Download. https://doi.org/10.15468/dl.c96k9k

Loon Preservation Committee. n.d. About Loons. https://loon.org/about-the-common-loon/

U.S. Geological Survey (USGS) - Gap Analysis Project (GAP), 2018, Pacific Loon (Gavia pacifica) bPALOx_CONUS_2001v1 Range Map: U.S. Geological Survey data release, https://doi.org/10.5066/F7MK6BXK.




## Historical Redlining in Cleveland and Vegetation Health

This analysis examines greenness of neighborhoods relative to historical redlining, or race-based exclusionary housing practices that were common in many cities in the U.S. in the middle-to-late 20th century. The [Digital Scholarship Lab](https://dsl.richmond.edu/) at the University of Richmond in Virginia ... [compiled spatial data on redlining](https://dsl.richmond.edu/panorama/redlining) using archival sources and developed redlining zone maps for numerous cities around the country. These maps are great tools for both teaching and learning, and the DSL has provided resources at the Mapping Inequality website. 

Some additional resources for further reading and data include the following:

    * [Ideastream: Racism was the primary reason Ohio neighborhoods were redlined, new study shows](https://www.ideastream.org/health/2023-02-02/racism-was-the-primary-reason-ohio-neighborhoods-were-redlined-new-study-shows)
    * [Visual Cleveland. Black Suburban Population Change, 1950-2010](https://visual.clevelandhistory.org/black-population-suburbs/)
    * Redlining maps for other Ohio cities: (https://guides.osu.edu/maps/redlining)
    * Berkeley Public Health: [50 years after being outlawed, redlining still drives neighborhood health inequities](https://publichealth.berkeley.edu/news-media/research-highlights/50-years-after-being-outlawed-redlining-still-drives-neighborhood-health-inequities)

#### Map of Redlining Zones in Cleveland
<embed type="text/html" src="imgs/cleve_rlplot1.html" width="1000" height="650">

The spatial redlining data in this map come the Digital Scholarship Lab at the University of Richmond. Residential areas were graded from A to D in terms of minority racial/ethnic groups' presence in the area. This was done for purposes of steering certain buyers away from areas with large non-white populations. In addition, securing mortgage loans in poorly-graded areas was very difficult. The effects of this type of systemic racism is perpetuated still today in economic, health, and environmental quality disparities, among others. 

#### Normalized Difference Vegetation Index

The data source for this is the Harmonized Landsat Sentinel-2 (HLS) which measures surface reflectance. The HLS imager was on NASA/USGS Landsat 8 and Landsat 9 satellites. The HLSL30 product I am using invludes spectral data at a 30-meter resolution. The technical name for the data is Nadir Bidirectional Reflectance Distribution Function (BRDF)-Adjusted Reflectance (NBAR). I am interested in recent data, and selected the July 26, 2023 imagery because it was a clear day in Cleveland. 

To measure greenness, I will calculate the Normalized Difference Vegetation Index (NDVI) for Cleveland. NDVI uses red- and near-infrared (nir) reflectance based on the following formula: 

NDVI = (NIR - RED) / (NIR + RED)

The measure ranges between 0 and, with 1 being the highest level of greenness or vegetation health. As such, it is generally best measured in the peak months of the growing season. The following map displays the estimated NDVI from July 26, 2023. 
<embed type="text/html" src="imgs/cleve_ndvi_map.png" width="800" height="800">

#### Analysis

The question here is whether NDVI score and redlining grade are related. My hypothesis is that they are, that we would see higher NDVI scores (more greenness) with an A and B redlining grade than with a C or D grade. To assess this, I'll use 2 models: a tree-based algorithm and a simple linear regression (using the sci-kit learn and statsmodels.api libraries, respectively). First, I'll look at basic means of each redlining grade across all the zones in the spatial redlining data and view it as a bar chart. 
<embed type="text/html" src="imgs/rl_grad_ndvi_means.html">

Next, I used a decision tree classifier to predict the redlining grade based on the NDVI score for each zone in the spatial redlining data. The map on the left shows the NDVI score in 2023 and the map on the right shows the redlining zones. 
<embed type="text/html" src="imgs/NDVI_and_redlining_plots_sxs.html" width="2000" height="700">

We can see that there is definitely some similarities where many of the darker green areas on the NDVI plot are also green on the redlining map. Next I'll calculate the error and see where the tree classifier didn't predict the correct grade for the zone.
<embed type="text/html" src="imgs/cleve_error_plot.html" width="1000" height="650">

For the second model I will run a linear regression of the NDVI score on grade as a categorical variable, with the highest grade as the reference. The results there showed that there were statistically significant differences in the NDVI score based on the redlining grade, with scores B, C, and D having significantly lower average NDVI scores compared to A grade zones, though the differences are very small. 
<embed type="text/html" src="imgs/redlining_ndvi_ols_summary.png" width="650" height="900">

Though the observed differences in greenness are night wildly different, there is a lingering difference between the old redlining zones in Cleveland. To further confirm this, I would consider some additional analysis. First, examining NDVI at different time points to ensure a consistent relationship would be important. Then, we might want to know more than just the NDVI - like what kinds of plants or trees are there? What is the extent of tree canopy cover that provides shade? What about species biodiversity? Analyses for another day!

#### References
Center for Public History + Digital Humanities. (2024). "Visual Cleveland. Black Suburban Population Change, 1950-2010".

Masek, J., Ju, J., Roger, J., Skakun, S., Vermote, E., Claverie, M., Dungan, J., Yin, Z., Freitag, B., Justice, C. (2021). <i>HLS Operational Land Imager Surface Reflectance and TOA Brightness Daily Global 30m v2.0</i> [Data set]. NASA EOSDIS Land Processes Distributed Active Archive Center. Accessed 2024-12-15 from https://doi.org/10.5067/HLS/HLSL30.002.

Nelson, R. K., Winling, L, et al. (2023). Mapping Inequality: Redlining in New Deal America. Digital Scholarship Lab. https://dsl.richmond.edu/panorama/redlining.

Last updated 16 Dec 2024


