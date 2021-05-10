# EQQST

Welcome to the EQSST Dataset

## Introduction

Subjective tests for the assessment of the quality of experience (QoE) are typically run with a pool of subjects providing their opinion scores using a 5-point scale. The subjects’ mean opinion score (MOS) is generally assumed as the best estimation of the average score in the target population. Indeed, for a large enough sample, we may assume that the mean of the variations across the subjects approaches zero, but this is not thecase for the limited number of subjects typically considered in subjective tests. In our paper titled "[Estimation of Quality Scores from Subjective Tests - beyond Subjects’ MOS](https://ieeexplore.ieee.org/document/9154548)" we propose an approach based on generalized linear models (GLMs) for estimation of the population average QoE. The approach recognizes the multinomial nature of the data and allows for correlation between scores of the same subject. The resulting estimated average QoE is shown to follow more credible patterns than the MOS, particularly for higher bitrates, for which the model estimates present more coherent behavior. 

The software that implements the model is made publicly available to enable reproducible results and application of the model to different datasets. In addition, we also present the results of the individual scores assigned by 25 subjects to a set of gaming videos evaluated under different resolutions and compression ratios of the already publicly available gaming video dataset, GamingVideoSET which can be accessed using the following link: https://kingston.box.com/v/GamingVideoSET. 

# Download

Please email Nabajeet Barman at `n.barman@ieee.org` to obtain the password to access the database. 

In case of any queries, please contact any of the authors below: 

    Sergio Pezzulli (`sergio.pezzulli@uniroma1.it`) - University of Rome La Sapienza, Italy

    Maria G. Martini ( `m.martini@kingston.ac.uk`) - Kingston University, London, U.K.

    Nabajeet Barman (`n.barman4@gmail.com`) – Kingston University, London, U.K.

# Details of the Database

The zip folder, `EQSSTDataset.zip` consists of the following files:

## (1) GamingVideoSET-SubjectiveTestResults_IndividualOpinionScores.xlsx: 
Individual test participant scores for each PVS is provided in the file.

P1, P2, P3 and so on represent the subjects
VideoName: Name of the Distorted video sequences. The nomenclature is as follows.

    "Name_30fps_30sec_v2_Res_BR_x264.mp4", where
    Name: Name of the game
    Res: is the resolution of the video (1920x1080 or 1280x720 or 640x480)
    BT: is the encoding bitrate in kbps
    x264 to represent that H.264/MPEG-AVC encoding standard was used.

For more details, please refer to GamingVideoSET available at https://kingston.box.com/v/GamingVideoSET.

## (2) Code.xlsx: 

We show the code implemented in the statistical package SAS (Statistical Analysis Software), version 9.4.

In particular, the following code is for:
	- data input, based on the SAS procedure DATA.
	- Model selection, based on the procedures LOGISTIC and GENMOD.
	- Selection of the correlation structure and fitting via generalized estimating equations, based on the procedure GEE.  

The data needs to be read in two different ways. 
In fact, while proc. GENMOD and GEE read the data in form of strings of the individual scores, proc LOGISTIC needs data in form of frequencies (e.g., for each sequence, how many individuals scored 1, 2, ..., 5).

# Copyright
-----------COPYRIGHT NOTICE STARTS WITH THIS LINE------------ 

Copyright (c) 2020 Kingston University, London
All rights reserved. 
Permission is hereby granted, without written agreement and without license or royalty fees, to use, copy, modify, and distribute this dataset and its documentation for any purpose, provided that the copyright notice in its entirety appear in all copies of this database, and the original source of this database, KINGSTON UNIVERSITY, LONDON is acknowledged in any publication that reports research using this database.

We are making this dataset available to the research community free of charge. If you use this dataset (or parts of it) in your research, we kindly ask that you to cite our paper listed below:

	`S. Pezzulli, M. G. Martini and N. Barman, "Estimation of Quality Scores from Subjective Tests - beyond Subjects' MOS," in IEEE Transactions on Multimedia, doi: 10.1109/TMM.2020.3013349.`
 
IN NO EVENT SHALL THE KINGSTON UNIVERSITY BE LIABLE TO ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OF THIS DATABASE AND ITS DOCUMENTATION, EVEN IF THE KINGSTON UNIVERSITY, LONDON HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. 

THE KINGSTON UNIVERSITY, LONDON SPECIFICALLY DISCLAIM ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE DATABASE PROVIDED HEREUNDER IS ON AN "AS IS" BASIS, AND THE KINGSTON UNIVERSITY, LONDON HAS NO OBLIGATION TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.

-----------COPYRIGHT NOTICE ENDS WITH THIS LINE------------

## Note

The dataset originally referenced in the paper is available on Google drive [here](https://drive.google.com/drive/folders/10xd7Wj3-r9BpsGxEO9rEgbQkNAYXon_k). This Github repository consists of the same dataset files as originally made available in the paper.
