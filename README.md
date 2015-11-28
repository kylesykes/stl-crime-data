# stl-crime-data
A repo to scrape and store the crime data from the St. Louis Metropolitan 
Police Departments website.

The raw data files scraped from the website can be found in raw_data.

There is a cleaned up version of the data in clean_data.  The file is
tab delimited and cleaned up to enable easy analysis for anyone who
wishes to play around with this data set.  In particular, neighborhood
information has been included using the neighborhood lookup table in the
FAQ.  The indicator/flag fields have been cleaned up to be simple Y/N.
There are columns denoting which raw_data file the data came from,
as well as a consistent column listing the date/time the crime was
reported to have occured.

Website data was scraped from:
http://www.slmpd.org/Crimereports.shtml
