This code (second version with the necessary corrections applied) aims to process satellite images from different sensors and calculate different burn severity indices for fires which burned from 1984 to 2022 in Portugal. 
Based on the year in which the fires burned and the availability of satellite imagery, different sensors have been used: 
    for fires which burned from 1984 to 2001 and 2003 to 2011: satellite images from LANDSAT 5 - dataset in GEE: 'LANDSAT/LT05/C02/T1_L2'
    for fires which burned in 2002: satellite images from LANDSAT 7 - dataset in GEE: 'LANDSAT/LE07/C02/T1_L2' 
    for fires which burned in 2012: satellite images from MODIS(500m) - dataset in GEE: 'MODIS/006/MOD09A1' and satellite images from LANDSAT 7 - dataset in GEE: 'LANDSAT/LE07/C02/T1_L2' 
    for fires which burned from 2013 to 2022: satellite images from LANDSAT 8 - dataset in GEE: 'LANDSAT/LC08/C02/T1_L2. 
    
The fire data- perimeter/bound, start/end date, area, year of burning- have been imported into GEE as assets and have been used as a table: 
(shared at https://code.earthengine.google.com/?asset=projects/the-name-367619/assets/Wildire_Perimeters_Dates_1984_2022_V6 )

To increase the efficiency of GEE, to perform each type of processing, different functions have been created and will be used inside the loops. 
The severity indices calculated within this code are as following: 
    NBR: Normalized Burn Ratio 
    dNBR: difference Normalized Burn Ratio 
    RdNBR: Relative difference of Normalized Burn Ratio 
    RBR : Relative Burn Ratio 
    dNBR-EVI: difference Normalized Burn Ration- Enhanced Vegetation Index

After running the code, it is highly likely that the browser freezes up and you will be given the choice of closing the browser or waiting. 
You should choose "waiting option" for GEE to become responsive again. Do not press "Exit". When the processing is done, the browser will unfreeze. When you want to export any of the processed maps or details about the maps, uncomment the export section written for that specific index. 

In the case of getting the error "API keys are not supported by this API. Expected OAuth2 access token or other authentication credentials that assert a principal", execute the code with smaller number of i. In case of getting the error "Earth Engine memory capacity exceeded." rerun the code especially for i for which the error was received.

This code is developed by Dina Jahanianfard, ULisboa. This code can only be used after the publication/citation of the manuscript entitled: "Multidecadal satellite-derived Portuguese Burn Severity Atlas (1984 -2022) ", ESSD, written by Jahanianfard.D, et al (2024).
