# Inter-Turn Short Circuit Faults (ITSCFs) Simulation Dataset for Wind Turbine (WT) Generators
## Introduction

This repository contains a comprehensive dataset of 75 inter-turn short circuit faults (ITSCFs) simulated in a wind turbine (WT) generator stator, based on the MATLAB/Simulink WT example: [Wind Turbine - MATLAB & Simulink (mathworks.com)](https://www.mathworks.com/help/sps/ug/wind-turbine.html)

## Simulation Details
Model Specifications: The generator stator in the Simulink WT model is characterized by an equivalent impedance of R=0.0027 Ohm.

Fault Definition: The stator winding is divided into healthy and faulty segments. The faults are defined by varying the faulty winding ratio p_s across values {0.05, 0.1, 0.2, 0.3, 0.5} , which indicates the extent of degradation. Additionally, the short circuit resistance R_s varies across {1,0.1,0.01,0.001,0.0001} Ohm to simulate different levels of insulation deterioration. 

Scenario Generation: Considering ITSCFs in all three phases, a total of 75 ITSCF scenarios (5 faulty winding ratios × 5 short circuit resistances × 3 phases) are generated. Including a baseline scenario with no ITSCF, the dataset comprises 76 scenarios in total.

Simulation Duration: Each scenario runs for 80 seconds using the default wind speed profile provided in the WT example.

Data Recording: Phase-to-phase current (in Amperes, A) and voltage (in Volts, V) signals are recorded at a sampling frequency of 4 kHz. 

## Dataset Contents
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

