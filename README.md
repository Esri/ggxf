# GGXF (Gridded Geodetic data eXchange Format)

GGXF is an Esri research and development project to define a standardized format for the exchange of gridded geodetic data. The project began in 2013 and has progressed in fits and starts since then. The requirements of GGXF are that it should psooses the following properties:

- Multi-dimensional
- Multi-resolution
- Self-defining metadata (header)
- Applicable to any datatype defined on a graticular grid
- Binary data storage structure
- Open-source GGXF reader/writers from commonly used existing formats

We quickly realized the formidible scope of this task. We also questioned the rationale of creating yet another standard format. After a fairly cursory review of existing geodetic data grid formats coupled with the fact that Esri already had capability to work with NetCDF/HDF5, we focused on leveraging this widely used, robust and mature format for our GGXF. The fact that NetCDF was already an OGC standard bolstered our decision to proceed in this direction.

Having decided to adapt [NetCDF/HDF5](https://www.unidata.ucar.edu/software/netcdf/), we created a set of attribute and variable names relevant to GGXF based on the [CF Conventions and Metadata](http://cfconventions.org/) guidelines. Currently, the set of attribute and variable names we use to describe the NetCDF file comprises a combination of [NetCDF Attribute Convention for Dataset Discovery](https://www.unidata.ucar.edu/software/netcdf-java/current/metadata/DataDiscoveryAttConvention.html) attributes along with our newly developed attribute and variable names to define those attributes of a GGXF file common to all grids in the file. These GGXF standard attributes and variables define the metadata/header file needed to ensure the format is self-describing.

Using these parameters we can create a [Common Data Form Language File](https://www.unidata.ucar.edu/software/netcdf/workshops/most-recent/nc3model/Cdl.html) (CDL) which is a human-readable notation for NetCDF objects and data. We tested this by creating a CDL file of a multi-resolution, nested NTv2 grid file and applied the `ncgen` function from the NetCDF library to convert the CDL file into binary NetCDF format. We successfully recovered the original CDL from the binary NetCDF file using the `ncdump` function. This process gave us confidence that NetCDF could possibly serve as a platform for GGXF.

A more complete bacground of the development of GGXF and examples of GGXF format grids can be found in the files uploaded above. The table below describes the content of each of these files.

| File                                               | Description                                                                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 6.OGC standarization of gridded geodetic data.pptx | Lott, R.M., M. Kennedy, K.M. Kelly, R. Juergens, D. Burrows and K. Ryden, 2015,  Standard file format for the exchange of gridded geodetic data,  OGC TC/PC Meeting, Barcelona, Spain, 9-13 March 2015 |
|                                                    |                                                                                                                                                                                                        |
|                                                    |                                                                                                                                                                                                        |
|                                                    |                                                                                                                                                                                                        |
|                                                    |                                                                                                                                                                                                        |
|                                                    |                                                                                                                                                                                                        |
