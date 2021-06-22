---
title: "ARSL - Research"
layout: textlay
excerpt: "ARSL -- Research"
sitemap: false
permalink: /research/
---

# Research

Here are some themes and techniques that we currently work on:

[Passive microwave Remote Sensing of Precipitation](#Passive)
[Development of GEO-KOMPSAT-2A Operational Rainfall and QPN Algorithm](#GK2A)

### Passive Microwave Remote Sensing of Precipitation

Passive microwave signatures from satellites are based on emission and scattering from the liquid and frozen hydrometeors in the cloud columns. Warm emission signals indicate the presence of liquid water and microwave signals at scattering channels with higher frequencies are depressed with the amount and types of ice particles above the rain columns. Our researches focus on the developments of rainfall retrieval algorithms and improving the retrieval accuracy.

 **Development of a rainfall retrieval algorithm based a parametric approach**

 This methodology is based on simultaneous uses of space-borne radar, cloud resolving models and radiative transfer models for construction of a-priori information. This fully parametric rainfall retrieval algorithm is designed for applications to a variety of passive microwave sensors that exist today and are planned for the future.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive1.jpg){: style="width: 70%; float: center; margin: 20px"}

 **Retrieval algorithm for monthly oceanic rainfall**

 With the accumulated satellite datasets for decades, it is possible that satellite-based data could contribute to sustained climate applications. Level-3 products from microwave sensors for climate applications can be obtained from several algorithms. For examples, the Microwave Emission brightness Temperature Histogram (METH) algorithm produces level-3 rainfalls directly, whereas the TRMM/GPM level-2 algorithms first generates instantaneous rainfalls and then temporal and spatial averaging process leads to level-3 products. The rainfall algorithm developed in this study follows a similar approach to averaging instantaneous rainfalls. However, the algorithm is designed to produce instantaneous rainfalls at an optimal resolution showing reduced non-linearity in brightness temperature (TB)-rain rate(R) relations. It is found that the resolution tends to effectively utilize emission channels whose footprints are relatively larger than those of scattering channels.

 This algorithm is mainly composed of a-priori databases (DBs) and a Bayesian inversion module. The DB contains massive pairs of simulated microwave TBs and rain rates, obtained by cloud and radiative transfer simulations. To improve the accuracy and efficiency of retrieval process, data mining technique is additionally considered. The entire DB is classified into eight types based on Koppen climate classification criteria using reanalysis data. Among these sub-DBs, only one sub-DB that presents the most similar physical characteristics is selected by considering the thermodynamics of input data. When the Bayesian inversion is applied to the selected DB, instantaneous rain rate with 6 hours interval is retrieved.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive3.jpg){: style="width: 45%; float: left; margin: 1%"}
 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive4.jpg){: style="width: 45%; float: right; margin: 1%"}<br>

 &nbsp;  

 **Retrieval error reduction**

 Vertically and horizontally inhomogeneous distributions of hydrometeors are often observed in precipitating clouds. The 3-D characteristics can then cause errors in the passive microwave rainfall measurements with the current off-nadir viewing sensors’ specifications. It was found that taking more viewing angles or the azimuth angles in the a priori information into consideration tended to moderate the retrieval difference that resulted from the different viewing directions.

 ![]({{ site.url }}{{ site.baseurl }}/images/respic/passive6.jpg){: style="width: 70%; float: center; margin: 20px"}<br>


### Development of GEO-KOMPSAT-2A Operational Rainfall and QPN Algorithm

The second Korean geostationary satellite (GEO-KOMPSAT-2A) is scheduled for launch in May 2018. Our team leads the operational and research products for clouds and precipitation.

 **An operational rainfall rate (RR) algorithm**

 An operational rainfall rate algorithm has been developed for the Advanced Meteorological Imager (AMI) onboard the GEO-KOMPSAT-2A (GK-2A). The AMI rainfall rate algorithm uses the a-priori information including the microwave rainfall data from the low-earth orbiting satellites and infrared (IR) brightness temperatures from geostationary satellites. The algorithm may better perform with a variety of a-priori information describing all possible precipitating systems. In addition, separation of physically different precipitating systems likely to improve the accuracy of retrieval process. However, it has been well known that such the separation can be hardly achieved based on the measurements of cloud top temperatures. This algorithm tries to utilize the radiative characteristics observed differently for different wavelengths in IR spectral regions. The characteristics include the different emissivity as a function of wavelength and cloud thickness. Using the brightness temperature differences (BTDs) between IR channels the algorithm discriminates three types of precipitating clouds: shallow, not-shallow-tall and not-shallow-taller types. The separation of three types of precipitating clouds may help the accuracy of rainfall estimates for each type of clouds. In addition to the separation of cloud types in the databases, the algorithm also uses databases classified by latitudinal bands. The bands are separated with four latitudinal zones. The separation of database based on latitudes may have an effect of distinguishing the cloud types that can occur regionally. Once the a-priori databases are constructed, the algorithm inverts the AMI IR brightness temperatures to the surface rainfall rate based on a Bayesian approach. The Bayesian approach has advantages on using multi-channel brightness temperatures simultaneously and utilizing the probability of rainfall reserved in the a-priori databases. As a proxy for the AMI this algorithm first tests the Advanced Himawari Imager (AHI) data. Retrieval results and the status and plan of the algorithm development will be introduced.

 **Quantitative Precipitation Nowcasts (QPN) algorithms**

 The AMI QPN products include the potential accumulated rainfall and the probability of rainfall for a 3-h lead time. The potential accumulated rainfall algorithm consists of two major procedures: 1) identification of rainfall features on the outputs from the GEO-KOMPSAT-2A rainfall rate algorithm, and 2) tracking of these rainfall features between two consecutive images. The potential accumulated rainfall algorithm extrapolates precipitation fields every 15 min. Rainfall rates at each time step are accumulated to yield the 3-hourly rainfall. In addition, the extrapolated precipitation fields at 15-min intervals are used as inputs for the probability of rainfall algorithm, which produces the probability of precipitation during the same 3-h period.  The QPN products can be classified as extrapolated features associated with precipitation.


