---
title: "ARSL - Research"
layout: textlay
excerpt: "ARSL -- Research"
sitemap: false
permalink: /research/
---

# Research

<div style="margin-top: 30px;"></div>

The following are the main areas we are currently working on:

- [Satellite remote sensing of clouds and precipitation](#remote-sensing)  
- [Microwave radiative modeling through precipitating clouds](#rtm)  
- [Balance and trends of atmospheric water cycle](#water-cycle)  

(Click on each research area to navigate to the respective section)

<a id='remote-sensing'></a>
<div style="margin-top: 30px;"></div>
<hr/>
<div style="margin-top: 30px;"></div>

## Satellite remote sensing of clouds and precipitation

### (1) Passive microwave remote sensing of precipitation

Passive microwave signatures from satellites are based on emission and scattering from the liquid and frozen hydrometeors in the cloud columns. Warm emission signals indicate the presence of liquid water. In contrast, microwave signals at scattering channels with higher frequencies are attenuated by the amount and types of ice particles in the rain column. Our research focuses on the development of rainfall retrieval algorithms and improving retrieval accuracy. We are also working on applying machine learning methods to precipitation-type classification and inversion models. Followings are brief descriptions of the precipitation algorithm and retrieval error studies.

**(1-1) Advancement of the parametric rainfall retrieval algorithm**

The initial version of the parametric rainfall retrieval algorithm was developed for various spaceborne microwave radiometers in [2003 (Shin and Kummerow)](https://doi.org/10.1175/1520-0450(2003)042<1480:PRRAFP>2.0.CO;2). It is based on simultaneous uses of space-borne radar, cloud-resolving, and radiative transfer models for the construction of a-priori information. This fully parametric rainfall retrieval algorithm is designed to be applicable to a wide variety of passive microwave sensors that currently exist and are planned for the future. The algorithm is continuously being improved by including radiative transfer simulations that are physically consistent with the cloud microphysics used in cloud models: [Kim et al. (2013)](https://doi.org/10.1175/JTECH-D-12-00261.1) and [Choi et al. (2019)](https://doi.org/10.1109/TGRS.2019.2948262).

<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/passive1.jpg" style="width: 80%; margin: 2%;">
</div>

**(1-2) Retrieval error analysis**

There are many sources of error in passive microwave rainfall estimation. Errors can be related to rainfall inhomogeneity within a large footprint (so-called beam-filling error), rain-column height, excessive emission from melting ice (bright-band effect), three-dimensional radiative effects of the precipitating system, forward model assumptions, and so on. These uncertainties can also be observed differently for different precipitation types and climate regimes. A better understanding of the uncertainties is important for better rainfall algorithms.

As an example, the following figure shows the effect of three-dimensional radiative effects of the precipitating system in rainfall measurements [(Kim et al., 2016)](https://doi.org/10.1109/TGRS.2015.2490743). Vertically and horizontally inhomogeneous distributions of hydrometeors are often observed in precipitating clouds. The three-dimensional characteristics can then cause errors in the passive microwave rainfall measurements within the current off-nadir viewing sensors' specifications. It was found that taking more viewing angles or the azimuth angles in the a-priori information into consideration tended to moderate the retrieval difference that resulted from the different viewing directions.

<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/3deffect.JPG" style="width: 80%; margin: 2%;">
</div>

### (2) Cloud and precipitation measurements from infrared observations

Visible and infrared observations from satellites are used to detect the optical properties of clouds and precipitation. We are working on developing precipitation and cloud phase algorithms based on physical, statistical, and machine-learning methods. Here are several examples of our team's work with infrared satellite data.

 **(2-1) An operational rainfall rate algorithm for GEO-KOMPSAT-2A satellite**

Geostationary satellites have the advantage of continuously observing weather systems with a spatial resolution of less than a few kilometers over about one-third of the Earth's surface. An operational rainfall rate algorithm has been developed for the Advanced Meteorological Imager (AMI) onboard the second Korean geostationary satellite, GEO-KOMPSAT-2A (GK-2A). The AMI rainfall rate algorithm uses the a-priori information including the microwave rainfall data from the low-earth orbiting satellites and infrared (IR) brightness temperatures from geostationary satellites. The algorithm may better perform with a variety of a-priori information describing all possible precipitating systems. In addition, the separation of physically different precipitating systems is likely to improve the accuracy of the retrieval process. However, it has been well known that such a separation can be hardly achieved based on the measurements of cloud top temperatures. This algorithm tries to utilize the radiative characteristics observed differently for different wavelengths in IR spectral regions. The characteristics include the different emissivity as a function of wavelength and cloud thickness. Using the brightness temperature differences (BTDs) between IR channels the algorithm discriminates five types of precipitating clouds: non-shallow-tall-cold, non-shallow-tall-colder, non-shallow-taller-cold, and non-shallow-taller-colder clouds. The separation of five types of precipitating clouds may help the accuracy of rainfall estimates for each type of cloud [(So and Shin, 2018)](https://doi.org/10.1002/qj.3288). In addition to the separation of cloud types in the databases, the algorithm also uses databases classified by latitudinal bands. The bands are separated into four latitudinal zones. The separation of databases based on latitudes may affect distinguishing the cloud types that can occur regionally. Once the a-priori databases are constructed, the algorithm inverts the AMI IR brightness temperatures to the surface rainfall rate based on a Bayesian approach. The Bayesian approach has the advantages of using multi-channel brightness temperatures simultaneously and utilizing the probability of rainfall reserved in the a-priori databases.  

<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/gk-2a_rr.JPG" style="width: 80%; margin: 2%;">
</div>

(These images and data are provided by the National Meteorological Satellite Center (NMSC). For more details, visit [NMSC Satellite Viewer](https://nmsc.kma.go.kr/enhome/html/satellite/viewer/selectSatViewerEnhome.do?dataType=gk2a).)

**(2-2) Quantitative Precipitating Nowcasts (QPN) algorithms GK-2A satellite**

The AMI QPN products include the potential accumulated rainfall and the probability of rainfall for a 3-h lead time. The potential accumulated rainfall algorithm consists of two major procedures: 1) identification of rainfall features on the outputs from the GK-2A rainfall rate algorithm, and 2) tracking of these rainfall features between two consecutive images. The potential accumulated rainfall algorithm extrapolates precipitating fields every 15 min. Rainfall rates at each time step are accumulated to yield the 3-hour rainfall. In addition, the extrapolated precipitation fields at 15-minute intervals are used as inputs for the probability of rainfall algorithm, which produces the probability of precipitation during the same 3-h period. The QPN products can be classified as extrapolated features associated with precipitation [(Hong et al., 2016)](https://doi.org/10.1109/TGRS.2016.2596293).

**(2-3) Measuring cloud phase based on machine learning approach**

Cloud thermodynamic phases include water, ice, and mixtures of the two, which play a significant role in the Earth's radiation budget due to their influence on the optical properties of clouds. A cloud phase algorithm based on an unsupervised machine learning technique with Gaussian Mixture Models (GMMs) has been developed. The GMM-based algorithm uses the brightness temperature (TB) of 11.2 (&#181;m) and the brightness temperature difference (BTD) of 8.6 and 11.2 (&#181;m) are applied to classify three different cloud phases including water, ice, and undetermined phases.

The water and ice phases estimated using the GMM-based algorithm are in good agreement with both the MODIS and CALIOP products. The GMM-based algorithm also significantly reduces the misidentified area for undetermined phases observed in the GK2A operational product. Water and ice phases are also effectively estimated in warm regions, resulting in distributions similar to those derived from MODIS and CALIOP products. Unlike most IR cloud-phase algorithms that utilize thresholds and other cloud parameters, the GMM-based cloud-phase algorithm has the advantage of using only TB, thus avoiding auxiliary cloud properties. The following figure compares GMM-based cloud phases to other products. More details can be found in [Kim and Shin (2024)](https://doi.org/10.1109/TGRS.2024.3383888).

<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/GMM-cloudphase.jpg" style="width: 70%; margin: 2%;">
</div>

<a id='rtm'></a>
<div style="margin-top: 30px;"></div>
<hr/>
<div style="margin-top: 30px;"></div>

## Microwave radiative modeling through precipitating clouds

Microwave emission and scattering signatures through precipitating clouds depend on the characteristics of hydrometeors. Clouds of hydrometeors act as volume scatterers and emitters. The individual optical properties of hydrometeors and their size distributions in volume are important in modeling microwave emission and scattering. In particular, scattering by ice particles is one of the most uncertain components in microwave radiative transfer modeling. This is because ice particles can have different shapes, densities, orientations, and particle size distributions (PSDs). Followings are brief descriptions of the passive microwave microwave radiative transfer simulations considering non-spherical and inhomogeneous hydrometeors.

**(1) Modeling microwave scattering from non-sphere and inhomogeneous ice particles**

PSDs of hydrometeors are usually assumed through a bulk parameterization approach based on various distribution functions like exponential and modified Gamma distribution functions. We are working on developing methods to incorporating non-spherical ice particles and various microphysical properties of hydrometeors into radiative transfer modeling for more accurate scattering signals. The following figures demonstrate the effects of spherical/non-spherical assumptions and different PSDs in simulating scattering signals at the high-frequency channels of GMI.

<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/rtm-microphysics.JPG" style="width: 77%; margin: 2%;">
</div>
<div style="text-align: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/rtm-nonspherical.JPG" style="width: 83%; margin: 2%;">
</div>

**(2) Incorporation of various cloud microphysics schemes into microwave radiative transfer models for physically consistent radiative simulations for all weather data assimilation**

Microwave data are important for all weather data assimilation. Microwave radiative transfer models for data assimilation need to adopt the properties of hydrometeors used in numerical weather prediction models. One of the key assumptions about the properties of hydrometeors is in cloud microphysics schemes. We are working to develop methods to effectively incorporate cloud microphysics schemes into radiative transfer models used for data assimilation.

[image?]

**(3) Retrievals of the microphysical properties of ice particles based on cloud models and scattering modeling**

We are developing ice particle retrieval algorithms for high frequencies in a variety of passive and active microwave sensors based on more accurate scattering simulations that consider non-spherical and inhomogeneous ice particles. Retrieval methods include numerical model simulations, deep-learning approaches, etc.

<a id='water-cycle'></a>
<div style="margin-top: 30px;"></div>
<hr/>
<div style="margin-top: 30px;"></div>

## Balance and trends of the atmospheric water cycle

Our research explores the balance of the atmospheric water cycle and examines trends in regional imbalances. This includes comprehensive studies of how water vapor is transported through the atmosphere, how precipitation patterns change over time, and how these changes affect different regions. Understanding these trends is critical for predicting future climate scenarios and mitigating the impacts of regional water imbalances on ecosystems and human activities.

**Global and regional atmospheric water balance closure problems and trends**

The atmospheric water cycle is one of the most important components of the global water cycle. Large amounts of water vapor that are evaporated from the ocean are transported to the continents through the atmosphere. The transported water vapor is converted into precipitating which provides vital water for living things on Earth. Precipitation and evaporation over the oceans change the sea surface salinity and help to drive the ocean thermohaline circulation. Changes in the phase of water in the atmosphere involve latent heat exchanges. Latent heat released by condensation is one of the major energy sources driving the general circulation of the atmosphere. Knowledge of the atmospheric water cycle is therefore essential in order to manage water resources and to understand the Earth's weather and climate. Our research uses the column-integrated atmospheric water balance over the ocean using various satellite-based and merged datasets and focuses on the closures and climatological trends of the regional unbalanced. 

<br>

