# Distance Sperated Automatic Labeled LiDAR Data for Human detection

Distance Sperated Automatic Labeled LiDAR Data are novel data with human label. The data contain various generated LiDAR scenes with human label. To download the data, please check your free disk space enough and run 'DownloadAndUnzip.sh'. You can also download the data by the following url.

* HumanDetectionVer02 (377GB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/HumanDetectionVer02.tar.gz
* TestsetForVer02 (851MB) : https://data.airc.aist.go.jp/AutomaticLabeledLiDARData/TestsetForVer02.tar.gz
  
The paper of Distance Sperated Automatic Labeled LiDAR Data :  
 **Wonjik Kim, Masayuki Tanaka, Masatoshi Okutomi, Yoko Sasaki, "Automatic Labeled LiDAR Data Generation and Distance-Based Ensemble Learning for Human Segmentation", IEEE Access, 2019.** ([link](https://ieeexplore.ieee.org/document/8703723))

---
# How to use
### Dependencies
* Python 3.6.5
* Tensorflow 1.9.0
* Keras 2.2.4
* Cuda 9.0

### Run DownloadAndUnzip.sh
In your own directory, please run the following command in terminal.
<br>
> bash ./DownloadAndUnzip.sh 

### Sample code
In directory of './TestsetForVer02/Testcode', you can see sample code for performance evaluation. When you want to check sample code, please run the following command in that directory.
<br>
> python Testgauss_Real(or Sim).py 

---
### Directory Specification

* HumanDetectionVer02
    * Data
        * 01to10 : Dataset 01to10
            * h5file : *containing 100.8K hdf5 files*
            * xml : *containing 100.8K xml files*
        * 05to15 : Dataset 05to15
            * h5file : *containing 100.8K hdf5 files*
            * xml : *containing 100.8K xml files*
        * 10to20 : Dataset 10to20
            * h5file : *containing 100.8K hdf5 files*
            * xml : *containing 100.8K xml files*
        * 15to25 : Dataset 15to25
            * h5file : *containing 100.8K hdf5 files*
            * xml : *containing 100.8K xml files*
        * 20to30 : Dataset 20to30
            * h5file : *containing 100.8K hdf5 files*
            * xml : *containing 100.8K xml files*

* TestsetForVer02
    * Testcode
        * fcn-depth-01to10.hdf5 : *trained weight of fcn by depth with dataset 01to10*
        * fcn-depth-05to15.hdf5 : *trained weight of fcn by depth with dataset 05to15*
        * fcn-depth-10to20.hdf5 : *trained weight of fcn by depth with dataset 10to20*
        * fcn-depth-15to25.hdf5 : *trained weight of fcn by depth with dataset 15to25*
        * fcn-depth-20to30.hdf5 : *trained weight of fcn by depth with dataset 20to30*
        * fcn.py : *fcn architecture*
        * mtinitializers.py
        * mtutil.py
        * padding.py
        * Testgauss_Real.py : *sample code for test with real data*
        * Testgauss_Sim.py : *sample code for test with simulation data*
    * Dataset
        * Real
            * 0.1K hdf5 files
        * Sim
            * 0.5K hdf5 files

---
# License
Automatic Labeled LiDAR Data Ver.02 are allowed only for noncommercial usage. Please cite our paper if our data were used in your work.
You can see specific terms of use in the LICENSE.md.

