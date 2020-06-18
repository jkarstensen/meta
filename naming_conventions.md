## EUREC4A
Shared code and standards designed to structure the EUREC4A data reposistory, improve treatment of metadata and thereby ease the EUREC4A data analysis.  An evolving metadata concept is proposed at the end of this page.


### Identifiers
The data repository, will be built around a controlled vocabulary consisting of a hierarchy of identifiers.  We also encourage the use of these identifiers in building file names and for inclusion as file meda-data.  We hope that doing so will help all of us see and more effectively use the diversity of data that has been collected, and also ease collaboration.

The identifiers are as follows, not every identifier will apply to every instance of the data:

  * **campaign_id:**  EUREC4A
  * **project_id:**  An optional identifier to allow groups to give additional specificity to a set of measurements collected with different platforms, for instance ATOMIC.
  * **platform_id:**  An identifier drawn from a controlled vocabulary specifying a platform from which the data was collected.  See [EUREC4A.yaml](EUREC4A.yaml) which maps platform_ids to platform metadata.
  * **instrument_id:**  Specifies an instrument from which a measurement has been made.  Ideally similar instruments from different platforms will adopt similar identifiers. Level 2 data will often have a platform_id and instrument_id, but in some cases an instrument and platform may be synoymous.  
  * **product_id:**  An optional identifier to be used with the instrument_id to allow groups the flexibility to group measurements in different ways, i.e., SAFIRE_Aerosol might designate a bundle of aerosol instruments run by SAFIRE.
  * **variable_id:** A specific quantity. Usually this will be the output from a sensor, but it could also be a derived or composite variable.  Examples might be a voltage on a power supply, a temperature reading, a radar reflectivity, the latitude and longitude of a track, or maybe the divergence from a sounding circle. 
  It should follow a standard vocabulary whenever possible the NetCDF Climate and Forecast (CF) Metadata Conventions.
  * **time_id:** For some data it may be useful to indicate the time of the measurement or the time-range of the data included in the file.  This will adopt the form yyyyddmmTHHMMSS-yyyyddmmTHHMMSS, or e.g., yyyymmdd for a single instance. 
 * **version_id:** The data versioning, in the form vN.M with N and M integers. Using version 0 for preliminary data is encouraged.

The EUREC4A data base will use the platform_id as the first level of data granualrity. Depending on the platform, additional levels of granularity (sub-directories) may be included and labeled by some (possibly empty) subset of instrument_id, product_id or variable_id.  It will not organize data by project_id, nor by time_id.

### File naming conventions

Filenames should be composed of a hierarchical application of the applicable subset of the controlled vocabularly, with ids separated by underscores.  Hyphens can be used for ids composed of compound words.  Hence the structure would be:

`<campaign_id>_<project_id>_<platform_id>_<instrument_id>_<variable_id>_<time_id>_<version_id>.nc`

Examples could be
  - EUREC4A_Meteor_Track_v0.2.nc
  - EUREC4A_ATR_Safire_Radiation_20200202_v2.2.nc  
  - EUREC4A_ATOMIC_SWIFT-12_T05_20200120-20200212_v1.0.nc
  - EUREC4A_Dropsonde_Circles_Divergence_v3.3.nc

We envision every file beginning with the campaign_id and ends with the version_id and includes at least one further id to add content specificity.

### File metadata

File metadata should include all the identifiers, i.e., platform_id: "ATR", campaign_id: "EUREC4A" and additionally contain contact information of the person or organization responsible for the file (its creator). Often the contact will be the PI for the platform (or instrument) or the creator for the derived product.  YAML databases are being provided for the EUREC4A community as a whole for the platforms [EUREC4A.yaml](EUREC4A.yaml). Instrument groups are encouraged to provide a similar metadata template to help others in the use and crediting of their data.

### Coordinates and variables

We suggest a controlled vocabulary for position information, i.e., time (seconds since 1970-01-01, lat (degree_north), lon (degree_east), z (m).  Again coordination among instrument scientists so that similar instruments across different platforms have the same name would be desirable.


