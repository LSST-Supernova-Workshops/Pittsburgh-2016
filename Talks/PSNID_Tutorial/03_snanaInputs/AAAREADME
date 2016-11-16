SNANA_PSNID_XX.NML:

Different ways of specifying the CIDS to be run over:

01:  SNCID_LIST
     Instead of doing a range, one can do a list of discrete values.
     NOTE that these discrete values are ON TOP OF whatever is
     given by CUTWIN_CID; if that parameter is not specified, everything
     will be run.  So make sure to feed it a null list.


02:  SNCID_LIST_FILE
     Specify a list in a CSV, space delimited, or hard break file.


Variations on the output data format

03:  SNTABLE_LIST
     Change the format or number of output files that are written


Other keywords to note:

OPT_MWEBV
	0 = no extinction
	1 = value in FILE header
	2 = SFD 98
	3 = Schlafly 2013


OPT_SETPKMJD
	-1 = DO NOT set pkmjd before running PSNID
	All other values are in 5.4 of SNANA manual
	and are now recommended against.


CUTWIN_NEPOCH: 5, 999
	Require any number of epochs of photometry between the two given values
	There are also parameters for specifying N filters out of a specified
	      list where M have SNR >= X.  Multiple such parameters can be set.
	

