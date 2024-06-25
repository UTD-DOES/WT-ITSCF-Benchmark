# Inter-Turn Short Circuit Faults (ITSCFs) Simulation Dataset for Wind Turbine (WT) Generators
## Introduction

This repository contains a comprehensive dataset of 75 inter-turn short circuit faults (ITSCFs) simulated in a wind turbine (WT) generator stator, based on the MATLAB/Simulink WT example: [Wind Turbine - MATLAB & Simulink (mathworks.com)](https://www.mathworks.com/help/sps/ug/wind-turbine.html)

## Simulation Details
- **Model Specifications:** The generator stator in the Simulink WT model is characterized by an equivalent impedance of R=0.0027 Ohm.

- **Fault Definition:** The stator winding is divided into healthy and faulty segments. The faults are defined by varying the faulty winding ratio p_s across values {0.05, 0.1, 0.2, 0.3, 0.5} , which indicates the extent of degradation. Additionally, the short circuit resistance R_s varies across {1,0.1,0.01,0.001,0.0001} Ohm to simulate different levels of insulation deterioration. 

- **Scenario Generation:** Considering ITSCFs in all three phases, a total of 75 ITSCF scenarios (5 faulty winding ratios × 5 short circuit resistances × 3 phases) are generated. Including a baseline scenario with no ITSCF, the dataset comprises 76 scenarios in total.

- **Simulation Duration:** Each scenario runs for 80 seconds using the default wind speed profile provided in the WT example.

- **Data Recording:** Phase-to-phase current (in Amperes, A) and voltage (in Volts, V) signals are recorded at a sampling frequency of 4 kHz. 

## Dataset Contents
- **Data Files:** The "76 WTG ITSCF .mat" folder contains 76 .mat files, each corresponding to one scenario. The files include time series data of the electrical signals.

- **Additional Resources:** Separate metadata and a ReadMe file provide detailed information about the dataset.

- **Visualization:** Raw current and voltage signals, along with first-level approximation coefficients derived from four different wavelet functions, are visualized in the "6fig Animation.mp4".

- **Model Access:** The Simulink model is available in "Wind Turbine Simulink (ITSCF).zip". A separate ReadMe.txt file within the zip provides additional guidance.

## Usage of this dataset

This dataset is intended to support the development of advanced Condition Monitoring and Fault Diagnosis (CMFD) systems for wind turbine generators. Unlike the typical 10-minute sampling datasets from Supervisory Control and Data Acquisition (SCADA) systems, this dataset includes high-frequency information crucial for detecting electrical failures.

## Contributions and Contact
Contributions and further research based on this benchmark WT model are highly encouraged. For inquiries or to contribute, please contact:

- **Jingyi Yan**, Ph.D. Student, Center for Wind Energy, Department of Mechanical Engineering, The University of Texas at Dallas (jingyi.yan@utdallas.edu)

- **Soroush Senemmar**, Ph.D. Student, Center for Wind Energy, Department of Electrical and Computer Engineering, The University of Texas at Dallas (soroush.senemmar@utdallas.edu)

- **Jie Zhang**, Associate Professor, Center for Wind Energy, Department of Mechanical Engineering, Department of Electrical and Computer Engineering, The University of Texas at Dallas (jiezhang@utdallas.edu)

