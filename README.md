# get-weather

This repo collects and cleans data obtained from [JAXA](https://sharaku.eorc.jaxa.jp/GSMaP/) (rainfall) and land surface data from [CDS](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-land?tab=overview)

##  Data

- Descriptions for both data are in the ``document`` folder in the respective ``data`` folder.

## Code

- `ftp.ipynb`
  - Loads data from the server using ftp
  - This creates the data in zip format
  - Require username and password from JAXA to retrive the data

- `clean_zip.ipynb`
  - Cleans extracted zip files
  - the final data output is ``data/rain/main.csv``
  - To match with school location "data/school_coordinates.csv" is used. The closest observation from each school (latitude and longitude) is used.

- `grib.ipynb`
  - loads data obtained from [CDS](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-land?tab=overview)
  - To match with school location "data/school_coordinates.csv" is used. The closest observation from each school (latitude and longitude) is used.
