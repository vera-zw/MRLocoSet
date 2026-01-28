# MRLocoSet
MRLocoSet: Simulation and experimental dataset for magnetic microroller locomotion, including state/control variables and dynamic linearization terms (e.g., φ matrices) in obstacle environments.
> Paper status: The associated manuscript is currently under preparation. Paper information will be added in a future update.

# Highlights
- Simulation + Experiment: both simulated and real microroller locomotion data are provided.
- Data-driven modeling oriented: each file includes state/control variables and dynamic linearization-related terms (e.g., φ matrix elements).
- Obstacle environments: trajectories are collected in obstacle fields similar to the example shown below.
![Obstacle environment example](docs/figures/obstacle_environment.png)
If the image is not displayed, please check that it exists at:
`docs/figures/obstacle_environment.png`

# Data Statistics
- Simulation: 6,279 trajectories (`.txt`), packaged into 7 zipped batches.
- Experiment: 82 trajectories (`.txt`), stored as plain text files.

# File Format (per .txt file)
Each `.txt` file is a comma-separated text file with a header row.
A typical header looks like:
`sequence, delta(k-1), f(k-1), theta(k), v(k), delta_diff(k-1), f_diff(k-1), theta_diff(k), v_diff(k), phi(1,1;k), phi(1,2;k), phi(2,1;k), phi(2,2;k)`

- `sequence`: sample index
- `delta, f, theta, v`: state/control-related variables used for microroller locomotion modeling
- `*_diff`: difference terms
- `phi(·,·;k)`: elements of the dynamic linearization matrix at time step k
