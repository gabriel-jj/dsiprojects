# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2 - Ames Housing Data and Kaggle Challenge

## Gabriel Choo, SG DSI 14

### Problem Statement
Ames is a city in Story County, Iowa, United States with 13 constituent neighborhoods. In order to raise value of a property, what are some of the key features or areas that a homeowner should focus on so that the property can fetch a higher price.

### Executive Summary

The objective of this report is to describe and infer our study of the key factors that might affect the sale price of a property in Ames and build a model that can help to determine the estimated sale price of a property.

The study included a detailed look at the various neighborhood of Ames, as well as the different features and conditions relating to each part of the property.

It has been observed that the key features that affect the sale price of a property is overall quality, age, size and the neighborhood that the property is located. The feature that appears to add most value to a property is the overall quality of the house and size of the ground living area. The fact that quality has more correlation than condition is that condition defect progress with age while in contrast a quality property grows with age. While size of property is always one of the factor when it comes to measuring of price, we have observed that the greater the proportion of overall ground living area, the higher the sale price is. However, there's one features that can negatively affect the sale price of a property. In one of the correlation analysis, we saw that an increase in the age of the property leads to drop in sale price.  

Homeowners can actually consider furnishing the overall quality and condition of the house before making a sale so that there's a higher probability that it can fetch a higher price. Since the heart of the home lies in the ground living area, it would be good to give a little update on the tiles and wall paint. Quality repairs to the fixtures and plumbing should also take into considerations as quality is one of the top positive correlation to sale price. Moreover if the property is located in areas like NorthRidge Heights and NorthRidge, homeowners can expect a higher sale price as compared to property in the other neighborhood.

It should be noted that this model will not generalize to a certain extent as the model only take into consideration of how property price is valuated in Aimes. The model includes the neighborhoods of Aimes in the modelling process hence it might not be applicable to other county or countries. However, in order to create a generalized model that can be used for any property, more datasets from various countries might be needed in the analyzing process.

### Data
For this project we are using Ames Housing Dataset from Kaggle:
- [Ames Housing Dataset](https://www.kaggle.com/c/dsi-us-6-project-2-regression-challenge/overview)
- [Data Documentation](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

### Data Dictionary

|Feature|Type|Description|
|:---|:---|:---|
|**ID**|*int64*|Observation number
|**PID**|*int64*|Parcel identification number  - can be used with city web site for parcel review
|**MS Subclass**|*int*|Identifies the type of dwelling involved in the sale
|**MS Zoning**|*object*|Identifies the general zoning classification of the sale
|**Lot Frontage**|*float*|Linear feet of street connected to property
|**lot area**|*int*|Lot size in square feet
|**Street**|*object*|Type of road access to property
|**Alley**|*float*|Type of alley access to property
|**Lot Shape**|*object*|General shape of property
|**Land Contour**|*object*|Flatness of the property
|**Utilities**|*object*|Type of utilities available
|**Lot Config**|*object*|Lot configuration
|**Land Slope**|*object*|Slope of property
|**Neighborhood**|*object*|Physical locations within Ames city limits
|**Condition 1**|*object*|Proximity to various conditions
|**Condition 2**|*object*|Proximity to various conditions
|**Bldg Type**|*object*|Type of dwelling
|**House Style**|*object*|Style of dwelling
|**Overall Qual**|*int*|Rates the overall material and finish of the house
|**Overall Cond**|*int*|Rates the overall condition of the house
|**Year Built**|*int*|Original construction date
|**Year Remod/Add**|*int*|Remodel date (same as construction date if no remodeling or additions)
|**Roof Style**|*object*|Type of roof
|**Roof Matl**|*object*|Roof material
|**Exterior 1**|*object*|Exterior covering on house
|**Exterior 2**|*object*|Exterior covering on house (if more than one material)
|**Mas Vnr Type**|*object*|Masonry veneer type
|**Mas Vnr Area**|*float*|Masonry veneer area in square feet
|**Exter Qual**|*int*|Evaluates the quality of the material on the exterior
|**Exter Cond**|*int*|Evaluates the present condition of the material on the exterior
|**Foundation**|*object*|Type of foundation
|**Bsmt Qual**|*float*|Evaluates the height of the basement
|**Bsmt Cond**|*float*|Evaluates the general condition of the basement
|**Bsmt Exposure**|*object*|Refers to walkout or garden level walls
|**BsmtFin Type 1**|*float*|Rating of basement finished area
|**BsmtFin SF 1**|*float*|Type 1 finished square feet
|**BsmtFinType 2**|*float*|Rating of basement finished area (if multiple types)
|**BsmtFin SF 2**|*float*|Type 2 finished square feet
|**Bsmt Unf SF**|*float*|Unfinished square feet of basement area
|**Total Bsmt SF**|*float*|Total square feet of basement area
|**Heating**|*object*|Type of heating
|**HeatingQC**|*int*|Heating quality and condition
|**Central Air**|*int*|Central air conditioning
|**Electrical**|*int*|Electrical system
|**1st Flr SF**|*int*|First Floor square feet
|**2nd Flr SF**|*int*|Second floor square feet
|**Low Qual Fin SF**|*int*|Low quality finished square feet (all floors)
|**Gr Liv Area**|*int*|Above grade (ground) living area square f
|**Bsmt Full Bath**|*float*|Basement full bathrooms
|**Bsmt Half Bath**|*float*|Basement half bathrooms
|**Full Bath**|*int*|Full bathrooms above grade
|**Half Bath**|*int*|Half baths above grade
|**Bedroom**|*int*|Bedrooms above grade (does NOT include basement bedrooms)
|*Kitchen**|*int*|Kitchens above grade
|**KitchenQual**|*int*|Kitchen quality
|**TotRmsAbvGrd**|*int*|Total rooms above grade (does not include bathrooms)
|**Functional**|*int*|Home functionality (Assume typical unless deductions are warranted)
|**Fireplaces**|*int*|Number of fireplaces
|**Garage Type**|*object*|Garage location
|**Garage Yr Blt**|*float*|Year garage was built
|**Garage Finish**|*float*|Interior finish of the garage
|**Garage Cars**|*float*|Size of garage in car capacity
|**Garage Area**|*float*|Size of garage in square feet
|**Garage Qual**|*float*|Garage quality
|**Garage Cond**|*float*|Garage condition
|**Paved Drive**|*object*|Paved driveway
|**Wood Deck SF**|*int*|Wood deck area in square feet
|**Open Porch SF**|*int*|Open porch area in square feet
|**Enclosed Porch**|*int*|Enclosed porch area in square feet
|**3-Ssn Porch**|*int*|Three season porch area in square feet
|**Screen Porch**|*int*|Screen porch area in square feet
|**Pool Area**|*int*|Pool area in square feet
|**Pool QC**|*int*|Pool quality
|**Fence**|*int*|Fence quality
|**Misc Feature**|*int*|Miscellaneous feature not covered in other categories
|**Misc Val**|*int*|$Value of miscellaneous feature
|**Mo Sold**|*int*|Month Sold (MM)
|**Yr Sold**|*int*|Year Sold (YYYY)
|**Sale Type**|*object*|Type of sale
|**SalePrice**|*int*|Sale price $$
