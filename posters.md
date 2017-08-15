## Poster Contributions

Please note that some contributions are still pending


### Image based classification using CNN for stroke detection
L. Herzog (UZH), E. Murina (ZHAW), S. Wegener (USZ), B. Sick(UZH, ZHAW)


#### Abstract
**Background:** Strokes are worldwide the second frequent cause of death. They mainly manifest as ischemic strokes which are diagnosed by using magnetic resonance imaging (MRI) techniques. Automatic detection of strokes can speed up the decision making process about interventions and treatment in clinical practice which is essential for a beneficial patient outcome.

**Objective:** In this project we aim to predict if a patient is experiencing a stroke based on a set of diffusion weighted magnetic resonance images (DWI’s).

**Methods:** For each patient there is a set of grey-scaled DW-images which can be considered as horizontal slices through the brain obtained from top down at different positions of the head. We developed a baseline Convolutional Neural Network whose architecture is inspired by the VGG nets expecting 3 channel images.
In a first step we used one image for outcome prediction by repeating the respective image over the three channels (baseline model). In a second and a third approach we take the hierarchical structure of the data into account. The image of interest is read into the second channel, the image above into the first and the image below in the third channel (structured model). In the third approach we use again three consecutive images which are forwarded simultaneously through three convolutional parts. Afterwards, the resulting fully connected layers are connected (parallel model).
The models are trained from scratch using the Adam algorithm. Batch normalization, dropout and augmentation were used to further improve the outcome.
Dropout is also used at test time to obtain multiple prediction values for an image which are combined in an appropriate way. To obtain a prediction for each patient, we use the maximum of the image based prediction values. A decision tree is applied to get a threshold for classification. If the highest prediction value is above the threshold a patient is considered to experience a stroke.

**Results:** A total of 304 patients (190 stroke and 114 non-stroke) and 10351 corresponding images are considered of which 2985 display a stroke and 7366 no stroke. On the image level, the baseline model achieves the best specificity with 99.3% while the parallel model achieves the best sensitivity with 80.42%. On the patient level, the parallel model shows the best outcomes with a sensitivity of 100% and a specificity of 95%.
Conclusion: We developed three models which provide good prediction results in stroke detection. Taking the hierarchical structure into account seemed to improve the outcome slightly but this has to be further investigated.

### Automatic detection and localization of intracranial aneurysms by means of deep learning.

<SmallText>
Kazuhiro Watanabe^{1,2} 
Norman Juchler^{2,3} 
Hitomi Anzai4 Makoto Ohta^{5}
Sven Hirsch^{2}
</SmallText>

Affiliations:
1 Graduate School of Biomedical Engineering, Tohoku University, Sendai, Japan
2 Institute of Applied Sciences, ZHAW, Waedenswil, Zurich
3 Institute of Physiology, University of Zurich, Zurich
4 Frontier Research Institute for Interdisciplinary Sciences, Tohoku University, Sendai, Japan
5 Institute of Fluid Science, Tohoku University, Sendai, Japan

#### Abstract
Intracranial aneurysms are focal malformations of cerebral arteries that indicate regions on the arterial wall with an increased risk of rupture, often causing severe brain damage or even death. On the search for patterns in the morphology and hemodynamic flow structure that may be relevant for the outcome prediction and clinical decision making, we aim at analyzing large amounts of MR and CT angiographies (several thousands). For this purpose, an automated detection and isolation system for aneurysms in 3D medical imaging data is required. In these days, deep learning proved to be a powerful tool to process large amounts of image data and to reveal underlying patterns in the data. However, due to the lack of standardization of medical imaging protocols and the following difficulty of accurate segmentation of lesioned parts from monochromatic 2D images, the design of a deep learning algorithm could be a delicate task. In our contribution, we present our approach to these problems.


### D-MAC : DNN powered Medical-Audio Compiler
Ketaki Joshi (NVIDEA)

#### Abstract

In recent years, outsourcing of medical transcription has significantly increased. The proposed solution is a completely objective technique that reduces human effort and errors due to human intervention.

