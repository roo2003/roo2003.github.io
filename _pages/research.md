---
title: "ARSL - Research"
layout: textlay
excerpt: "ARSL -- Research"
sitemap: false
permalink: /research/
---

# Research

The following are the main areas we are currently working on:

- [Satellite remote sensing of clouds and precipitation](#Satellite-remote-sensing-of-clouds-and-precipitation)  
- [Microwave radiative modeling through precipitating clouds](#Microwave-radiative-modeling-through-precipitating-clouds)  
- [Balance and trends of atmospheric water cycle](#Balance-and-trends-of-atmospheric-water-cycle)  

<hr/>

## [Satellite remote sensing of clouds and precipitation]

### Passive microwave remote sensing of precipitation

Passive microwave signatures from satellites are based on emission and scattering from the liquid and frozen hydrometeors in the cloud columns. Warm emission signals indicate the presence of liquid water. In contrast, microwave signals at scattering channels with higher frequencies are attenuated by the amount and types of ice particles in the rain column. Our research focuses on the development of rainfall retrieval algorithms and improving retrieval accuracy. We are also working on applying machine learning methods to precipitation-type classification and inversion models. Followings are brief descriptions of the precipitation algorithm and retrieval error studies.

**(1) Advancement of the parametric rainfall retrieval algorithm**

The initial version of the parametric rainfall retrieval algorithm was developed for various spaceborne microwave radiometers in 2003 (Shin and Kummerow). It is based on simultaneous uses of space-borne radar, cloud-resolving, and radiative transfer models for the construction of a-priori information. This fully parametric rainfall retrieval algorithm is designed to be applicable to a wide variety of passive microwave sensors that currently exist and are planned for the future. The algorithm is continuously being improved by including radiative transfer simulations that are physically consistent with the cloud microphysics used in cloud models: Kim et al. (2013) and Choi et al. (2019).

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive1.jpg){: style="width: 70%; float: center; margin: 2%"}<be>

**[The section below is currently under construction. Please check back later for updates]**

 **Retrieval algorithm for monthly oceanic rainfall**

 With the accumulated satellite datasets for decades, it is possible that satellite-based data could contribute to sustained climate applications. Level-3 products from microwave sensors for climate applications can be obtained from several algorithms. For examples, the Microwave Emission brightness Temperature Histogram (METH) algorithm produces level-3 rainfalls directly, whereas the TRMM/GPM level-2 algorithms first generates instantaneous rainfalls and then temporal and spatial averaging process leads to level-3 products. The rainfall algorithm developed in this study follows a similar approach to averaging instantaneous rainfalls. However, the algorithm is designed to produce instantaneous rainfalls at an optimal resolution showing reduced non-linearity in brightness temperature (TB)-rain rate(R) relations. It is found that the resolution tends to effectively utilize emission channels whose footprints are relatively larger than those of scattering channels.

 This algorithm is mainly composed of a-priori databases (DBs) and a Bayesian inversion module. The DB contains massive pairs of simulated microwave TBs and rain rates, obtained by cloud and radiative transfer simulations. To improve the accuracy and efficiency of retrieval process, data mining technique is additionally considered. The entire DB is classified into eight types based on Koppen climate classification criteria using reanalysis data. Among these sub-DBs, only one sub-DB that presents the most similar physical characteristics is selected by considering the thermodynamics of input data. When the Bayesian inversion is applied to the selected DB, instantaneous rain rate with 6 hours interval is retrieved.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive2.jpg){: style="width: 70%; float: center; margin: 2%"}<br>

 **Retrieval error reduction**

 Vertically and horizontally inhomogeneous distributions of hydrometeors are often observed in precipitating clouds. The 3-D characteristics can then cause errors in the passive microwave rainfall measurements with the current off-nadir viewing sensors’ specifications. It was found that taking more viewing angles or the azimuth angles in the a priori information into consideration tended to moderate the retrieval difference that resulted from the different viewing directions.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive6.jpg){: style="width: 70%; float: center; margin: 2%"}<br>

