If you have a bunch of photometry files that you want to run PSNID on,
you need to do a few steps first.  Mainly, the photometry needs to be put into
SNANA format, and ideally also FITS format from TEXT files.

The enclosed NML file shows how to turn a simple list of photometry files
into a photometry version that SNANA can read in.  Simply run:

> snana.exe SNANA_to_ASCII.nml

the OUTPUT will be 5 files:
1.  a text list of the photometry inputs (VERSION.LIST)
2.  a text list of CIDs that were ignored (VERSION.IGNORE)
3.  a text README file (VERSION.LIST)
4.  a FITS file that has all of the HEADER information for each LC (VERSION_HEAD.FITS)
5.  a FITS file that has all of the PHOTOMETRY information for each LC (VERSION_PHOT.FITS)

Note that the INPUT photometry consists of a series of photometry text files,
plus 1-3 of the above; that is, even if there is nothing to IGNORE and no README,
a blank one must be created.

