# stl-crime-data
### Overview
This repo serves as a place for the St. Louis Crime Data from the [St. Louis Metropolitan 
Police Departments website](http://www.slmpd.org/Crimereports.shtml).  The data extends back to January 2008 and goes through to the present.  There are scripts to reproduce our scraping process and cleaning process.  While we provide a cleaned version of the data, the raw files are provided along with our scripts so anyone can reproduce the data set.

### Files

**raw_data:** The raw data files scraped from the website.  Raw data is comma seperated.

**clean_data:** The dataset cleaned and enriched with additional information from other data sets.  Cleaned data is tab-delimited.

**CrimeDataFrequentlyAskedQuestions.pdf:** The FAQ from SLMPD's website describing the raw_data sets.

**UCRCodes.csv:** Lookup table for the 26 types of crimes as defined by the FBI using the Uniform Crime Repoting (UCR) Codes (mentioned in the FAQ above but completed with some digging through FBI's website and the raw_data).

**neighborhood_lookup.csv:** Lookup table for to enrich the data with names of neighborhoods found in the FAQ above.

**scraping_stl_crimedata.ipynb:** IPython notebook used to scrape the raw_data from the website.

**cleaning_stl_crime_data.ipynb:** IPython notebook used to transform the raw_data into clean_data.

### Data Dictionary for clean_data (raw_data is described in FAQ above)

|  Column | Format  | Description  |
|---|---|---|
|FileName                          |   string  | File name correspoding to the raw_data file where the row originated from |
|AdministrativeAdjustmentIndicator |   string  | Y/N, indicates whether the entry was adjusted by an admin.  An administrative adjustment indicates a change in crime classification |
|CADAddress                        |   string  | Address number where incident occured as reported by 911 caller |
|CADStreet                         |   string  | Stree name where incident occured as reported by 911 caller |
|CodedMonth                        |   string  | YYYY-mm ; Year and month reported for some fields (incomplete, see Issue #9)|
|Complaint                         |   string  |  (Unique?) Number assigned to incident|
|Count                             |   int64   | Integer representing how the crime affects the total crime number.  **Summing on this column will give you the total number of crimes**|
|Crime                             |   string  | 6-digit crime code, as defined by Uniform Crime Reporting guidelines |
|DateOccured                       |   string  | Date the incident was reported to have occured|
|Description                       |   string  | Description of the crime described by 'Crime' column |
|District                          |   int64   | 1-9; indicates which police district a crime was reported in|
|FlagAdministrative                |   string  | Y/N|
|FlagCleanup                       |   string  | Y/N|
|FlagCrime                         |   string  | Y/N|
|FlagUnfounded                     |   string  | Y/N|
|ILEADSAddress                     |   string  | Address number logged on official police report |
|ILEADSStreet                      |   string  | Street name logged on official police report |
|LocationComment                   |   string  | Additional comments about the location |
|LocationName                      |   string  | Additional information to help identify location (St. Louis Zoo, Scottrade Center, etc.)|
|MonthReportedtoMSHP               |   string  | YYYY-mm ; Year and month reported for some fields (incomplete, see Issue #9)|
|Neighborhood                      |   int64   | Number representing neighborhood incident was reported in|
|NewCrimeIndicator                 |   string  | Y/N |
|UnfoundedCrimeIndicator           |   string  | Y/N |
|XCoord                            |   float64 | X-Coordinates in State Plane NAD83 format|
|YCoord                            |   float64 | Y-Coordinates in State Plane NAD83 format|
|NeighborhoodName                  |   string  | Neighborhood name, matched from 'Neighborhood'|
|NeighborhoodPrimaryDistrict       |   float64 | Primary police district the neighborhood lies in|
|NeighborhoodAddlDistrict          |   float64 | Additional police districts that the neighborhood might be in|
