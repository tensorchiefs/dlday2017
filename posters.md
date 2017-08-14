## Poster Contributions

### Image based classification using CNN for stroke detection
L. Herzog^{1}, E. Murina^{2}, S. Wegener^{1}, B. Sick^{1,2}

1. UZH
2. ZHAW

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

#### Abstract
Provided soon

### D-MAC : DNN powered Medical-Audio Compiler
Ketaki Joshi (NVIDEA)

#### Abstract

In recent years, outsourcing of medical transcription has significantly increased. The proposed solution is a completely objective technique that reduces human effort and errors due to human intervention.

Subjective transcription is affected by known issues like disparity, delays or incoherent audio recordings. But one of the critical issues that goes unnoticed is the transcriber’s native language might be different from the doctor dictating in the recording. Hence, it sometimes becomes difficult for the transcribers to decode the accent. This leads to misinterpretations and wrong data being written.

The existing solutions are partially-automated. They focus on the known issues of disparities and delays and ignores this critical issue. Also, they mostly use prevalent speech to text solutions (not all are enabled with deep learning) that are not tailor-made for medical field inputs. Hence, they often produce incorrect output. The final output of prevalent solutions is reviewed by the transcriber. This defeats the purpose of automating the process. Their response is used for training the network in case of solutions that use deep learning. Hence, the issue of accent misinterpretations can still occur. The transcript reviewers could still feed incorrect data due to misinterpretations and create an incorrect training set. Hence, the training of the network is done at the ‘incorrect-end’. Also, this increases the work of the doctors who must re-read the transcripts and correct the mistakes if any.

The proposed solution is a DNN powered medical-audio compiler(MAC). Analogous to the generic compiler structure, the front end of the D-MAC framework has custom lexical and semantic analyzer for whom the dictionary is created with training sets comprising of solely medical linguistics. i.e. not a generic data base like prevalent solutions. This is the first layer of the neural network. The scanner created tokens will be then ‘semantically analyzed’ to see if they fit the context. The pauses, delays etc. are eliminated. The semantic analysis rules are created with the contexts learnt from the training sets for different tokens and their permutations. This forms the underlying layer of the neural net. The back-end of D-MAC has a ‘text generator’ which generates a text output in specified format: text/tabular etc. Also, unlike prevalent solutions, the proposed technique targets the training to be done from the ‘correct’ end. i.e. if a doctor makes a correction in the transcript, the network learns this. Hence, reducing the number of errors overtime and completely automating the process.

Making the process completely objective reduces the errors caused by the existing subjective or partial-subjective alternatives. It also reduces the risk of breach of confidentiality of the audio files when they are outsourced. D-MAC fastens the process and can be maintained in-house by hospitals/healthcare professionals. i.e. no need of outsourcing at all.

