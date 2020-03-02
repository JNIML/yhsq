# References of Graphical Report of Australian Fire

[Attributes](https://earthdata.nasa.gov/faq/firms-faq#ed-modis-fire-onground)

- MODIS: Data collected by the satellites utilize an algorithm that exploits the strong emission of mid-infrared radiation from fires and thermal anomalies - these fires and thermal anomalies are shown here as red points. The points represent the center of a pixel within which one or multiple fires have occurred. For the **MODIS instrument the point represents the center of a 1km pixel**, for the VIIRS instrument the point represents the center of a 375m pixel. Using the eye icon, turn on and off the MODIS and VIIRS Day and Night time fire points to view the differences between the sources.

- Scan & Track: The scan value represents the spatial-resolution in the East-West direction of the scan and the track value represents the North-South spatial resolution of the scan. 
  **It should be noted that the pixel size is not always 1km across the scan track**. The pixels at the “Eastern” and the “Western” edges of the scan are bigger than 1km. It is 1km only along the nadir (exact vertical from the satellite). Thus, the values shown for scan and track represent the actual spatial resolution of the scanned pixel.

- Brightness temperature: a measure of the **photons at a particular wavelength** received by the spacecraft, but **presented in units of temperature**.

- Detectable Fires: In any given scene the minimum **detectable fire size is a function of many different variables** (scan angle, biome, sun position, land surface temperature, cloud cover, amount of smoke and wind direction, etc.), so the precise value will vary slightly with these conditions. MODIS routinely **detects both flaming and smoldering fires 1000 m^2 in size**. Under very good observing conditions (e.g. near nadir, little or no smoke, relatively homogeneous land surface, etc.) flaming fires one tenth this size can be detected. Under pristine (and extremely rare) observing conditions even smaller flaming fires 50 m2 can be detected. **It is not recommended to estimate burned area from the active fire data**, Determining this to an acceptable degree of accuracy is generally not possible due to nontrivial spatial and temporal sampling issues. For some applications, however, acceptable accuracy can be achieved, although the effective area burned per fire pixel is not simply a constant, but rather varies with respect to several different vegetation and fire-related variables. See [Giglio et al. (2006)](https://earthdata.nasa.gov/earth-observation-data/near-real-time/firms/about-firms#ed-firms-publications) for more information.

  Unlike most contextual fire detection algorithms designed for satellite sensors that were never intended for fire monitoring (e.g. AVHRR, VIRS, ATSR), there is no upper limit to the largest and/or hottest fire that can be detected with MODIS.

- Confidence: The confidence value was added to help users gauge **the quality of individual fire pixels** is included in the Level 2 fire product. **The confidence field should be used with caution; it is likely that it will vary in meaning in different parts of the world.** Nevertheless some of our end users have found such a field to **be useful in excluding false positive occurrences of fire**. They are different for MODIS and VIIRS.

  For MODIS, the confidence value ranges from 0% and 100% and can be used to assign one of the three fire classes (low-confidence fire, nominal-confidence fire, or high-confidence fire) to all fire pixels within the fire mask. In some applications errors of commission (or false alarms) are particularly undesirable, and **for these applications one might be willing to trade a lower detection rate to gain a lower false alarm rate**. Conversely, for other applications missing any fire might be especially undesirable, and one might then be willing to tolerate a higher false alarm rate to ensure that fewer true fires are missed. Users requiring fewer false alarms may wish to retain only nominal- and high-confidence fire pixels, and treat low-confidence fire pixels as clear, non-fire, land pixels. Users requiring maximum fire detectability who are able to tolerate a higher incidence of false alarms should consider all three classes of fire pixels.
  
  [**MODIS Collection 6 Active Fire Product User’s Guide Revision B**](https://cdn.earthdata.nasa.gov/conduit/upload/10575/MODIS_C6_Fire_User_Guide_B.pdf)
  
  > “Users requiring fewer false alarms may wish to consider only nominal- and high-confidence fire pixels, and treat low-confidence fire pixels as clear, non-fire, land pixels.”
  >
  > **0% ≤ C < 30% low**
  
  

- **Maximum FRP**: **The maximum fire radiative power** of all fire pixels falling within each grid cell is provided on a daily basis in the “MaxFRP” SDS. Here the FRP values have been scaled by a factor of 10 and stored as a 32-bit signed integer. Multiply these scaled values by 0.1 to retrieve the maximum FRP in MW.

  >Our results suggest that MODIS and GOES fire radiative power (FRP) estimates derived for individual fire‐pixel clusters are subject to **errors due to** the effects of the point spread function of those instruments (underestimation of up to 75%), improper fire background characterization (overestimation of up to 80% assuming a 10 K cold bias in background temperature), and omission of small fire lines. **Detection limits were approximately 11 and 9 MW for MOD14 and MYD14, respectively, and were equivalent to 27 and 19 MW for WF_ABBA data acquired coincidently with MOD14 and MYD14, respectively**. We found a positive correlation between FRP and percentage tree cover indicating that FRP is sensitive to biomass density.
  >
  >_______On the use of fire radiative power, area, and temperature estimates to characterize biomass burning via moderate to coarse spatial resolution remote sensing data in the Brazilian Amazon

  > FRP represents the energy emitted by fire through radiative processes (i.e. the total fire intensity minus the energy dissipated through con- vection and conduction) over its total area. It is widely used as a proxy for fire impact assessment (Barrett and Kasis- chke, 2013; Sparks et al., 2018), biomass combustion rates (Roberts et al., 2005) or fire event (Hernandez et al., 2015) and fire spread (Johnson et al., 2017) modelling. 
  >
  > --------Varying relationships between fire radiative power and fire size at a global scale

- Dsfsad