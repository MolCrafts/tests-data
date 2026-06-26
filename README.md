# Chemfiles data files for integration tests

This repository contains data files for testing the
[chemfiles](https://github.com/chemfiles/tests-data) library.

Each folder contains files in a given format, and contains either files that should be
readable, or files that should fail. The failing files are put together into a `bad`
folder.

All these files are under the CC-0 licence.

## cube_traj/ — multi-frame electron-density cube trajectories

`au-h2-aimd-3frame.cube` — three consecutive frames of the total SCF electron
density from a CPMD ab-initio MD run (H2 incident on an Au(111) double layer;
26 atoms; 54×64×80 grid; atomic units), concatenated as standard Gaussian Cube
blocks. Frames 0–2 of a 25-frame trajectory.
Source: Axel Kohlmeyer, CPMD-VMD tutorial volumetric-data examples
(http://ftp.theochem.ruhr-uni-bochum.de/outgoing/axel_kohlmeyer/vmd-examples/au-dens-cube.tar.gz).
Real CPMD output (not synthetic). Consumed by molrs `CubeTrajectory` /
travis-parity-07 (every file in this dir must be a parseable multi-frame cube).
