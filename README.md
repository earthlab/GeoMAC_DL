# GeoMAC DL
###### A Python script to download fire data from [GeoMAC](http://www.geomac.gov/)

## Description

[GeoMAC](http://www.geomac.gov/) (Geospatial Multi-Agency Coordination Group) is an application from USGS which hosts and distributes fire data. Data from GeoMAC is downloaded as a KMZ (zipped KML file) with user-inputted layers and formatting. Once downloaded, this data can be viewed with applications such as [Google Earth](https://www.google.com/earth/)

### Running w/ User Input

When downloading data from GeoMAC you must specify which server to download data from, which layers you want in the KMZ file, and how you want this data formatted. If you do not know this information ahead of time, you can run this script interactively and these options will be provided to you. Place the script in the directory you wish to download data to, cd into that directory from a command line, and run:

```
python GeoMAC_DL.py
```

Input format is specified below:
 1. Enter what you want your downloaded KMZ file to be named
 2. Enter the corresponding number of the listed servers you want to download data from
 3. Enter the corresponding number(s) of the layers you want included in the KMZ file separated by commas and no spaces (Example: 1,3,7)
 4. Enter the corresponding number of the layer option that you want the KMZ file to be formatted in
 
### Running Directly from the Command Line

If you already know the information specified in the previous section, you can run this script directly from the command line with additional arguments. The command line arguments following 'python GeoMAC_DL.py are as follows:
1. <server>, The corresponding number of the server you wish to download data from
2. <file_name>, The name you want the downloaded KMZ file to be
3. <layer_numbers> ,The numbers of the layers you want to be included in the KMZ file separated by periods and no spaces (Example: 1.3.7)
4. <layer_option>, The corresponding number of the layer option that you want the KMZ file to be formatted in (1 = Composite, 2 = Separate Image, 3 = Non-Composite)

An example is provided below:

```
# python GeoMAC_DL.py <server> <file_name> <layer_numbers> <layer_option>
python GeoMAC_DL.py 1 firedata 1.3.7 1
```

Running this will download a KMZ file named 'firedata' with layers 1, 3, and 7 in composite format from the first server hosted on GeoMAC.