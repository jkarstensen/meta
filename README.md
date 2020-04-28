# EUREC4A
Shared code and standards designed to ease the EUREC4A data analysis.

## Controlled vocabulary
For the data repository and post-processing we encourage a controlled vocabulary.  File names are to be composed from a hierarchical application of the applicable subset of this vocabularly.  The vocabulary regulates the following terms:

> Campaign-ID:  EUREC4A

> Project-ID:  This could be anything, but some common ones people have proposed to use to identify collective activities within EUREC4A includ ATOMIC.  Others could be UK, ISO, OA, CloudBrake, etc.

> Platform-ID:  This is a unique identifier of platforms used during EUREC4A.  Examples include BCO, ATR, HALO, Meteor, Melonhead (a glider) and so on

> Instrument-ID:  This is a unique identifier that is given to a particular instrument that may be operating on a specific platform, for instance WALES is an DIAL lidar on HALO, or the MRR is the Microrain radar at the BCO.  Groups organized around platforms should decide on the Instrument_IDs they wish to use, but when similar instruments are used across different platforms it would be helpful if groups tried to coordinate the choice of names.

> Product-ID:  THis might describe a product that is either associated with a platform, or with an instrument.   For instance Track describes the track (lat, lon, perhaps height) versus time of a platform, or in special cases where a tethered platform (like a CTD) is identified as an instrument rather than a platform on its own, then this could refer to the instrument.

> Variable-ID: This is the name of a specific output from an instrument.  It could be a voltage, or a temperature reading, or a reflectivity.

> Time-ID: For some data it may be useful to indicate the time of the measurement or the time-range of the data included in the file.  This will adopt the form YYYYMMDDTHHMMSS-YYYYMMDDTHHMMSS, or e.g., YYYYMMDD, or YYYYMMDDTHHMM for a single instance. 

> Version-ID: For data files the version of the data should be specified, and any updaes to the file should be accompanied with a new version number. 

## File Naming Conventions

Filenames should be composed of a hierarchical application of the applicable subset of the controlled vocabularly, with IDs separated by underscores.  Hyphens can be used for IDs composed of compound words.  Hence the structure would be:

`Campaign-ID_Project-ID_Platform-ID_Instrument-ID_Variable-ID_Time-ID_Version-ID.nc`

Examples could be
  - EUREC4A_Meteor_Track_v0.2.nc
  - EUREC4A_HALO_KT19_T2_20200202_v2.2.nc  
  - EUREC4A_ATOMIC_SWIFT12_T04_20200120-20200212_v1.0.nc
We ask that every file containe one Campaign_ID, one version_ID and at least one further ID specifiying the particulars of the data the file contains.

## File metadata

File meta data should repeat the ID information, i.e., Platform_ID: "ATR", Campaign_ID: "EUREC4A" and additionally contain contact information of the person responsible for the data.

## Coordinates and variables

We would prefer a controlled vocabulary for position information, i.e., time (seconds since YYYY-MM-DDTHH:MM:SS, lat (degree_north), lon (degree_east), height (m), depth (m).  Again coordination among instrument scientists so that similar instruments across different platforms have the same name would be desirable.
