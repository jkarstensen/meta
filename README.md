# EUREC4A meta data repository

Shared metadata, code and standards designed to structure the EUREC4A data reposistory, improve treatment of metadata and thereby ease the EUREC4A data analysis. 

## State of the project

Currently, the [goals](goals.md) of the metadata repository are being refined while experiments on fist metadata structures, mostly considering measurement platforms are conducted.
If you just came across this repository, please have a look at the current [goals document](goals.md) as well as issues and pull requests.
Please don't hesitate to add more issues or pull requests if you have use cases, expectations, opinions or questions about EUREC4A data or metadata, which are not yet written down.

## Metadata concept

EUREC4A metadata will be sourced from the owners of the objects the metadata describes.  That is each instrument would provide instrument metadata, with a minimal set of controlled language, and a subset of this infomation would be inherited by the platform metadata.  Campaign metadata can then inherit information from the plafforms.  This ensures that all the metadata is provided by the owners.  At each stage of the process additional information could be included an inherited.  An example would be the flight-track dictionaries being developed for HALO, which would then find their way into the HALO metadata.

Metadata also proide a _controlled vocabulary_ i.e. a list of valid ways to refer to a platform, instrument, etc.

## Tentiative naming conventions

Although file naming conventions are not a particular goal of this metadata concept, some ideas have already evolved and can be found in [naming_conventions.md](naming_conventions.md) for reference.
