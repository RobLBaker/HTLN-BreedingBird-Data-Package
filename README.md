# HTLN-BreedingBird-Data-Package
----------------
Contains files and scripts for creating an NPS data package. The main areas are metadata (EML) and the final products (Package). The working example is the HTLN breeding bird protocol and database. The 2022 breeding bird protocol revision is located in Documentation. The directory ./src is my dev area. Files stored in other directories are functioning executable scripts and data products. Thanks for reading!

Additional background info on HTLN breeding bird monitoring project is here:

https://www.nps.gov/im/htln/birds.htm

--------------------------------
# Notes

20230427

Finished csv exports from SQL Server
Reviewed csv files
  lookup tables still need to be addressed
  join LUTs into data tables whereever possible

Lookup table - csv files affected
  cover class codes: 
    foliar-cover.csv
    horiz-distance-profile.csv
    horiz-vegetation-profile.csv
    veg-type.csv

Following all apply to site-birdobs.csv
  site conditions:
    wind codes
    rain codes
    noise codes
  bird observations:
    AOUCodes and species names
    Detection Type codes

Tree tally needs species as well as common name
  

20230403

Get site / bird observations in final form; habitat data in dataset flat file format from database.


20230331

Review these repos and docs

https://github.com/nationalparkservice/NPS_EML_Script

https://github.com/nationalparkservice/EMLeditor

https://github.com/nationalparkservice/NPSdataverse


Documentation for EML process at NPS

https://nationalparkservice.github.io/NPS_EML_Script/


Cleanup...

Moved all EML dev files back to src. 
Archived all of the itis work. 
EMLAssembly should auto-generate ITIS higher taxonomy.


20230310

Removed Validate component of repo. Validation will be included in a separate repo.


20230227

Installed SQL Server, loaded ITIS database. Created HTLN_Sandbox db. Ran join on TSN, ScientificName.
TSNs and scientific names in HTLN_Landbirds agree with Itis.


20230213

Created branch called 'itis'. Downloaded copy of itis. Need to install SQL Server on new computer.


20230130

Created species list based on observation data. List includes TSN, Family, Genus, Species, AOUCode, CommonName. 
Need copy of ITIS to join Orders to TSNs



20230120

Created branch for taxonomy. Write T-SQL to create species list including TSN, Family, Genus, Species, CommonName. Need write R script to insert Kingdom, Phylum, Order into each species record.


20221222

Re-ran T-SQL to pull .csv file. Removed CUVA data for now due to formatting issues with PlotID. Come back to this at some future point.

20221114

Loaded the .csv into R dataframe using fread.


20221216

Ran first part of EML creation script to create blank text files for the abstract, additional information, custom units, intellectual
rights, keywords, methods, and personnel. Then ran function to create "attributes_datafilename.txt" to describe the dataset attributes.

20221110

Downloaded EML_Creation_Script.R from here:

https://github.com/nationalparkservice/NPS_EML_Script

Created T-SQL script called BirdObservationThru2022.sql
Created .csv file called HTLNBreedingBirds_BirdObs.csv

Copied EML_Creation_Script.R to EML_Creation_Script_HTLNBreedingBirds.R

20221031

Installed packages associated with NPSdataverse from here:

https://github.com/nationalparkservice/NPSdataverse







