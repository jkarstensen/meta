# EUREC4A meta data repository

Shared metadata, code and standards designed to structure the EUREC4A data reposistory, improve treatment of metadata and thereby ease the EUREC4A data analysis. 

## State of the project

Currently, the [goals](goals.md) of the metadata repository are being refined while experiments on fist metadata structures, mostly considering measurement platforms are conducted.
If you just came across this repository, please have a look at the current [goals document](goals.md) as well as issues and pull requests.
Please don't hesitate to add more issues or pull requests if you have use cases, expectations, opinions or questions about EUREC4A data or metadata, which are not yet written down.

## Metadata concept

Ideally the EUREC4A metadata would be sourced from the owners of the objects the metadata describes.  That is each instrument would provide an instrument_id.yaml file, with a minimal set of controlled language, and a subset of this infomation would be inherited by a platform_id.yaml.  The campaign_id.yaml could then inherit the information from the plafform.  This would ensure that all the metadata is sourced to the owners.  At each stage of the process additional information could be included an inherited.  An example would be the flight-track dictionsaries being developed for HALO, which would then find their way into the EUREC4A_HALO.yaml file.

## Tentiative naming conventions

Although file naming conventions are not a particular goal of this metadata concept, some ideas have already evolved and can be found in [naming_conventions.md](naming_conventions.md) for reference.
