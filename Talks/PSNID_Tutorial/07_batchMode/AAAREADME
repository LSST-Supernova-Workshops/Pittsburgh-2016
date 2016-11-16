For large runs, it is preferable to split PSNID into many separate smaller jobs,
running it in 'batch' mode.  To do this, you do the following:


1.  Add the following to the top of the NML file:

JOBNAME_LCFIT: psnid.exe

This specifies the name of the script to run one each separate batch job once
it is split up



2.  Specify the output directory

OUTDIR:  PSNID_OUTPUT

There will be a subdirectory that has the FITRES file after the batch job has run.
It also stores all the logs from each individual SPLIT job, and is necessary for
the code to determine when all the jobs are finished so the output can be
merged together


3.  Create your BATCH template

Most of these are machine-specific; included in this directory is a template
that works on the UChicago cluster 'Midway'.



4.  Run the code 'split_and_fit.pl' with the updated NML file:

> split_and_fit.pl BATCH_PSNID.NML

This is the SNANA utility that will split the job into many smaller jobs,
using the JOBNAME_LCFIT parameter to determine which script will be run
on each job.  Note that this script can also be used with JOBNAME snlc_fit.exe.



Notes
- this example ran for me (50 batch jobs, 611 SNe) in ~7 minutes on Midway.
- there are additional flags (e.g., GZIP_FLAG, DELAY_SUBMIT) which you can
  tell from reading the comments in the header are completely optional.
