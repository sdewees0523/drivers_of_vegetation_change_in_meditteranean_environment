# drivers_of_vegetation_change_in_meditteranean_environment
Data and code used for the data processing and analysis published in "Determining potential drivers of vegetation change in a meditteranean environment". 

Authors: Shane Dewees, Carla D'Antonio, and Nicole Molinari

#### Data descriptions

##### vegetation_classifications
*plots.shp*: Shapefile containing the randomly generated 30m radius plots used for vegetation classifications and analysis.
  * *FID*: Unique id for each feature in this layer. Was also used as the identifying plot number in data preparation code. 
  * *Shape*: Feature class for each feature in this layer. As this layer consists of all the plots, all values are Polygon. 
  * *BUFF_DIST*: Radius in meters of each feature. 

*plot_points.shp*: Shapefile containing the 50 randomly generated points per plot and the associated vegetation type that each point falls in.   
  * *FID*: Unique id for each feature in this layer. 
  * *Shape*: Feature class for each feature in this layer. As this layer consists of the randomly generated points, all values are Point.  
  * *CID*: Identifying value to match the points to the plot they were generated in. Is identical to the *FID* value in *plots.shp*. 
  * *F1930_Veg*: Vegetation group of the pixel that the point falls in for 1930 imagery. Possible values are:
      * t = tree
      * g = grass
      * s = sage scrub
      * c = chaparral
      * b = barren
  
  * *F2009_Veg*: Vegetation group of the pixel that the point falls in for 2009 imagery. Possible values are:
     * t = tree
     * g = grass
     * s = sage_scrub
     * c = chaparral
     * b = barren

##### csv_data
*plots_percent_cover_tidy*: Percent cover and vegetation data formatted for easy graphing of percent cover data. 
  * *plot_number*: Identifying number to the corresponding plot from the *plots.shp* shapefile. 
  * *dominant_veg_1930*: Primary vegetation (defined as the vegetation group with the most random points associated to it) type of that plot in 1930. Possible values are tree, grass, chaparral, sage, mixed, or barren. 
  * *secondary_veg_1930*: Secondary vegetation type of that plot in 1930. Possible values are tree, grass, chaparral, sage, mixed, or barren. 
  * *dominant_cover_1930*: Percent cover of the primary vegetation type of that plot in 1930(calculated as the number of points identified to that vegetation type multiplied by 2).
  * *secondary_cover_1930*: Percent cover of the secondary vegetation type of that plot in 1930. 
  * *dominant_veg_2009*: Primary vegetation type of that plot in 2009. Possible values are tree, grass, chaparral, sage, mixed, or barren. 
  * *secondary_veg_2009*: Secondary vegetation type of that plot in 2009. Possible values are tree, grass, chaparral, sage, mixed, or barren. 
  * *dominant_cover_2009*: Percent cover of the primary vegetation type of that plot in 2009. 
  * *secondary_cover_2009*: Percent cover of the secondary vegetation type of that plot in 2009.    

*plots_percent_cover*: counts of vegetation type per plot formatted for graphing vegetation distributions in all plots. 
  * *plot_number*: Identifying number to the corresponding plot from the "plots.shp* shapefile.
  * *grass_1930*: Number of points identified as grass in that plot in 1930. 
  * *tree_1930*: Number of points identified as tree in that plot in 1930. 
  * *chaparral_1930*: Number of points identified as chaparral in that plot in 1930.
  * *sage_1930*: Number of points identified as sage scrub in that plot in 1930. 
  * *barren_1930*: Number of points identified as barren in that plot in 1930. 
  * *dom_veg_1930*: The number of points identified to the vegetation group with the most points in that plot in 1930. 
  * *sec_veg_1930*: The number of points identified to the vegetation group with the second most points in that plot in 1930. 
  * *dominant_cover_1930*: The percent cover of the primary vegetation group for that plot in 1930. 
  * *secondary_cover_1930*: The percent cover of the secondary vegetation group for that plot in 1930. 
  * *dominant_veg_1930*: The primary vegetation type in that plot in 1930. 
  * *secondary_veg_1930*: The secondary vegetation type in that plot in 1930.
  * *grass_2009*: Number of points identified as grass in that plot in 2009. 
  * *tree_2009*: Number of points identified as tree in that plot in 2009. 
  * *chaparral_2009*: Number of points identified as chaparral in that plot in 2009.
  * *sage_2009*: Number of points identified as sage scrub in that plot in 2009. 
  * *barren_2009*: Number of points identified as barren in that plot in 2009. 
  * *dom_veg_2009*: The number of points identified to the vegetation group with the most points in that plot in 2009. 
  * *sec_veg_2009*: The number of points identified to the vegetation group with the second most points in that plot in 2009. 
  * *dominant_cover_2009*: The percent cover of the primary vegetation group for that plot in 2009. 
  * *secondary_cover_2009*: The percent cover of the secondary vegetation group for that plot in 2009. 
  * *dominant_veg_2009*: The primary vegetation type in that plot in 2009. 
  * *secondary_veg_2009*: The secondary vegetation type in that plot in 2009. 

