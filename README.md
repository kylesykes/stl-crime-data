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

### Data Dictionary for clean_data


