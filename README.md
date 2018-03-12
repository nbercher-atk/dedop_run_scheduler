# dedop_run_scheduler

DeDop automated job scheduler written in bash

DeDop is a User Configurable Tool for Processing Delay Doppler
Altimeter Data.  Please visite this page for more details:
<https://github.com/DeDop>.


<a id="orgb964766"></a>

## About dedop_run_scheduler

The dedop_run_scheduler script in intended to work with [dedop-core](https://github.com/DeDop/dedop-core).

What can do dedop_run_scheduler:

 - Run one dedop job per input ncfile and several jobs in parallel.

 - Automate the scheduling of parallel dedop jobs up to a limit
   defined by the user OR computed from the number of logical CPUs of
   the running machine.  Run a new job each time another one
   terminates, until no more files are to be processed.

 - By default, run on the default user's workspace input files, using
   the default workspace's configuration.

 - Optionally ignore the processing if output file(s) already
   existing, honouring =dedop run= '-s' option.

 - Automatically kill dedop jobs that have been running for too long
   (workaround an infinte loop bug in dedop-core versions <=1.1.0).

So far, only [bundled package of dedop-core v1.3.0](https://github.com/DeDop/dedop-core/releases/download/v1.3.0/DeDop-core-1.3.0-Linux-x86_64.sh%0A) has been tested, but
it should work with all versions.

The script should be mature enough to be run for production purposes.


<a id="org1782477"></a>

## Installation

1.  Clone this repository in some folder on your local machine.

2.  Add this folder to your PATH environment variable.

3. Ensure that the following files have the executable bit set:

    dedop_run_scheduler
    libdedop

    Note: dedop_run_scheduler requires that libdedop is also in your
    PATH, this is normally the case when steps 1. and 2. have been
    done properly.

## Documentation
The documentation of the dedop_run_scheduler is embed as commented
text in the script.

## Usage examples

 1. Run on the default user's workspace input files, using the default
    workspace's configuration:

    $ dedop_run_scheduler


## Authors
Nicolas Bercher, Along-Track SAS, 2017.

## Licence
The bash scripts in this repository are licenced under the terms of the GPLv2 licence.
