# GINav
NOTE: The program is still under development, and some bugs still exist in GINav. Comments and suggestions from users are welcome, please send them to the author (kaichen@cumt.edu.cn). Additionally, we will further optimize GNSS/INS integration algorithms and develop a C language-based GINav. If you're interested in the GINav algorithm, you can join the GINav discussion group (`QQ:533185090`) <br>

## Introduction <br>
GINav is an open-source software, which focuses on the data processing and analysis of GNSS/INS integrated Navigation system, and can also process multi-constellation and multi-frequency GNSS data. GINav is suitable for in-vehicle scenarios and is aimed at providing a useful tool for carrying out GNSS/INS-related research. It is a convenient platform for testing new algorithms and experimental functionalities. GINav is developed in MATLAB environment. It provides the user-friendly graphical user interface (GUI) to facilitate users to quickly use it, and a visualization tool, GINavPlot, is also provided for solution presentation and error analysis.  <br>
The main features of the software are: <br>
* Support GNSS absolute positioning modes, include standard single positioning (SPP) and precise single positioning (PPP) <br>
* Support GNSS relative positioning modes, include post-processing differenced, kinematic and static (PPD, PPK and PPS) <br>
* Support multi-constellation and multi-frequency GNSS data processing <br>
* Support GNSS/INS loosely coupled (LC) modes, include SPP/INS LC, PPD/INS LC, PPK/INS LC and PPP/INS LC <br>
* Support GNSS/INS tightly coupled (TC) modes, include SPP/INS TC, PPD/INS TC, PPK/INS TC and PPP/INS TC <br>
* INS-aided cycle slip detection and robust estimation for GNSS/INS integration <br>
* Convenient visualization <br>
## Requirements <br>
GINav was developed and tested in MATLAB version 2016a. For this reason, MATLAB version 2016a or newer is required for running GINav. Furthermore, GINav uses LAMBDA v3.0 toolbox to resolve ambiguity. If you use PPK, PPS or PPK/INS mode to process data, please download and install the lambda-3.0.zip file from http://gnss.curtin.edu.au/research/lambda.cfm. <br>
## Installation <br>
The installation steps of GINav are as follows: <br>
(1).Unzip GINav.zip to the GINav folder <br>
(2).Unzip lambda-3.0.zip and place the lambda-3.0 folder into the `GINav\3rd` folder <br>
(3).Open the MATLAB application and set the current folder to the unzipped GINav folder <br>
## Quick Start <br>
Please refer to the GINav manual. <br>
## Configuration file <br>
Please refer to the GINav manual. <br>
## GINavPlot <br>
GINavPlot is a visualization tool for solution presentation and error analysis, it provides three modules, namely, Plot, Error Plot and PPP Plot modules. You can run `GINav\Plot_Analysis.m` to start GINAvPlot. Please refer to the GINav manual for the usage of GINavPlot. <br>
## Dataset <br>
GINav provides different dataset to evaluate its performance, you can use the corresponding configuration file in `GINav\conf\` folder to perform GNSS modes and GNSS/INS integration modes. Note that some data are collected from the Internet, if you use the dataset, please cite related paper or indicate the source. Please refer to the GINav manual for more details. <br>
* Dataset "data_cpt". This dataset is collected in a suburban environment with vehicle. The data collection platform is equipped with the Trimble R10 receiver and a tactical grade IMU, together with accurate reference solutions from NovAtel-SPAN-CPT system. This dataset can be used to evaluate the performance of GINav. You can use the corresponding configuration file in `GINav\conf\` folder to perform GNSS modes (SPP, PPD, PPK and PPP) and GNSS/INS integration modes (SPP/INS LC, PPD/INS LC, PPK/INS LC PPP/INS LC, SPP/INS TC, PPD/INS TC, PPK/INS TC and PPP/INS TC), and analyze position, velocity and attitude error using GINavPlot. <br>
* Dataset "data_tokyo". This dataset comes from open-source project UrbanNav that can be found at website https://github.com/weisongwen/UrbanNavDataset. The dataset was collected in a typical urban canyon of Tokyo on December 19, 2018. It can be used to assess the availability of GINav for handling urban dataset. You can use the corresponding configuration file in `GINav\conf\` folder to perform SPP, PPK, SPP/INS TC and PPK/INS TC modes, and analyze position, velocity and attitude error using GINavPlot. <br>
* Dataset "data_mgex". The GNSS observations are collected from IGS-MGEX stations on December, 1, 2019, with 30s sampling intervals, including station WUH2, JFNG and HARB. The dataset includes all required files to perform PPP. You can use the corresponding configuration file in `GINav\conf\` folder to perform PPP mode, and plot PPP error using GNIavPlot. <br>
* Dataset "data_cu". The short-baseline GNSS data are collected from GNSS Research Centre at Curtin University (http://gnss.curtin.edu.au/). GNSS observations on March, 6, 2020 from station CUAA and CUBB can be used to evaluate the performance of PPS mode. Moreover, the ground truth of CUBB station is stored in the `GINav\data\data_cu\cubb_pos_ref.mat`. You can use the corresponding configuration file in `GINav\conf\` folder to perform this dataset, and plot the position error using GINavPlot. <br>
## Mathematical model <br>
Please refer to the GINav manual. <br>
## Acknowledgement <br>
First of all, I pay tribute to Mr. Tomoji Tkasu, the author of RTKLIB software. I admire him for his selfless open-source spirit and elegant programming. The most functions of GINav are refer to RTKLIB. The software is also referring to the PSINS software of Gongmin Yan from Northwestern Polytechnic University, the PPPLib software of Chao Chen from China University of Mining and Technology, the GAMP software of Feng Zhou from Shangdong University of Science and Technology. GINav uses the LAMBDA v3.0 toolbox from Curtin University and some open-source datasets. Thanks to the authors of above software, [Curtin GNSS Research Centre](http://gnss.curtin.edu.au/), and sharer of UrbanNavdataset. Many thanks are due to Steve Hillia from Notional Oceanic and Atmospheric Administration for his detailed suggestions. <br>
## Contact author <br>
Any suggestions, corrections, and comments about GINav are sincerely welcomed and should be sent to: <br>
Author: Kai Chen <br>
E-mail: kaichen@cumt.edu.cn <br>
Address: School of Environment and Geo-informatics, China University of Mining and Technology <br>
