# GGXF (Gridded Geodetic data eXchange Format)

GGXF is an Esri research and development project to define a standardized format for the exchange of gridded geodetic data. The project began in 2013 and has progressed in fits and starts since then. The requirements of GGXF are that it should psooses the following properties:

- Multi-dimensional
- Multi-resolution
- Self-defining metadata (header)
- Applicable to any datatype defined on a graticular grid
- Binary data storage structure
- Open-source GGXF reader/writers from commonly used existing formats

We quickly realized the formidible scope of the task. We also questioned the veracity of creating yet another standard format. After a fairly cursory review of existing data 


GGXF a formidable task? Why create yet another format?
NetCDF/HDF5 mature, widely used, robust, OGC Standard
 Can we adapt NetCDF/HDF5 to GGXF? Let’s try it!
Based on the Common Data Form Language File (CDL) standards:
Created a set of variables (standard names) relevant to GGXF
These defined a self-describing CDL header
Used NetCDF library to convert a multi-resolution, nested NTv2 grid file into CDL file and into binary NetCDF format
Successfully recovered CDL from binary NetCDF file
“Warm and fuzzy” that NetCDF could possibly serve as a platform for GGXF
