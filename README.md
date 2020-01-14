# GGXF (Gridded Geodetic data eXchange Format)

GGXF is an Esri research and development project to define a standardized format for the exchange of gridded geodetic data. The project began in 2013 and has progressed in fits and starts since then. The requirements of GGXF are that it should psooses the following properties:

- Multi-dimensional
- Multi-resolution
- Self-defining metadata (header)
- Applicable to any datatype defined on a graticular grid
- Binary data storage structure
- Open-source GGXF reader/writers from commonly used existing formats

We quickly realized the formidible scope of this task. We also questioned the rationale of creating yet another standard format. After a fairly cursory review of existing geodetic data grid formats coupled with the fact that Esri already had capability to work with NetCDF/HDF5, we focused on leveraging this widely used, robust and mature format for our GGXF. The fact that NetCDF was already an OGC standard bolstered our decision to proceed in this direction.

Having made the decision to adapt [NetCDF/HDF5]https://www.unidata.ucar.edu/software/netcdf/, we created a set of variables (standard names) relevant to GGXF based on the Common Data Form Language File (CDL) standard. These would define the self-describing metadata/header file needed to ensure the format was self-describing. Using our defined standard names we created a CDL file of a multi-resolution, nested NTv2 grid file and applied the `ncgen` function from the NetCDF library to convert the CDL file into binary NetCDF format. We successfully recovered the original CDL from the binary NetCDF file using the `ncdump` function. This process gave us confidence that NetCDF could possibly serve as a platform for GGXF.

...add table describing each file above ...