Subjective transcription is affected by known issues like disparity, delays or incoherent audio recordings. But one of the critical issues that goes unnoticed is the transcriber’s native language might be different from the doctor dictating in the recording. Hence, it sometimes becomes difficult for the transcribers to decode the accent. This leads to misinterpretations and wrong data being written.

The existing solutions are partially-automated. They focus on the known issues of disparities and delays and ignores this critical issue. Also, they mostly use prevalent speech to text solutions (not all are enabled with deep learning) that are not tailor-made for medical field inputs. Hence, they often produce incorrect output. The final output of prevalent solutions is reviewed by the transcriber. This defeats the purpose of automating the process. Their response is used for training the network in case of solutions that use deep learning. Hence, the issue of accent misinterpretations can still occur. The transcript reviewers could still feed incorrect data due to misinterpretations and create an incorrect training set. Hence, the training of the network is done at the ‘incorrect-end’. Also, this increases the work of the doctors who must re-read the transcripts and correct the mistakes if any.

The proposed solution is a DNN powered medical-audio compiler(MAC). Analogous to the generic compiler structure, the front end of the D-MAC framework has custom lexical and semantic analyzer for whom the dictionary is created with training sets comprising of solely medical linguistics. i.e. not a generic data base like prevalent solutions. This is the first layer of the neural network. The scanner created tokens will be then ‘semantically analyzed’ to see if they fit the context. The pauses, delays etc. are eliminated. The semantic analysis rules are created with the contexts learnt from the training sets for different tokens and their permutations. This forms the underlying layer of the neural net. The back-end of D-MAC has a ‘text generator’ which generates a text output in specified format: text/tabular etc. Also, unlike prevalent solutions, the proposed technique targets the training to be done from the ‘correct’ end. i.e. if a doctor makes a correction in the transcript, the network learns this. Hence, reducing the number of errors overtime and completely automating the process.

Making the process completely objective reduces the errors caused by the existing subjective or partial-subjective alternatives. It also reduces the risk of breach of confidentiality of the audio files when they are outsourced. D-MAC fastens the process and can be maintained in-house by hospitals/healthcare professionals. i.e. no need of outsourcing at all.

### Fully Convolutional Neural Networks for Newspaper Article Segmentation
Benjamin Meier (ZHAW)

#### Abstract
Segmenting newspaper pages into articles that semantically belong together is a necessary prerequisite for article-based
information retrieval on print media collections like e.g. archives and libraries. It is challenging due to vastly differing layouts of papers, various content types and different languages, but commercially very relevant for e.g. media monitoring. We present a semantic segmentation approach based on the visual appearance of each page. We apply a fully convolutional neural network (FCN) that we train in an end-to-end fashion to transform the input image into a segmentation mask in one pass. We show experimentally that the FCN performs very well: it outperforms a deep learning-based commercial solution by a large margin in terms of segmentation quality while in addition being computationally two orders of magnitude more efficient.
 
### Deep Learning for classification of Non-Small Cell Lung Cancer histologic subtypes 
Elvis Murina (ZHAW),Ruben Casanova (USZ),  Martina Haberecker (USZ), Hanna Honcharova-Biletska (USZ), Bart Vrugt (USZ), Alex Soltermann(USZ) ,Beate Sick (ZHAW), Oliver Dürr(ZHAW)

#### Abstract 
Non-small cell lung cancer (NSCLC) is the most common type of lung cancer. Adenocarcinoma (ADC) and squamous cell carcinoma (LSCC), the two main subtypes. ADC and LSCLC can be often distinguished by trained pathologists based on formation of glands in ADC or by the presence of keratin and/or intercellular desmosomes for LSCC which can be identified by visually checking histologic slides in an optical microscope. In clinical practice, histologic subtyping is an important factor for treatment decisions, as different therapies are proposed to non-squamous NSCLC due to higher toxicity or reduced efficacy in LSCC.

We have developed a CNN to differentiate ADC from LSCC on a cohort consisting of 208 NSCLC patients. Patients cohorts were split into a training set (n=140 patients) and validation set (n=68). The performances of the CNN were evaluated on the validation set and are compared with the results of three experienced pathologists. In addition we have used a pretrained CNN of ImageNet for unsupervised feature extraction of the images and show results of 2D representations allowing for subgroup identification without relying on any expert labels.





