# Parcel Project in GIS using CRISP DM Model
This repository contains code and documentation for a parcel project in GIS using the CRISP DM (Cross-Industry Standard Process for Data Mining) model. The project aims to use GIS technology to analyze parcel data and provide insights on land use, land value, and property taxation.

## Project Overview
The project follows the CRISP DM model, which consists of the following six phases:

Business Understanding
Data Understanding
Data Preparation
Modeling
Evaluation
Deployment
Business Understanding

In this phase, we identify the business objectives and define the problem statement. The objective of this project is to provide insights on land use, land value, and property taxation using parcel data. The problem statement is to analyze parcel data using GIS technology to identify patterns and trends in land use and value.

### Data Understanding
In this phase, we gather and understand the data that will be used for analysis. The data used for this project includes parcel data, which contains information on land use, property value, and tax assessments. The data is obtained from local government agencies and is in the form of shapefiles and CSV files.

### Data Preparation
In this phase, we clean and preprocess the data for analysis. The data is first imported into a GIS software and geocoded to obtain spatial data. The data is then cleaned and filtered to remove any irrelevant or incomplete records. The data is also transformed and normalized to ensure consistency and accuracy in the analysis.

### Data was enriched with Fire Hazard Zone, Flood Risk Zone, Fault Zones, Landslide Risk, Liquefaction Zones, Drought Conditions, and the potential for Renewable Energy (Solar Radiation and Wind Speed) layers, in addition to the layers provided by the county. The table schema is detailed below.


Name of Field

Alias

Type of Data

Description

APN

APN

STRING

Assessor's Parcel Number

HOUSE_NUM

HOUSE NUM

INTEGER

House Number

PREFIX_DIR

PREFIX DIR

STRING

Prefix Direction

ST_NAME

STREET NAME

STRING

Street Name

ST_TYPE

STREET TYPE

STRING

Street Type

UNIT

UNIT

STRING

Unit

FULL_ADD

FULL ADDRESS

STRING

Full Address

FULL_STNA

FULL STREET NAME

STRING

Full Street Name

CITY

CITY

STRING

City

ZIP_CODE

ZIP CODE

STRING

Zip Code

LAND_USE

LAND USE

STRING

Land Use (County)

ZONING

ZONING

STRING

Zoning

SCAG_LUCO

SCAG LANDUSE CODE

STRING

Land Use (SCAG Code)

SCAG_LU

SCAG LANDUSE

STRING

Land Use (SCAG)

FHSZ_CODE

FIRE HZ ZONE CODE

STRING

Fire Hazard Zone Code

FHSZ_DESC

FIRE HZ ZONE DESC

STRING

Fire Hazard Zone Description

FLO_CODE

FLOOD CODE

STRING

Flood Risk Code

FLO_DESC

FLOOD DESC

STRING

Flood Risk Description

FAULTZONE

FAULT ZONE

STRING

Fault Zone

LANDSLIDE

LANDSLIDE

STRING

Landslide

LIQ_ZONE

LIQUIFACTION ZONE

STRING

Liquifaction Zone

DROUGHT

DROUGHT

STRING

Drought

DRO_DESC

DROUGHT DESC

STRING

Drought Description

SOL_RAD

SOLAR RADIATION

DOUBLE

Solar Radiation

WIND_SP

WIND SPEED

DOUBLE

Wind Speed

LAND_VAL

LAND VALUE

DOUBLE

Land Value

BUI_AREA

BUILT AREA

DOUBLE

Built Area

TAX

TAX

STRING

Tax

OWNERSHIP

OWNERSHIP

STRING

Ownership

AREA_AC

AREA ACRES

DOUBLE

Acres

AREA_SQFT

AREA SQ FT

DOUBLE

Square Feet

### Modeling
In this phase, we develop a model to analyze the data and provide insights. The model used for this project is a spatial analysis model that uses GIS technology to identify patterns and trends in land use and value. The model is developed using Python and the ArcPy library, which provides access to GIS functionality.

### Evaluation
In this phase, we evaluate the model and its results. The model is evaluated based on its accuracy, completeness, and relevance to the business objectives. The results of the analysis are also evaluated to ensure that they are actionable and provide meaningful insights.

#### Deployment
In this phase, we deploy the model and its results to stakeholders. The results are presented in the form of maps, charts, and reports. The stakeholders can use the results to make informed decisions on land use, property value, and tax assessments.

### Getting Started
To run the code in this repository, you will need the following:

GIS software, such as ArcGIS or QGIS
Python 3.x
ArcPy library
Once you have installed the required software and libraries, you can clone this repository and run the code in a Python IDE or Jupyter Notebook.

## Contributing
Contributions to this project are welcome. If you would like to contribute, please submit a pull request with your changes.

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.