*veg_enviro_fire_drought*: Processed data including the vegetation cover data and all independent variables for each plot. Ready for use in the analysis code titled *manuscript*. 
  * *plot_number*: Identifying number to the corresponding plot from the "plots.shp* shapefile. 
  * *dominant_veg_1930*: Primary vegetation type of that plot in 1930. Possible values are tree, grass, chaparral, sage scrub, mixed, or barren. 
  * *secondary_veg_1930*: Secondary vegetation type of that plot in 1930. Possible values are tree, grass, chaparral, sage scrub, mixed, or barren. 
  * *dominant_cover_1930*: Percent cover of the primary vegetation type of that plot in 1930. 
  * *secondary_cover_1930*: Percent cover of the secondary vegetation type of that plot in 1930.
  * *dominant_veg_2009*: Primary vegetation type of that plot in 2009. Possible values are tree, grass, chaparral, sage scrub, mixed, or barren. 
  * *secondary_veg_2009*: Secondary vegetation type of that plot in 2009. Possible values are tree, grass, chaparral, sage scrub, mixed, or barren. 
  * *dominant_cover_2009*: Percent cover of the primary vegetation type of that plot in 2009. 
  * *secondary_cover_2009*: Percent cover of the secondary vegetation type of that plot in 2009. 
  * *elevation*: Mean elevation of all 50 points randomly generated in that plot. Units of meter. 
  * *aspect*: Mean southwestness value of all 50 points randomly generated in that plot. Values range from -1 to 1. 
  * *slope*: Mean slope of all 50 points randomly generated in that plot. Units of degrees. 
  * *solar_radiation_summer*: Mean summer solar radiation of all 50 points randomly generated in that plot. Units of watt hours per square meter. 
  * *solar_radiation_equinox*: Mean spring solar radiation of all 50 points randomly generated in that plot. Units of watt hours per square meter. 
  * *solar_radiation_winter*: Mean winter solar radiation of all 50 points randomly generated in that plot. Units of watt hours per square meter. 
  * *road_dist*: Mean distance to closest road of all 50 points randomly generated in that plot. Units of meter.
  * *precipitation*: Mean annual precipitation normal of all 50 points randomly generated in that plot. Units of millimeter per year. 
  * *max_temp*: Mean maximum August temperature normal of all 50 points randomly generated in that plot. Units of Celsius. 
  * *mean_temp*: Mean average annual temperature normal of all 50 points randomly generated in that plot. Units of Celsius. 
  * *min_temp*: Mean minimum January temperature normal of all 50 points randomly generated in that plot. Units of Celsius. 
  * *max_vpd_jan*: Mean maximum January vapor pressure deficit normal of all 50 points randomly generated in that plot. Units of hectopascal. 
  * *max_vpd_aug*: Mean maximum August vapor pressure deficit normal of all 50 points randomly generated in that plot. Units of hectopascal. 
  * *available_water_supply*: Mean available water supply of soil down to 150cm of all 50 points randomly generated in that plot. Units of centimeter cubed. 
  * *bulk_density*: Mean bulk density of soil down to 150cm of all 50 points randomly generated in that plot. Units of gram per centimeter cubed. 
  * *organic_matter*: Mean organic matter of soil down to 150cm of all 50 points randomly generated in that plot. Units of percent. 
  * *clay*: Mean percent clay content of soil down to 150cm of all 50 points randomly generated in that plot. Units of percent. 
  * *sand*: Mean percent sand content of soil down to 150cm of all 50 points randomly generated in that plot. Units of percent. 
  * *silt*: Mean percent silt content of soil down to 150cm of all 50 points randomly generated in that plot. Units of percent. 
  * *number_fires*: The number of fires that burned through a plot between 1912 and 2003. 
  * *min_return_interval*: The smallest fire free interval of a plot between 1912 and 2003. For plots that only burned once, value was set to 86. Units of years.
  * *min_anomaly*: The minimum post-fire (calculated for just the year of fire) annual precipitation anomaly (calculated as annual precipitation minus annual precipitation normal) for that plot. Units of millimeter per year. 

