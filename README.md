# Upsampling-LC-Maps-Using-Machine-Learning
Upsampling already available land cover raster layers using machine learning inside Google Earth Engine platform.

## Scope

## Description

The Copernicus Global Land Service (CGLS) is earmarked as a component of the Land service to operate a multi-purpose service component that provides a series of bio-geophysical products on the status and evolution of land surface at global scale.

The Dynamic Land Cover map at 100 m resolution (CGLS-LC100) is a new product in the portfolio of the CGLS and delivers a global land cover map at 100 m spatial resolution. The CGLS Land Cover product provides a primary land cover scheme. Next to these discrete classes, the product also includes continuous field layers for all basic land cover classes that provide proportional estimates for vegetation/ground cover for the land cover types. This continuous classification scheme may depict areas of heterogeneous land cover better than the standard classification scheme and, as such, can be tailored for application use (e.g. forest monitoring, crop monitoring, biodiversity and conservation, monitoring environment and security in Africa, climate modelling, etc.).

These consistent Land Cover maps (v3.0.1) are provided for the period 2015-2019 over the entire Globe, derived from the PROBA-V 100 m time-series, a database of high quality land cover training sites and several ancillary datasets, reaching an accuracy of 80% at Level1 over al years. It is planned to provide yearly updates from 2020 through the use of a Sentinel time-series.

	NDMI	NDVI	BSI	NDBI
Formula

	(NIR-SWIR)/(NIR+SWIR)	(NIR-RED)/(NIR+RED)	((SWIR+RED)-(NIR+BLUE))/((SWIR+RED)+(NIR+BLUE))	((SWIR-NIR))/((SWIR+NIR))
Landsat 5	(B04-B05)/(B04+B05)
	(B04-B03)/(B04+B03)	((B05+B03)-(B04+B01))/((B05+B03)+(B04+B01))	(B05-B04)/(B05+B04)
Landsat 7	(B04-B05)/(B04+B05)
	(B04-B03)/(B04+B03)	((B05+B03)-(B04+B01))/((B05+B03)+(B04+B01))	(B05-B04)/(B05+B04)
Landsat 8	(B05-B06)/(B05+B06)
	(B05-B04)/(B05+B04)	((B06+B04)-(B05+B02))/((B06+B04)+(B05+B02))	(B06-B05)/(B06+B05)
![image](https://user-images.githubusercontent.com/23013328/233996047-6bf1a59a-fe5b-40f9-9499-8e9df5fd9749.png)


## Steps

## Results

## Bibliography

## Credits
Credits to <a href="https://www.linkedin.com/in/spatialthoughts/"> Ujaval Gandhi</a> and <a href="https://spatialthoughts.com/">SpatialThought</a> team for their excellent tutorials which I used through out this project.
