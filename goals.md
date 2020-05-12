# Goals for the EUREC4A metadata repository

To design the metadata structure, a set of goals that this metadata should serve is to be established. Based on these goals and available information about platforms, instruments and the like, a prototype for the metadata structure will be established. This document is explicitly meant to be updated, comments are always welcome.

## direct goals
The achievement of these goals should be easily decidable by a yes / no answer.

* establish ownership and responsibility for measurements, instruments and platforms, e.g.,
  - association with a PI
  - institutional ownership, if applicable
  - contact for usage questions
  - provide means of acknowledging use of data.
* ability to localize measurement (time, place, instrument, quantity), e.g.,
  - through unique names / ids to platforms and instruments
  - list of measured quantities
  - platform that hosted measurement
* support the cataloguing of larger datsets, e.g, for use by other tools, such as  [intake](https://intake.readthedocs.io/en/latest/index.html).
* index to storage locations of measurement data (may also be generated from metadata included in data files)

## broader goals
These goals should be strived for, but the outcome of this might not be easily decided on by a yes / no answer.

* machine readable
* community sourced
* should evolve incrementally
* make things more findable
* ability to trace version history of measurements
* ability to trace version history of metadata
* ability to identify commonalities with other measurements, e.g., from the same or similar instruments
* provide a means to share common analysis conventions, e.g., segmentation, thresholding
* adopt existing standards to the extent possible, e.g., [GCMD Keywords](https://earthdata.nasa.gov/earth-observation-data/find-data/gcmd/gcmd-keywords). See also [here](https://gcmd.nasa.gov/search/Keywords.do#keywords) and [here](https://earthdata.nasa.gov/earth-observation-data/find-data/gcmd/gcmd-keywords)

## non-goals
Things which are explicitly not a goal of the metadata structure

* focus on filenames as ordering scheme
* enforce a single tree structure
* imposed preconceived ways of working or sharing of data
