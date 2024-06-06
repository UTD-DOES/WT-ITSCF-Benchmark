# WT-ITSCF-Benchmark
## Introduction

In this repository, 75 inter-turn short circuit faults (ITSCFs) in wind turbine (WT) generator stator are defined and simulated based on the MATLAB/Simulink WT example: [Wind Turbine - MATLAB & Simulink (mathworks.com)](https://www.mathworks.com/help/sps/ug/wind-turbine.html)

In the Simulink WT model, the generator stator is modeled based on the generator's equivalent impedance R=0.0027 Ohm. Such stator winding is initially partition to healthy and faulty part, and an increasing series of faulty winding ratio p_s:={0.05, 0.1, 0.2, 0.3, 0.5} represents the propagation of the degradation. Then, a decreasing series of  short circuit resistance R_s:={1,0.1,0.01,0.001,0.0001} Ohm represents the degradation of the insulation layer. Considering ITSCFs taking place in three phases, totally 5x5x3=75 ITCSF scenarios are generated. Including a normal operation scenario with no ITSCF, the dataset contain 76 scenarios.

All scenarios run 80 seconds with default wind speed profile in the WT example. 3 phases' phase-to-phase current (in Ampere, A) and voltage (in Volt, V) signals are recorded at 4kHz frequency. 

The electrical signal data can be found in 76 WTG ITSCF mat folder. 76 .mat files associated with every scenario are included, where all signals are in time series format and separate metadata and ReadMe are provided. 

Raw current and voltage signals together with first-level approximation coefficients in terms of 4 different wavelet functions are visualized in 6fig Animation.mp4.

For those who want to access to the Simulink model, please refer to Wind Turbine Simulink (ITSCF).zip. Separate ReadMe.txt can be found inside.

## Usage of this dataset

While extensive Condition Monitoring and Fault Diagnosis (CMFD) systems are built on top of the Supervisory Control and Data Acquisition (SCADA) system, the high frequency information is missing in the 10-minute sampling dataset for condition monitoring, especially for electrical failure. This dataset is open-sourced to enhance the development of CMFD system in wind turbine generator.

More contributions based on the same benchmark WT model are highly welcomed. Any contribution and question can be emailed to: jingyi.yan@utdallas.edu

## Author Information
Jingyi Yan (jingyi.yan@utdallas.edu), Ph.D. Student, Center for Wind Energy, Department of Mechanical Engineering, The University of Texas at Dallas

Soroush Senemmar(soroush.senemmar@utdallas.edu), Ph.D. Student, Center for Wind Energy, Department of Electrical and Computer Engineering, The University of Texas at Dallas

Jie Zhang (jiezhang@utdallas.edu), Associate Professor, Center for Wind Energy, Department of Mechanical Engineering, Department of Electrical and Computer Engineering, The University of Texas at Dallas

