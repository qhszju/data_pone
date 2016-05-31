#Brief

This repo contains the raw data for the paper titled **Spatial-temporal congestion identification based on Time Series Similarity considering Missing Data** . 

Two types of data is available: geo data and velocity data.

The velocity data is converted to **CSV** format, thus allow to be opened at Excel, etc. 

The geo data is in **shpfile** format, which is regulated by (Environmental Systems Research Institute Esri)

#Formate details

##Geo type
Geo data contains two sub-files: **link.shp** and **link.dbf** . 
The  **link.shp**  contains all the geometric location of each link (for example, ((x1,y1),(x2,y2),(x3,y3)) is a typical link, which consists of three points. And the link length is the length of piecewice linear curve (x1,y1)-----(x2,y2)------(x3,y3). Genearlly, number of points can not be controlled but rather depedent on the geo data collection equipments).

 **link.dbf** contains property of each link in the  **link.shp** . Such as link rank (major arterial road, branch road, etc), begning node, ending node, etc. 
 
 Geo files are mainly used to visualize the results. Besides it is used to set the data limit of the method. 



##velocity data

The data is velocity data collected at 12/01/2012, at HangZhou city, CHINA. The meta data is collected by GPS installed at each Taxi, the data in this repo is processed based on the raw data (raw data is not covered). It contains the velocity for each link at each interval (5min). For the whole day, there are 24 hours, thus 288*5min. Therefor there are 288 columns in the data.csv. Each column correspond to a 5min length time interval. 

Each row correspond to a link, labelled by its name. The two-way road is counted twice. For example, if the Link ID is 1234, Data at the two directions are collected respectively. In the dataset, there are two rows, **Link1234** and **Link1234Reverse** respectively. 

For some moments there are missing data, caused by either equipment failure, or there is no taxi go across. 