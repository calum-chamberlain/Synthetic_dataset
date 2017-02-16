##A canonical test-case for earthquake detection and automated analysis.

#Motivations:
Various detection methods have been devised, but comparing them is difficult – case-by-case, different methods have different benefits.  We seek to provide structured synthetic test-cases, where the distribution of earthquakes is known, to fully test the accuracy of these methods, as well as their efficiency. These synthetic test-cases will be open-source and provide a transparent benchmark for further improvements in earthquake detection and analysis.

#Methods:
  1. sta/lta
  2. matched-filter
  3. subspace
  4. FAST
  5. cross-station
  6. autocorrelation
  7. synthetic matched-filter
  8. brightness / back-projection
  9. Magnitude calculation methods
  1. auto-pick amplitudes
  2. Relative amplitudes
  3. SVD
  10. Location resolution

#Test-cases:
  1. Background poisson
  2. Tremorous (think about freq content & duration)
  3. Swarm
  4. Mainshock-aftershock.

#Tectonic settings:
  1. Vertical fault in simple horizontally-layered velocity model (SAF)
  2. Subduction type setting
  3. Geothermal type setting

#Plan:
  1. Generate velocity models for synthetic tectonic settings;
  2. Write scripts to generate synthetic waveforms using SPECFEM3D, to be used as templates/seeds;
  3. Generate synthetic miniseed files with background noise seeded with waveforms;

#Repository contents
  - models: Synthetic 3D velocity models;
  - scripts: Scripts to generate synthetic templates and synthetic data;
  - templates: Synthetic template waveforms, all synthetic earthquakes should be stored here;
  - synth_data: Continuous synthetic dataset to try and detect within.
