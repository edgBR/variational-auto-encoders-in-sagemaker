# variational-auto-encoders-in-sagemaker

The data in this set represents experiments from runs on a milling machine under various operating
conditions. In particular, tool wear was investigated (Goebel, 1996) in a regular cut as well as entry cut
and exit cut. Data sampled by three different types of sensors (acoustic emission sensor, vibration
sensor, current sensor) were acquired at several positions.

The data is organized in a 1x167 matlab struct array with fields as shown in Table 1 below:


case Case number (1-16)
run Counter for experimental runs in each case
VB Flank wear, measured after runs; Measurements for VB were not taken after each run
time Duration of experiment (restarts for each case)
DOC Depth of cut (does not vary for each case)
feed Feed (does not vary for each case)
material Material (does not vary for each case)
smcAC AC spindle motor current
smcDC DC spindle motor current
vib_table Table vibration
vib_spindle Spindle vibration
AE_table Acoustic emission at table
AE_spindle Acoustic emission at spindle

There are 16 cases with varying number of runs. The number of runs was dependent on the degree of
flank wear that was measured between runs at irregular intervals up to a wear limit (and sometimes
beyond). Flank wear was not always measured and at times when no measurements were taken, no entry
was made.