*veg_enviro_fire_drought_1* through *veg_enviro_fire_drought_5*: Identical metadata as for above *veg_enviro_fire_drought* file. The only difference is the *min_anomaly* column is calculated with the annual precipitation data for the year of fire and number of years after fire corresponding to the number at the end of the file name. For example, *veg_enviro_fire_drought_2* was calculated for the year of fire and two years following the fire. 

*rmse*: Random forest accuracy values for different postfire precipitation anomaly calculations provided in Appendix S2.
    * *Precipitation anomaly variable*: How many years postfire were used to calculate the given postfire precipitation anomaly variable.
    * *Root mean square error*: The random forest model accuracy for each precipitation anomaly variable from the chaparral cover change dataset. 
    * *Kappa*: The random forest model accuracy for each precipitation anomaly variable from the chaparral conersion to grass dataset. 

*cover_correlation*: Correlation matrix provided in Appendix S6 showing the Pearsons' correlation coefficient for eahc set of variables on the chaparral cover change dataset. Both column and row names are variables. 

*chaparral_cover_short*: Correlation matrix provided in Appendix S6 showing the Pearsons' correlation coefficient for eahc set of variables on the chaparral cover change dataset subset to only include minimum fire return intervals less than 81 years. Both column and row names are variables. 

*chaparral_cover_long*: Correlation matrix provided in Appendix S6 showing the Pearsons' correlation coefficient for eahc set of variables on the chaparral cover change dataset subset to only include minimum fire return intervals greater than or equal to 81 years. Both column and row names are variables. 

*conversion_correlation*: Correlation matrix provided in Appendix S6 showing the Pearson's correlation coefficient for each set of variables on the chaparral conversion to grass dataset. Both column and row names are variables.

*chaparral_conversion_short*: Correlation matrix provided in Appendix S6 showing the Pearson's correlation coefficient for each set of variables on the chaparral conversion to grass dataset subset to only include minimum fire return intervals less than 81 years. Both column and row names are variables.

*chaparral_conversion_long*: Correlation matrix provided in Appendix S6 showing the Pearson's correlation coefficient for each set of variables on the chaparral conversion to grass dataset subset to only include minimum fire return intervals greater than or equal to 81 years. Both column and row names are variables. 

**The following data is all obtained from external sources, with websites and querry specifics described in detail in Appendix S8 of the associated manuscript and also included in this repository for convenience. What follows are very brief descriptions of the data in each folder**

##### Aspect 
Aspect raster used to calculate southwestness. 

##### Elevation
Elevation raster obtained from USGS and used for elevation variable and to calculate aspect, slope, and solar insolation. 

##### fire_perimeters
Historic fire perimeters obtained from CALFIRE FRAP and used to create number of fires, minimum fire return interval, and postfire precipitation anomaly variables. 

##### precip_anomalies
Precipitation anomalies calculated for all years from 1912-2009 and used to create the postfire precipitation anomaly variables. Calculated from PRISM climate data outlined in Appendix S8 and not provided here. The number at the end of each file name corresponds to the year it was calculated for. For example, *anom_1913* was calculated for the year 1913. 

##### PRISM_DATA
Climate normals obtained from PRISM and used in analysis. 
  * ppt = precipitation
  * tmax = maximum August temperature
  * tmean = mean annual temperature
  * tmin = minimum January temperature
  * vpdmax_..._01 = maximimum January vapor pressure deficit. 
  * vpdmax_..._08 = maximum August vapor pressure deficit. 

##### Road_dist
Minimum distance to roads raster used for the distance from roads variable. 

##### Slope
Slope raster used for the slope variable. 

##### soil
Shape files obtained from SSURGO and used for their corresponding soil variables. This process is detailed extensively in Appendix S8

##### Solar Insolation
Winter, spring (equinox) and summer solar radiation rasters used for solar radiation variables. 

#### Code descriptions

###### data_preperation.rmd
This code takes all the raw data (plot_points.shp and all the above climate, topographic, and fire data) and cleans them, combines them and makes the veg_enviro_fire_drought csv files and plots_percent_cover and plots_percent_cover_tidy csv files for use in the other three rmarkdown files. 

###### random forest.rmd
This code takes all six of the veg_enviro_fire_drought csv files and runs random forest models to asses which method of calculating the minimum postfire precipitation anomaly leads to the most accurate predictive models. The data obtained from this code is used to make the rmse csv file and Appendix S2.

###### data exploration.rmd
This code takes the veg_enviro_fire_drought_4 csv file and checks all of the independent variables for normal or non-normal distribution. 

###### manuscript.rmd
This code takes the veg_enviro_fire_drought_4, plot_percent_cover, and plots_percent_cover_tidy csv files and performs all of the analyses discussed in the associated manuscript and creates all of the figures (excluding figure 1) as well. 
