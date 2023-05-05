# Upsampling-LC-Maps-Using-Machine-Learning
Upsampling already available land cover raster layers using machine learning inside Google Earth Engine platform.

Clone the project by typing:
git clone https://earthengine.googlesource.com/users/fkwstas/unitus/Upsampling_LC_Maps_Sentinel2

## Scope

## Description
The method used is the supervised pixel based multi-class semantic segmentation to upsample already available land cover maps with coarse spatial resolution.  For the current study pre-existing land cover maps were used which were freely available but offered in coarse spatial resolution, thus leading us to adopt an upscaling approach. This term is quite self-explanatory since its goal is to formulate a statistical model which uses as input low resolution datasets and outputs the same data but in a finer resolution. Upscaling methods are superior from simple resampling methods like nearest neighbour while it has also been adopted by several research programs. The result of this method is a raster layer with a pixel size equal to initial image and a color-coded pixel value corresponding to one of the several labels (forest, built-up etc.) The machine learning model that was chosen is called Random Forest already available in most common platforms (Google Earth Engine, Orfeo ToolBox et.c). It is a supervised learning algorithm belonging to a class of classifiers named as ensemble, based on multiple different individual decision trees and each one is trained on a subset of the original data created using the bootstrap method. In practice, random forests tend to perform very well right out of the box and tend to be less prone to overfitting compared to other classifiers like Support Vector Machines.

The ground truth sampels were collected from MODIS Land Cover Type Product (MCD12Q1), which is a land cover map at 500-meter spatial resolution at annual time step for six different land cover legends. The maps are created from classifications of spectro-temporal features derived of data from the Moderate Resolution Imaging Spectroradiometer (MODIS). The MCD12Q1 product supplies global maps of land cover at annual time steps from 2001 until present, making it ideal for our purpose. Among the six different classification themes (legends) it was preferred the IGBP land cover classification. The thematic classes along with the relevant pixel value are listed on the table.

![Screenshot 2023-05-05 at 21 31 11](https://user-images.githubusercontent.com/23013328/236539725-94afc8d6-364f-49bf-9328-3d60e5be6344.png)




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