**Scanning tunneling noise spectroscopy (STNS).** We have developed a novel cryogenic MHz amplifier that allows us to measure not only the average tunneling current, but also its fluctuation! This has many applications: one can detect the fluctuations of the electronic states, peculiar tunneling processes, and shot noise. We have used this instrument to discover charge trapping in the insulating layer of the cuprates, connected to the c-axis mystery, and to measure the doubling of the charge due to Andreev processes to the superfluid in a lead sample.


**Mott physics and high-temperature superconductivity.** Questions of interest include: (i), How does the Mott state collapse upon doping and how is this related to the complex phase diagram of high-temperature superconductors? (ii), What is the strange metal phase seen in correlated electron systems? Is this an exotic long-range entangled state? What is the mechanism of dissipation in that state? (iii), Why is the transition temperature in high-temperature superconductors so high? We have worked on iridates, rhodates, and cuprates.

**Nanofabricated "Smart Tips"**.
![]({{ site.url }}{{ site.baseurl }}/images/respic/SmartTip.png){: style="width: 250px; float: left; margin: 0px  10px"}
One of the  projects back from my job-proposal is to develop nanofabricated STM tips. The idea behind these “smart tips” is to use the technologies that were developed over decades in nanofabrication and make them available for scanning probe by using a nano-device instead of the traditional STM tungsten tip. One gains the flexibility of using different functionalities that are known from the fields of nanofabrication and mesoscopic physics. We are collaborating with the group Simon Groeblacher at TU Delft to realize this concept, benefitting from their unparalleled micro/nano fabrication know how.  A prototype of a smart tip is shown to the left. See publications in Microsyst Nanoeng, Nanotechnology, and PRB.

**Josephson STM.** Josephson STM has the ability to gain insight into spatial variations of the order parameter, or superfluid density. We have managed to, for the first time, use JSTM with atomic resolution on a quantum material.
We have used atomic-resolution Josephson scanning tunneling microscopy to reveal a strongly inhomogeneous superfluid in the iron-based superconductor FeTe0.55Se0.45. The results and their implications are published in Nature.

We also detected and investigated a quite particular YSR state in the same material.

**Ultra-stable SI-STM instrument.**  ![]({{ site.url }}{{ site.baseurl }}/images/respic/STMHead.png){: style="width: 250px; float: right; margin: 0px 10px"}
For SI-STM, having the most stable STM head is key. We have used finite element simulations, good choices in material science, and craftsmanship to build the most stable STM head in the world, to our knowledge. See publication in RSI.


**Strange Metals.** The strange metal phase might be the most mysterious phase of high-temperature superconductors. Here, the electrical resistivity grows linearly with temperature T in large areas of the phase diagram, with a mean free path that diminishes to a fraction of the interatomic distance. T-linear resistivity is often associated with quantum critical points and marginal-Fermi-liquid physics. In strange metals, the mystery seems to go even further: we deal with something that looks like a quantum critical phase over an extended range of the phase diagram instead of cumulating in a point. There exists no consistent theory for strange metals, leading to more adventurous new approaches including the holographic theories that use insights from quantum gravity to explain strange metals (a recent textbook on this was written by our colleagues at Leiden University, Schalm and Zaanen).
We are part of the 'Strange Metal consortium NL' that includes the groups of Hussey, Golden, van Heumen, Zaanen, Schalm, Stoof and Vandoren. 

**Magnetic fluctuations and electron spin resonance.**
![]({{ site.url }}{{ site.baseurl }}/images/respic/SpinFluc.png){: style="width: 70%; float: center; margin: 10px"}

**Twisted bilayer graphene and other material with super-periodicities.**
We have proposed that artificial super-periodicities can lead to improved superconductivity, both because of increased density of states and because of phase space arguments (see image from our SciPost publication below). Perhaps for different reasons, twisted bilayer graphene has been shown to superconduct! We are investigate this material with the groups of Efetov, Baumberger, and van der Molen.

![]({{ site.url }}{{ site.baseurl }}/images/respic/SciPost.png){: style="width: 70%; float: center; margin: 0px"}

### ... and more.
