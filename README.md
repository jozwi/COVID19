# COVID19
KNIME workflow for calculation of daily compartment numbers

An algorithm was developed in KNIME software in order to automatically calculate the GLEAMviz outputs into actual daily case numbers of different compartments (i.e. number of people in every compartment on a given day).

Usage:

- Download GLEAMviz output data: the .tsv files saved separately for exposed, infected and recovered compartments for the chosen geographic region in the Simulator.
- Download and launch KNIME workflow published here
- Select the path to the files in the List Files node
- Add input values* per compartment in the Table Creator node
- Set output path in the Image Writer(Port) node
- Run the workflow.

*Input values mean initial global distribution of population in compartments (compartment/person, e.g. [susceptible=9 213 355, exposed=6, infected=5, recovered=0] = Hungarian population(100%)=9 21 33 66).

The output file shows the distribution of the actual daily case numbers of the four compartments on a graph.

The workflow works with input .tsv file of GLEAMviz version 7.0 for SEIR compartment models.

The KNIME basic user instructions are available at: https://www.knime.com/knime
The user must ensure that the R plugin is installed so that the R script is available in node repository of KNIME. The following R packages are required for script to work properly:

- ggplot2
- tidyverse