<hr/>

### Development of GEO-KOMPSAT-2A Operational Rainfall and QPN Algorithm

The second Korean geostationary satellite (GEO-KOMPSAT-2A) is scheduled for launch in May 2018. Our team leads the operational and research products for clouds and precipitation.

 **An operational rainfall rate (RR) algorithm**

 An operational rainfall rate algorithm has been developed for the Advanced Meteorological Imager (AMI) onboard the GEO-KOMPSAT-2A (GK-2A). The AMI rainfall rate algorithm uses the a-priori information including the microwave rainfall data from the low-earth orbiting satellites and infrared (IR) brightness temperatures from geostationary satellites. The algorithm may better perform with a variety of a-priori information describing all possible precipitating systems. In addition, separation of physically different precipitating systems likely to improve the accuracy of retrieval process. However, it has been well known that such the separation can be hardly achieved based on the measurements of cloud top temperatures. This algorithm tries to utilize the radiative characteristics observed differently for different wavelengths in IR spectral regions. The characteristics include the different emissivity as a function of wavelength and cloud thickness. Using the brightness temperature differences (BTDs) between IR channels the algorithm discriminates three types of precipitating clouds: shallow, not-shallow-tall and not-shallow-taller types. The separation of three types of precipitating clouds may help the accuracy of rainfall estimates for each type of clouds. In addition to the separation of cloud types in the databases, the algorithm also uses databases classified by latitudinal bands. The bands are separated with four latitudinal zones. The separation of database based on latitudes may have an effect of distinguishing the cloud types that can occur regionally. Once the a-priori databases are constructed, the algorithm inverts the AMI IR brightness temperatures to the surface rainfall rate based on a Bayesian approach. The Bayesian approach has advantages on using multi-channel brightness temperatures simultaneously and utilizing the probability of rainfall reserved in the a-priori databases. As a proxy for the AMI this algorithm first tests the Advanced Himawari Imager (AHI) data. Retrieval results and the status and plan of the algorithm development will be introduced.

 **Quantitative Precipitation Nowcasts (QPN) algorithms**

 The AMI QPN products include the potential accumulated rainfall and the probability of rainfall for a 3-h lead time. The potential accumulated rainfall algorithm consists of two major procedures: 1) identification of rainfall features on the outputs from the GEO-KOMPSAT-2A rainfall rate algorithm, and 2) tracking of these rainfall features between two consecutive images. The potential accumulated rainfall algorithm extrapolates precipitation fields every 15 min. Rainfall rates at each time step are accumulated to yield the 3-hourly rainfall. In addition, the extrapolated precipitation fields at 15-min intervals are used as inputs for the probability of rainfall algorithm, which produces the probability of precipitation during the same 3-h period.  The QPN products can be classified as extrapolated features associated with precipitation.<br>

<hr/>

### Radar Operation and Applications

 **Development of a KMA operational merging algorithm for complete radar coverage**

 Our team is currently working for the radar center of KMA. The works include the development of the algorithm to combine radar, satellite and NWP model for precipitation estimation. The algorithm is now being tested for an operational use to produce complete coverage by ground-based radar in case that the coverage is hampered by terrain blockage and beam-related errors.

 This research develops a method merging precipitation estimates from various sensors and models with optimally determined weights. The merging method determines the optimal weights in terms of the relative magnitudes of the root-mean-square errors (RMSE) between the reference sensor observation and the individual precipitation dataset. The merged precipitation fields have been created outside of the ground-based radar observing areas with the interpolated precipitation with the adjacent radar observations, satellite-based precipitation estimates and the short-term forecast model data.  Ongoing works include improving the short-term forecast model based on an optimal estimation with geostationary and LEO satellite data.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/radar1.jpg){: style="width: 60%; float: center; margin: 2%"}<br>
 *Figure 1. Merging procedure for the combining algorithm*

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/radar2.jpg){: style="width: 70%; float: center; margin: 2%"}<br>
 *Figure 2. Precipitation distributions observed by the Jindo radar for four precipitation cases (the first column), same as Fig. 6, but focused on the surrounding of the gap areas (black line box). Precipitation estimations over the black boxes from the three merging experiments employing the optimal weights determined by the original radar data and the AWS data, and equal weights (1/2) are illustrated in the rest of the columns, respectively*

 **Operation of a polarimetric radar**

 A polarimetric X-band radar will be installed by the end of Feb. 2017 at the Science hall of Yonsei University. The radar will be operated in collaboration with KICT (Korea Institute of Civil Engineering and Building Technology).  Our group will first focus on joint works with KICT and Korea University for monitoring flash floods in the high population city, understanding microphysical properties of regional weather systems, and precipitation measurements from mulit-sensors.

