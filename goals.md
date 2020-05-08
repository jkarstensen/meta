# Goals for the EUREC4A metadata repository

In order to find a good design for the metadata structure, a set of goals which should be accomplished with the metadata must be established.
Based on these goals and available information about platforms, instruments and the like, a prototype for the metadata structure will be established.
This document is explicitly meant to be updated, comments are always welcome.

## direct goals
The achievement of these goals should be easily decidable by a yes / no answer.

* get a complete list of platform <-> PI associations
* list of measured quantities
* contact information for data usage
* provide unique names / ids to platforms and instruments to facilitate data exchange and communication
* source for campaign definitions (e.g. flight circles)
* produce an [intake](https://intake.readthedocs.io/en/latest/index.html) catalog for EUREC4A
* produce [GCMD Keywords](https://earthdata.nasa.gov/earth-observation-data/find-data/gcmd/gcmd-keywords). See also [here](https://gcmd.nasa.gov/search/Keywords.do#keywords) and [here](https://earthdata.nasa.gov/earth-observation-data/find-data/gcmd/gcmd-keywords)
* index to storage locations of measurement data (may also be generated from metadata included in data files)

## broader goals
These goals should be strived for, but the outcome of this might not be easily decided on by a yes / no answer.

* machine readable
* community sourced
* should evolve incrementally
* make things more findable

## non-goals
Things which are explicitly not a goal of the metadata structure

* focus on filenames as ordering scheme
* enforce a single tree structure
