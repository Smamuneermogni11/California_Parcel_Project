# Parcel Project in GIS using CRISP DM Model
This repository contains code and documentation for a parcel project in GIS using the CRISP DM (Cross-Industry Standard Process for Data Mining) model. The project aims to use GIS technology to analyze parcel data and provide insights on land use, land value, hazards and property taxation.

## Project Overview
The project follows the CRISP DM model, which consists of the following six phases:

Business Understanding
Data Understanding
Data Preparation
Modeling
Evaluation
Deployment
Business Understanding

In this phase, we identify the business objectives and define the problem statement. The objective of this project is to provide insights on land use, land value, and property taxation using parcel data. The problem statement is to analyze parcel data using GIS technology to identify patterns and trends in land use, value and hazards.

### Data Understanding
In this phase, we gather and understand the data that will be used for analysis. The data used for this project includes parcel data, which contains information on land use, property value, tax, ownership, hazards and addresses. The data is obtained from local government agencies and is in the form of shapefiles and CSV files.

Amador County: https://www.amadorgov.org/departments/information-technology/gis/gis-data

Constra Costa County: https://www.contracosta.ca.gov/1818/GIS

ElDorado County: https://www.edcgov.us/Government/planning/pages/parcel_data_information_system.aspx

Kern County: https://maps.kerncounty.com/H5/index.html?viewer=KCPublic

Madera County: https://www.maderacounty.com/government/geographic-information-system-gis

### Data Preparation
In this phase, we clean and preprocess the data for analysis. The data is first imported into a GIS software and geocoded to obtain spatial data. The data is then cleaned and filtered to remove any irrelevant or incomplete records. The data is also transformed and normalized to ensure consistency and accuracy in the analysis.

#### Data was enriched with Fire Hazard Zone, Flood Risk Zone, Fault Zones, Landslide Risk, Liquefaction Zones, Drought Conditions, and the potential for Renewable Energy (Solar Radiation and Wind Speed) layers, in addition to the layers provided by the county. The table schema is detailed below.
			
