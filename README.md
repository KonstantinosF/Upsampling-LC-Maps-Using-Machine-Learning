# Upsampling-LC-Maps-Using-Machine-Learning
Upsampling already available land cover raster layers using machine learning inside Google Earth Engine platform.

## Scope

## Description

The Copernicus Global Land Service (CGLS) is earmarked as a component of the Land service to operate a multi-purpose service component that provides a series of bio-geophysical products on the status and evolution of land surface at global scale.

The Dynamic Land Cover map at 100 m resolution (CGLS-LC100) is a new product in the portfolio of the CGLS and delivers a global land cover map at 100 m spatial resolution. The CGLS Land Cover product provides a primary land cover scheme. Next to these discrete classes, the product also includes continuous field layers for all basic land cover classes that provide proportional estimates for vegetation/ground cover for the land cover types. This continuous classification scheme may depict areas of heterogeneous land cover better than the standard classification scheme and, as such, can be tailored for application use (e.g. forest monitoring, crop monitoring, biodiversity and conservation, monitoring environment and security in Africa, climate modelling, etc.).

These consistent Land Cover maps (v3.0.1) are provided for the period 2015-2019 over the entire Globe, derived from the PROBA-V 100 m time-series, a database of high quality land cover training sites and several ancillary datasets, reaching an accuracy of 80% at Level1 over al years. It is planned to provide yearly updates from 2020 through the use of a Sentinel time-series.

![image](https://user-images.githubusercontent.com/23013328/233996047-6bf1a59a-fe5b-40f9-9499-8e9df5fd9749.png)


## Steps
1. Degine the year of interest and draw two polygons; one representing the are where training samples will be extracted and another one which depicts the area we are interested to segment.
2. PREPARE THE GROUND TRUTH LABELS
3. INTEROPOLATE GAPS FROM CLOUDY PIXELS and APLLY SMOOTHING
4. BUILD THE FEATURE SPACE 
5. Collect Training Data from Global Land Cover Map
6. Train a Random Forest 
7. Apply the Previously Trained RF on the Image and Produce a Classified Image. Asses the Accuracy
8. Save the Result on Google Drive

## Results

## Known Limitations

1. If the geographic area used for collecting training samples is larger than 90 square Km. then GEE will return an issue with reprojection.
2. If the geographic area that we want to semanticly segment should be smaller than the area we use to collect training samples.

## Bibliography

Buchhorn, M.; Smets, B.;Bertels, L.; De Roo, B.;Lesiv, M.; Tsendbazar, N.E., Linlin, L.,
Tarko, A.(2020): Copernicus Global Land Service: Land Cover 100m: Version 3Globe
2015-2019: Product User Manual; Zenodo, Geneve, Switzerland, September 2020;
doi:10.5281/zenodo.3938963.


## Credits
Credits to <a href="https://www.linkedin.com/in/spatialthoughts/"> Ujaval Gandhi</a> and <a href="https://spatialthoughts.com/">SpatialThought</a> team for their excellent tutorials which I used through out this project.
