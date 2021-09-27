# Grand-Challenge-on-Neural-Network-based-Video-Coding
Grand Challenge on Neural Network-based Video Coding from CAS-VSPCTC

## Abstract:
Recently, there is an increasing interest in the neural network-based video coding, including end-to-end and hybrid schemes. To foster the research in this emerging field and provide a benchmark, we propose this Grand Challenge (GC). In this GC, different neural network-based coding schemes will be evaluated according to their coding efficiency and innovations in methodologies. Two tracks will be evaluated, including the hybrid and end-to-end solutions. In the hybrid solutions, deep network-based coding tools shall be used with traditional video coding schemes. In the end-to-end solutions, the whole video codec system shall be built primarily upon deep networks. Participants are highly recommended to submit their papers to sub-track X under Track 15 and present their proposals at ISCAS 2022. Note that this sub-track is only open to authors who express their interest to participate in the Grand Challenge on Neural Network-based Video Coding by Sep. 30, 2021.

## Rationale:
In recent years, deep learning-based image/video coding schemes have achieved remarkable progress. As two representative approaches, hybrid solutions and end-to-end solutions have both been investigated extensively. The hybrid solution adopts deep network-based coding tools to enhance traditional video coding schemes while the end-to-end solution builds the whole compression scheme based on deep networks. In spite of the great advancement of these solutions, there are still numerous challenges remaining to be addressed, e.g.: 1) how to harmonize a deep coding tool with a hybrid video codec, e.g. how to take compression into consideration when developing a deep tool for pre-processing; 2) how to exploit long-term temporal dependency in an end-to-end framework for video coding; 3) how to leverage automated machine learning-based network architectures optimization for higher coding efficiency; 4) how to perform efficient bit allocation with deep learning frameworks; 5) how to achieve the global minimum in rate-distortion trade-offs, e.g. to take the impact of the current step on later frames into account, possibly by using reinforcement learning; and 6) how to achieve better complexity-performance trade-offs. In view of these challenges, several activities towards improving deep-learning-based image/video coding schemes have been initiated. For example, there are a special section on "Learning-based Image and Video Compression" in TCSVT, July 2020, a special section on "Optimized Image/Video Coding Based on Deep Learning " in OJCAS, Dec. 2021, and the "Challenge on Learned Image Compression (CLIC)" in CVPR, which has been organized annually since 2018. In hopes of encouraging more innovative contributions towards resolving the aforementioned challenges in the ISCAS community, we propose this grand challenge. 

## Requirements, Evaluation, Timeline and Awards
### Training Data Set
It is recommended to use the following training data.
1.	UVG dataset, http://ultravideo.cs.tut.fi/
2.	CDVL dataset, https://cdvl.org/
Additional training data are also allowed to be used given that they are described in the submitted document.

### Test Specifications
In the test, the proposals will be evaluated on multiple YUV 4:2:0 test sequences in the resolution of 1920x1080. There is no constraint on the reference structure. Note that the neural network must be used in the decoding process..

### Evaluation Criteria
The test sequences will be released according to the timeline in Table 1 and the results will be evaluated with the following criteria:
1.	The decoded sequences will be evaluated in 4:2:0 color format. 
2.	PSNR (6*PSNRY + PSNRU + PSNRV)/8 will be used to evaluate the distortion of the decoded pictures.
3.	Average Bjøntegaard delta bitrates (BDR) calculated using [1] for all test sequences will be gathered to compare the coding efficiency.
4.	An anchor of HM 16.22 [2] coded with QPs = {22, 27, 32, 37} under random access configuration defined in the HM common test conditions [3] will be provided. The released anchor data will include the bit-rates corresponding to the four QPs for each sequence. It is required that the proposed method should generate four bit-streams for each sequence, targeting the anchor bit-rates corresponding to the four QPs. Additional constraints are listed as follows:
a.	For each sequence, the range of four real bit-rates shall be [90% * the lowest anchor bit-rate, 110% * the highest anchor bit-rate].
b.	Only one single decoder shall be utilized to decode all the bitstreams. 
c.	The intra period in the proposed submission shall be no larger than that used by the anchor in generating the validation and test sequences.
Proposed documents
A docker container with the executable scheme must be submitted for results generation and cross-check. Each participant will be invited to submit a paper, which must describe the following items in detail. 
o	The methodology;
o	The training data set;
o	Detailed rate-distortion data (Comparison with the provided anchor is encouraged). 
Complexity analysis of the proposed solutions is encouraged for the paper submission.