![image](https://user-images.githubusercontent.com/112990273/235898636-7d2eface-ca7c-4392-b125-c55580aa59fd.png)


### Modeling
In this phase, we develop a model to analyze the data and provide insights. The model used for this project is a spatial analysis model that uses GIS technology to identify patterns and trends in hazards and parcel data. The model is developed using Python and the ArcPy library, which provides access to GIS functionality to join hazards like Drought and Liquifaction using model builder in a form of toolbox, SCAG Calculator to join different types of Land Use using SCAG Codes and Colors and Geocoder to print missing addresses for Parcel Data.

## METHODOLOGY:

### DROUGHT MODEL BUILDER: 
The Drought Model Builder in ArcGIS Pro is a powerful tool that allows users to create custom models to analyze drought conditions. One of the key features of the model builder is its ability to use the Select by Location tool to intersect drought layers with county parcel layers. This allows users to determine the number of records that intersect between the two layers.

To begin using the Drought Model Builder, the user must first create a new model within ArcGIS Pro. This can be done by selecting the ModelBuilder button from the Analysis tab and then clicking on the New Model button. Once the model has been created, the user can begin adding tools and data layers to it.

To intersect the drought layer with the county parcel layer, the user must first add both layers to the model. This can be done by dragging and dropping the layers from the Layers pane onto the model canvas. Once the layers have been added, the user can connect them to the Select Layer by Location tool. The tool allows the user to specify the type of spatial relationship they want to use to select the features from the drought layer that intersect with the county parcel layer.

Once the Select Layer by Location tool has been configured, the user can use the Get Count tool to determine the number of records that intersect between the two layers. This information can be useful for determining the severity of drought conditions within a particular county.

To spatially join the drought layer with the county parcel layer, the user can use the Spatial Join tool. This tool allows the user to combine attributes from two layers based on their spatial relationship. Once the spatial join has been completed, the user can use the Select Layer By Attribute tool to filter the results to only show records that intersect between the two layers.

Finally, the user can use the Table Select tool to print out the records that intersect between the drought layer and the county parcel layer.

### LIQUIFACTION MODEL BUILDER: 
The liquefaction model builder in ArcGIS Pro is a powerful tool for identifying areas that may be susceptible to soil liquefaction during an earthquake. This tool uses the "Select by Location" option in ArcGIS Pro to identify the layers that intersect between the liquefaction and county parcel layers.

The first step in using this model builder is to ensure that both the liquefaction and county parcel layers are loaded into your ArcGIS Pro project. Once these layers have been added, you can begin using the "Select by Location" option to identify the intersecting features.

To do this, you will need to open the "Select by Location" tool in ArcGIS Pro. This tool allows you to select features from one layer that intersect with features from another layer. In this case, you will want to select features from the liquefaction layer that intersect with features from the county parcel layer.

Once you have identified the intersecting features, you can use the "Calculate Field" option to mark these features in the county parcel layer. This is done by adding a new field to the county parcel layer and setting the value of this field to 1 for all intersecting features and 0 for all other features.

### SCAG CALCULATOR: 
IT ADDS ALL THE SCAG CODES AND COLORS BASED ON LAND USE DATA

### GEOCODER: 
This tool uses longitude and latitude extracted from counties and uses python codes and api from arcgis developers website and prints the required addresses

### Evaluation
In this phase, we evaluate the model and its results. The model is evaluated based on its accuracy, completeness, and relevance to the business objectives. The results of the analysis are also evaluated to ensure that they are actionable and provide meaningful insights.

Amador County: https://agis.maps.arcgis.com/home/item.html?id=210fc281ff2641aaa7b34bb4893b77bf

Contra Costa County: https://agis.maps.arcgis.com/home/item.html?id=f93d97615a32416ebf5fd713762daca5

ElDorado County: https://agis.maps.arcgis.com/home/item.html?id=0df7235190884d01b5456ff07238c946

Kern County: https://agis.maps.arcgis.com/home/item.html?id=0e20e98c26b74271af49abde6546bb9d

Madera County: https://agis.maps.arcgis.com/home/item.html?id=69e0e387235648b08918b1271f338832

#### Deployment
In this phase, we deploy the model and its results to experience builder to create an app. The results are presented in the form of Experience Builder app. The stakeholders can use the results to make informed decisions on land use, property value, and tax, ownership, addresses and hazards.
The parcel project data is viewed in the app by integrating it with the parcel data source in the form of web app in ArcGIS Online. All layers of parcel data and other relevant data such as zoning, land use, and demographics is added to the app. There are widgets added to the app to provide interactive functionality, such as filtering, querying, and analysis.

![image](https://user-images.githubusercontent.com/112990273/235910137-da8e939f-c4c4-4548-b87f-f8bc985ba9f7.png)

Amador County: https://experience.arcgis.com/experience/7d1ac593e57c4ba9926b93ef09f6de9d/

Contra Costa County: https://experience.arcgis.com/experience/16ecbbf079064d178e985deee183020d/

ElDorado County: https://experience.arcgis.com/experience/815517ad9987454299dc92e69c765b18/

Kern County: https://experience.arcgis.com/experience/c85261946523493c988e49bb31e5c831/

Madera County: https://experience.arcgis.com/experience/600249bded9241fbb1cd599c750b3858/

### Getting Started
To run the code in this repository, you will need the following:

GIS software, such as ArcGIS
Python 3.x
ArcPy library
Once you have installed the required software and libraries, you can clone this repository and run the code in a Python IDE or Jupyter Notebook.

## Cloning
Here is a step by step method to clone this repository:
https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository

## Disclaimer
This application can be used by the public to view parcel information for the County. We have made every attempt to ensure the data contained within the map is up to date; however, we cannot guarantee the accuracy of the information provided or its lack thereof.
