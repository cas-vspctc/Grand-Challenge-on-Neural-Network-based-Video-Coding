<script type="text/javascript"
  src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

# Grand-Challenge-on-Neural-Network-based-Video-Coding
Grand Challenge on Neural Network-based Video Coding from CAS-VSPCTC

## Abstract:
Recently, there is an increasing interest in the neural network-based video coding, including end-to-end and hybrid schemes. To foster the research in this emerging field and provide a benchmark, we propose this Grand Challenge (GC). In this GC, different neural network-based coding schemes will be evaluated according to their coding efficiency and innovations in methodologies. Two tracks will be evaluated, including the hybrid and end-to-end solutions. In the hybrid solutions, deep network-based coding tools shall be used with traditional video coding schemes. In the end-to-end solutions, the whole video codec system shall be built primarily upon deep networks. Participants are highly recommended to submit their papers to sub-track X under Track 15 and present their proposals at ISCAS 2022. Note that this sub-track is only open to authors who express their interest to participate in the Grand Challenge on Neural Network-based Video Coding by Sep. 30, 2021.

## Rationale:
In recent years, deep learning-based image/video coding schemes have achieved remarkable progress. As two representative approaches, hybrid solutions and end-to-end solutions have both been investigated extensively. The hybrid solution adopts deep network-based coding tools to enhance traditional video coding schemes while the end-to-end solution builds the whole compression scheme based on deep networks. In spite of the great advancement of these solutions, there are still numerous challenges remaining to be addressed, e.g.: 1) how to harmonize a deep coding tool with a hybrid video codec, e.g. how to take compression into consideration when developing a deep tool for pre-processing; 2) how to exploit long-term temporal dependency in an end-to-end framework for video coding; 3) how to leverage automated machine learning-based network architectures optimization for higher coding efficiency; 4) how to perform efficient bit allocation with deep learning frameworks; 5) how to achieve the global minimum in rate-distortion trade-offs, e.g. to take the impact of the current step on later frames into account, possibly by using reinforcement learning; and 6) how to achieve better complexity-performance trade-offs. In view of these challenges, several activities towards improving deep-learning-based image/video coding schemes have been initiated. For example, there are a special section on *"Learning-based Image and Video Compression"* in TCSVT, July 2020, a special section on *"Optimized Image/Video Coding Based on Deep Learning"* in OJCAS, Dec. 2021, and the *"Challenge on Learned Image Compression (CLIC)"* in CVPR, which has been organized annually since 2018. In hopes of encouraging more innovative contributions towards resolving the aforementioned challenges in the ISCAS community, we propose this grand challenge. 

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
2.	$PSNR (6\*PSNR_Y + PSNR_U + PSNR_V)/8$ will be used to evaluate the distortion of the decoded pictures.
3.	Average Bjøntegaard delta bitrates (BDR) calculated using [1] for all test sequences will be gathered to compare the coding efficiency.
4.	An anchor of HM 16.22 [2] coded with QPs = {22, 27, 32, 37} under random access configuration defined in the HM common test conditions [3] will be provided. The released anchor data will include the bit-rates corresponding to the four QPs for each sequence. It is required that the proposed method should generate four bit-streams for each sequence, targeting the anchor bit-rates corresponding to the four QPs. Additional constraints are listed as follows:

a.	For each sequence, the range of four real bit-rates shall be [90% * the lowest anchor bit-rate, 110% * the highest anchor bit-rate].
b.	Only one single decoder shall be utilized to decode all the bitstreams. 
c.	The intra period in the proposed submission shall be no larger than that used by the anchor in generating the validation and test sequences.
Proposed documents
A docker container with the executable scheme must be submitted for results generation and cross-check. Each participant will be invited to submit a paper, which must describe the following items in detail. 
o.	The methodology;
o.	The training data set;
o.	Detailed rate-distortion data (Comparison with the provided anchor is encouraged). 
Complexity analysis of the proposed solutions is encouraged for the paper submission.

### Important Dates

|Date|Event|
|--|--|
|Sep. $30^th$, 2021|Participants express interest in participation by sending an email to the organizer Dr. Yue Li (yue.li@bytedance.com)|
|Oct. 8^th^, 2021|The organizers release the validation set as well as the corresponding test information (e.g., frame rates and intra periods) and template for performance reporting (with rate-distortion points for the validation set)|
|Nov. 8^th^, 2021|Deadline of paper submission (to be aligned with Special Sessions in case of extension) for participants|
|Nov. 22^th^, 2021|Participants upload docker container wherein only one single decoder shall be utilized for the decoding of all the bitstreams|
|Nov. 26^th^, 2021|The organizers release the test sequences (including frame rate, corresponding rate-distortion points, etc.)|
|Dec. 15^th^, 2021|Participants upload compressed bitstreams and decoded YUV files|
|Dec. 28^th^, 2021|Deadline of fact sheets submission for participants|
|Jan. 14^th^, 2021|Paper acceptance notification|
|Feb. 5^th^, 2021|Camera-ready paper submission deadline|
|TBA|Paper presentation within Track 11.2 on “Learning-based Image/Video Coding”|
|TBA|Awards announcement (at the ISCAS 2022 banquet)|

