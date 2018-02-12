=========
LADT - Landscape Anomaly Detection Tool
=========

Date Created: November 16, 2017

Purpose:
This script calculates Relative Green, percent change in Relative Green, and Normalized Burn Ratio, and displays NAIP Imagery and USDA Croplands data layers to help the United
States Fish and Wildlife Service detect land use changes and preliminarily explore potential causes of the changes. 

Description:
The HCP study areas are located within the Pacific Southwest, a region that has highly variable land cover. Therefore, the main index used to evaluate vegetation cover was 
Relative Green (RG), which compares the NDVI in the study period to a historical baseline of NDVI values (Eq.1 and 2). To use the tool, the user selects the HCP of interest, and
the map zooms to the selected location. Then the user types in the month and year of interest. These two initial inputs are used by the tool when the user clicks other buttons
to run calculations and display other map layers.

In order to help the user preliminarily explain the potential causes of the land use changes, three ancillary datasets have been added. NBR (Eq. 3) establishes whether a fire
is likely to have occurred anywhere in the HCP, so the user can determine whether a fire could have been the cause of land use changes. The second ancillary dataset is the USDA
Croplands Data layers, which can help establish if change in crop type may have caused any land use changes. The third ancillary datset is the National Agriculture Imagery Program
data, which is high resolution imagery that can give the user a better context of what is happening in the HCP of interest.

For the RG related images, low vegetation/vegetation loss is displayed in purple, little change is displayed in white, and high vegetation/vegetation gain is displayed in green.
These colors were chosen instead of a more intuitive red/green color ramp to avoid challenges for people who are colorblind. For NBR, likelihood occurrence of fire (very low NBR)
is displayed in red and all other areas are beige.

NDVI = (NIR - Red) / (NIR + Red)
Equation 1: Normalized Difference Vegetation Index (NDVI) where NIR is the Near Infrared band and Red is the Red band in Visible Light.

RGi,j = (NDVIi,j - NDVImin,j) / (NDVImax,j - NDVImin,j)
Equation 2: where i,j is the recorded NDVI at time i at pixel j and NDVI max,j and NDVI min,j are the 'historical' max and min NDVI for that pixel from the baseline, which is
currently set to 2000-2010.

NBR = (NIR - SWIR) / (NIR + SWIR)
Equation 3: Normalized Burn Ratio (NBR) where NIR is the Near Infrared band and SWIR is the Short Range Infrared band.


Required Packages
=================
Google Earth Engine


Workflow:
1) Copy code into Google Earth Engine API. 
2) Hover your cursor over the part of the code at the very beginning that is underlined in yellow, and click Convert when the option appears.
3) Click 'Run' on the top right part of the code editor. The user interface will load on the right side of the screen.
4) Drag the map up to fill the screen and hide the code editor. Use the user interface to run analyses and display ancillary data.
**Use the Word and video tutorials as needed**


Contact
=======
Authors: 
Kimberly Johnson, Jarell Perez, Michaela Britt, Justin Herbst, Emily Gotschalk, Zachery Stout
Created by NASA DEVELOP Pacific Southwest Cross-Cutting II Team Fall 2017

Contact:
Kimberly Johnson
kimberlybuskjohnson@gmail.com
