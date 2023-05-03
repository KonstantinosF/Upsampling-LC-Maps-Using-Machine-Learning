# Upsampling-LC-Maps-Using-Machine-Learning
Upsampling already available land cover raster layers using machine learning inside Google Earth Engine platform.

Clone the project by typing:
git clone https://earthengine.googlesource.com/users/fkwstas/unitus/Upsampling_LC_Maps_Sentinel2

## Scope

## Description



## Steps
1. Degine the year of interest and draw two polygons; one representing the are where training samples will be extracted and another one which depicts the area we are interested to segment. Name the first area as "geo" and the second area as "geo_small".
2. Prepare the ground truth labels.
3. Interpolate gaps from cloudy pixels and apply smoothing.
4. Build the feature space.
5. Collect Training Data from Global Land Cover Map.
6. Train a Random Forest.
7. Apply the Previously Trained RF on the Image and Produce a Classified Image. Asses the Accuracy.
8. Save the Result on Google Drive.

## Results

![GEE_result](https://user-images.githubusercontent.com/23013328/236033293-51e7f568-1b43-448a-9a7c-dc0584bddb56.png)


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
