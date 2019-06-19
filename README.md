# QC-STORM
QC-STORM is an online processing plugin (Micro-Manager & ImageJ) for super-resolution localization imaging with large FOV. At single-molecule fitting mode, QC-STORM is able to process the imaging data generated by sCMOS camera at full FOV and fastest frame rate (2048 x 2048 pixels x 100 fps). Even at high density activation and multi-emitter fitting mode, QC-STORM is able to process images with 1024 x 1024 pixels at 100 fps.

# Key features

Ultrahigh efficient MLE localization: online processing for sCMOS camera based localization microscopy at full FOV and fastest frame rate without sacrificing localization precision (localization speed > 8x10^6 for 7x7 pixels ROI based on Gigabyte GeForce GTX 1080 Ti Gaming OC 11GB Graphic Cards). 

Ultrahigh efficient MLE localization.

Most processing parts of QC-STORM are GPU accelerated, and their performance increase almost linearly with GPU’s single floating performance (GFLOPS). Note the speed value could be measured low with small and low activation density image, and the speed may also be reduced by low CPU memory bandwidth and low speed image reading from hard disk.

The localization performance evaluation are available at previous work of Sage, Daniel, et al. "Super-resolution fight club: A broad assessment of 2D & 3D single-molecule localization microscopy software." bioRxiv (2018): 362517.

MLE Localization type: 2D, Astigmatism 3D

Online super-resolution image rendering and statistical information analyzing (photon number, background intensity, SNR, PSF width, localization density, on time)

Online localization precision (CRLB) calculation

Drift correction by cross-correlation (post-processing)

Merging molecules emitting in consecutive frames (localization precision weighted average)

Online feedback control for localization density stabilizing and axial drift correction (hardware dependent)

Sequential Multi-FOV acquisition (hardware dependent)

Configuration parameters remembering, saving and loading

The open dataset evaluation of QC-STORM can be found in http://bigwww.epfl.ch/smlm/challenge2016/index.html using name QC-STORM-2019. Note the evaluation of QC-STORM in recently published paper "Super-resolution fight club: assessment of 2D and 3D single-molecule localization microscopy software" is based on submission in 2017, and the results were only processed by single-molecule localization. Moreover, the double-helix localization mode was removed in current version.


# System requirements and installation
1, Windows 7 sp1 or newer, x64.

2, NVidia CUDA enabled GPU with compute capability no less than 3.5.

**Note: please upgrade your GPU driver to the newest (https://www.geforce.com/drivers , Compatible Driver Versions >= 411.31) or the plugin can't work successfully.**

3, ImageJ/Fiji, Micro-Manager 2.0 (beta or gamma). 
**Note: please set at least 4 GB memory buffer for ImageJ, Micro-Manager and ImageJ of Micro-Manager.**

4, Download and install Microsoft Visual C++ 2015 Redistributable Update 3 (x64) (https://www.microsoft.com/en-us/download/details.aspx?id=53587). You may need to uninstall Visual C++ 2017 Redistributable first.

5, Download newest QC-STORM release from https://github.com/SRMLabHUST/QC-STORM/releases.

6, Copy the downloaded .dll files into installation directory of ImageJ or Micro-Manager, and .jar files into "plugins" or "mmplugins" folder for ImageJ and Micro-Manager respectively.

7, Note: QC-STORM only supports English file name / path.


# Recompile the source codes
1, The Java GUI for ImageJ (v1.52g) and Micro-Manager beta (MMSetup_64bit_2.0.0-beta3 from nightly builds of Micro-Manager 2.0) are developed by NetBeans IDE 7.3.1 with Java jdk1.6.0_45. The Java GUI for Micro-Manager gamma are developed by NetBeans IDE 10.0 with Java jdk1.8.0_201.

2, The C++ core image processing algorithms are developed by Visual Studio 2015 Update 3, and accelerated by NVidia CUDA 10.0.

3, Download the codes, open the projects by corresponding software and recompile the codes.

4, Program framework of QC-STORM:

![](https://github.com/SRMLabHUST/QC-STORM/blob/master/QC-STORM%20program%20framework.png)

# Declaration
This program is free software: you can redistribute it and/or modify it under the terms of the GNU LESSER GENERAL PUBLIC LICENSE as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU LESSER GENERAL PUBLIC LICENSE for more details.

You should have received a copy of the GNU LESSER GENERAL PUBLIC LICENSE along with this program.  If not, see <https://www.gnu.org/licenses/>.

For more questions, please contact Prof. Zhenli-Huang at "leo@mail.hust.edu.cn" or author Luchang Li at "luchangli1993@163.com".
