# Datawarehousing-for-vehicle-Accidents

### Introduction 

The goal of this project was to
1. To create a datawarehouse and store data in necessary dimensions
2. Created a Data model and finalized the model with a snowflake Schema.
3. The data was ingested into the target location(data warehouse) after necessary transfroamtions were done.
4.Do visualizations on top of the  SSAS cube which was deployed.

## Dataset used

The dataset which was chosen for this project is a collection of vehicle accidents. Since the dataset was not cleam enough, necessary modification swere done such as removing null values and unwanted columns as well. To complete the project successfully certain datasets were merged together.

## ER Diagram of the Data Model
![ER diagram](https://github.com/DerickAlex/Datawarehousing-for-vehicular-Accidents/blob/main/ER%20model.PNG)


## Technologies Used
1.SSMS - For Data storing purposes(raw,staging and the datawarehouse) , Creating transformations,Creating Packages,Data Profiling,Creation of SCDs etc.
2.SSAS - For deployment of OLAP Cube
3.SSRS - For Reporting 
4.PowerBI - For Reporting

## Execution of the Project
At first to load data into the staging area, I extracted data from two sources (SQLDB and a csv File).Staging area is an intermediate storage between source systems and target,datawarehouse.After all the data has been loaded properly to the staging phase,next step was to migrate it to the datawarehouse.

But beforehand necessary transformations had to be done , such as replacing null values with unkown and merge two tables together(inner join). Created slowly changing dimesnions as well . Since in this project, the history is not maintained due to this we can simply just load the new data rather than truncating the whole table and loading all data at once. 
Next step was to deploy a multi-dimensional cube via using SSAS, and create KPI s on top of this and later on use this as the data source for PowerBI for Further Visualizations.