<hr/>

### Cloud Microphysics and Satellite Observation

Clouds and precipitation processes in the numerical weather forecasting model have some degree of uncertainty with various microphysics parameterization schemes. Therefore, it is important to apply microphysics schemes in accordance with their characteristics for rainfall retrievals. Using emission and scattering signals from hydrometeors in the precipitation system, the simulated results from numerical models can be evaluated by comparing them after calculating brightness temperatures to the observed data from passive microwave sensors. The research develops a methodology for the comparison of numerical model and satellite observations and used the methodology to understanding, evaluate and improve the microphysics schemes in the cloud resolving models.

![]({{ site.url }}{{ site.baseurl }}/images/respic/microphysics1.jpg){: style="width: 70%; float: center; margin: 2%"}<br>
![]({{ site.url }}{{ site.baseurl }}/images/respic/microphysics2.jpg){: style="width: 70%; float: center; margin: 2%"}<br>

<hr/>

### Utilization of Infrared and Microwave Data for Satellite Data Assimilation

 **Bias correction**

 The satellite data usually have systematic errors and these errors (or biases) can degrade the quality of the analysis field and ultimately forecast field. The observation biases must be corrected before satellite data assimilation. We have studied to improve the bias correction scheme of the Advanced Microwave Sounding Unit-A (AMSU-A), which have operationally applied in Korea Meteorological Administration (KMA).

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/assimilation1.jpg){: style="width: 70%; float: center; margin: 2%"}<br>
 *Figure 1. Examples of scan bias correction (NOAA-19 & MetOP-A)*  
 ![]({{ site.url }}{{ site.baseurl }}/images/respic/assimilation2.jpg){: style="width: 70%; float: center; margin: 2%"}<br>
 *Figure 2. Examples of air mass correction (NOAA-19 & MetOP-A)*   

 **1d-var applications**

 The one-dimensional variational analysis (1D-Var) can determine the most probable atmospheric variables at the specific location given the observation and first-guess of atmosphere. We have performed the 1D-Var analysis to retrieve temperature profiles using the Atmospheric Infrared Sounder (AIRS).

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/assimilation3.jpg){: style="width: 50%; float: center; margin: 2%"}<br>
 *Figure 1. An example of temperature profile retrievals*  

<hr/>

### Water Cycle Balance and Trend

 **Global and regional atmospheric water balance closure problems and trends**

 The atmospheric water cycle is one of most important components of the global water cycle. Large amounts of water vapor that are evaporated from the ocean are transported to the continents through the atmosphere. The transported water vapor is converted into precipitation that provides vital water for living things on Earth. Precipitation and evaporation over the oceans change the sea surface salinity and help to drive the ocean thermohaline circulation. Changes in the phase of water in the atmosphere involve latent heat exchanges. Latent heat released by condensation is one of the major energy sources driving the general circulation of the atmosphere. Knowledge of the atmospheric water cycle is therefore essential in order to manage water resources and to understand the Earth’s weather and climate. Our research uses the column integrated atmospheric water balance over the ocean using various satellite-based and merged datasets and focuses on the closures and climatological trends of the regional unbalances.


### ... and more.