### Awards
ByteDance will sponsor the awards of this grand challenge. Three categorizes of awards are expected to be presented. Two top-performance awards will be granted according to the performance, for the hybrid track and the end-to-end track, respectively. In addition, to foster the innovation, a top-creativity award will be given to the most inspiring scheme recommended by a committee group and it is only applicable to authors with their corresponding papers accepted by ISCAS 2022.


## References
[1].	G. Bjøntegaard, “Calculation of average PSNR differences between RD-Curves,” ITUT SG16/Q6, Doc. VCEG-M33, Austin, Apr. 2001.
[2].	https://vcgit.hhi.fraunhofer.de/jvet/HM/-/tree/HM-16.22
[3].	Common Test Conditions and Software Reference Configurations for HM (JCTVC-L1100)

## Organizer Biographies:
 **Li** Zhang received the Ph.D. degree in computer science from the Institute of Computing Technology, Chinese Academy of Sciences, Beijing, China, in 2009. From 2009 to 2011, she held a post-doctoral position at the Institute of Digital Media, Peking University, Beijing. From 2011 to 2018, she was a Senior Staff Engineer at Qualcomm, Inc., San Diego, CA, USA. She is currently the Head of Advanced Video Group, Bytedance Inc., San Diego, CA, USA. Her research interests include 2D/3D image/video coding, video processing, and transmission. She was a Software Coordinator for Audio and Video Coding Standard (AVS) and the 3D extensions of High Efficiency Video Coding (HEVC). She has authored 450+ standardization contributions, 170+ granted US patents, 90+ technical articles in related book chapters, journals, and proceedings in image/video coding and video processing. She has been an active contributor to the Versatile Video Coding (VVC), Advanced AVS, the IEEE 1857, 3D Video (3DV) coding extensions of H.264/AVC and HEVC, and HEVC screen content coding extensions. During the development of those video coding standards, she co-chaired several ad hoc groups and core experiments. She has been appointed as an Editor of AVS, the Main Editor of the Software Test Model for 3DV Standards. She organized/co-chaired multiple special sessions and grand challenges at various conferences.

**Jizheng Xu** received the Ph.D. degree in electrical engineering from Shanghai Jiaotong University, China in 2011. He joined Microsoft Research Asia in 2003 and served as a Research Manager and joined ByteDance multimedia lab as a Research Scientist in 2018. He has authored and co-authored over 140 refereed conference and journal refereed papers. His research interests include image and visual signal representation, image/video compression and communication, computer vision and deep learning. He has been an active contributor to ISO/MPEG and ITU-T video coding standards, including H.264/AVC, H.265/HEVC and VVC/H.266. He initiated the screen content coding in H.265/HEVC and was a major technical contributor. He chaired and co-chaired the ad-hoc group of exploration on wavelet video coding in MPEG, and various technical ad-hoc groups in JCT-VC, e.g., on screen content coding, on parsing robustness, on lossless coding. He was an Associate Editor for the IEEE Transactions on Circuits and Systems for Video Technology from 2018 to 2020. He served as a Guest Editor for the special issue on Screen Content Video Coding and Applications of the IEEE Journal on Emerging and Selected Topics in Circuits and Systems in 2016. He co-organized and co-chaired special sessions on scalable video coding, directional transform, high quality video coding at various conferences.

**Kai Zhang** received the B.S. degree in computer science from Nankai University, Tianjin, China, in 2004. In 2011, he received the Ph.D. degree in computer science from the Institute of Computing Technology, Chinese Academy of Sciences, Beijing, China. From 2011 to 2012, he worked as a researcher in Tencent Inc. Beijing, China. From 2012 to 2016, he worked as a technical manager then a team manager in Mediatek Inc. Beijing, China, leading a research team to propose novel technologies to emerging video coding standards. In 2016, he joined Qualcomm Inc. San Diego, CA. Since 2018, he has been doing research work on video coding as a senior research scientist in Bytedance Inc. San Diego, CA. Dr. Zhang’ research interests include video/image compression, coding, processing and communication, especially video coding standardization. In 2006, he proposed his first proposal to JVT. From then, he has contributed more than 300 proposals to JVT, VCEG, JCT-VC, JCT-3V, JVET and AVS team, covering many important aspects of major standards such as H.264/AVC SVC extension, HEVC, 3D-HEVC, VVC and AVS. During the development of VVC, Dr. Zhang co-chaired several core experiments and branch of groups. Currently, Dr. Zhang serves as a coordinator of the reference software known as ECM in JVET, to explore video coding technologies beyond VVC. Dr. Zhang has 300+ granted or pending U.S. patents applications, which are mostly essential to popular video coding standards. Dr. Zhang has authored/co-authored 30+ papers on well-known journals/conferences such as T-IP, T-CSVT, T-B, JETCAS, ICIP, ISCAS, etc. Dr. Zhang also serves as a reviewer for those journals/conferences.

**Yue Li** received the B.S. and Ph.D. degrees in electronic engineering from the University of Science and Technology of China, Hefei, China, in 2014 and 2019, respectively. He is currently a Research Scientist with Bytedance Multimedia Lab, San Diego, CA, USA. His research interests include image/video coding and processing. He has authored 10+ neural network-based standardization contributions to the Versatile Video Coding (VVC). He has authored/co-authored 15+ papers on well-known journals/conferences such as T-IP, T-CSVT, CSUR, ICIP, ICME, DCC, etc. He also serves as a reviewer for those journals/conferences.
