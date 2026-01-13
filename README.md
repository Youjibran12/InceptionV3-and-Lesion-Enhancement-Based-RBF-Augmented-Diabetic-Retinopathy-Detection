**Introduction:**
Diabetic retinopathy (a complication of Diabetes Mellitus)
which is considered to be one of the most severe eye condition
is a major cause of blindness. According to the trending
reports approximately 12 million people in India suffers
from any grade of diabetic retinopathy, with about 4 million
people having this life-threating disease. It happens when
the excessive glucose in the vessels of retina gets damaged
ultimately leading to leakage, swelling and permanent loss of
vision. This condition can be prevailed if detected early, but
however due to lack of access of ophthalmologists in some
areas and people having less knowledge about this condition
makes it even more difficult. Also manual screening, costs
and treating the disease within the time are one of the major
areas to be worked upon.The traditional screening methods
are also prone to human error. To avoid human error and
for better results CAD (Computer Aided Design) came into
the picture providing more reliable and faster detection of
Diabetic Retinopathy (DR). As science and technology progressed
hand-in-hand CNN (Convolutional Neural Networks)
gave major breakthroughs in the medical field mostly for
deep analysis. To further simply the process and to get more
accurate results we propose a model, InceptionV3 integrated
with RBF. InceptionV3 is a CNN architecture which will be
able to classify the stages of Diabetic Retinopathy. There are
five classes: No DR, Mild DR, Moderate DR, Severe DR and
Proliferative DR. In the proposed model the Softmax layer of
InceptionV3 is removed and another layer RBF (Radial Basis
Function) is trained to reduce over-fitting and to yield greater
accuracy. The dataset used for this purpose is the APTOS
dataset (having 3000 fundus images) which is divided into
three phases: Training, Validation and Testing. Furthermore
for pre-processing MS-DRLBP technique is applied so that
the lesions become clearly visible.

**Workflow Model:**
<img width="221" height="220" alt="image" src="https://github.com/user-attachments/assets/59ac7d00-d07f-4ecc-9485-1e015870b9c5" />


**Workflow Model Description:**
It starts with loading the necessary libraries and dependencies
and then the retinal fundus image dataset is loaded.
The images are then passed through a preprocessing phase,
which consists of size reduction to 512x512, adaptive gamma
correction, contrast enhancement methods such as CLAHE and
QE, texture feature extraction by using MS-DRLBP, lesion
masking by using Otsu thresholding with morphological operations.
After preprocessing, the workflow determines whether
it has been successful or not; otherwise, the process repeats
again to rectify the errors. Passed through a successful preprocessing
of images are extracted features through InceptionV3
embeddings, which produces deep features. The same features
are then sent to classification phase where fully connected (FC)
layer and RBF classifier are applied to classify the images
into various stages of diabetic retinopathy. The model is then
trained and validated to make sure that it is reliable and then
produces the classification output. The system then performs
an evaluation and metrics assessment (accuracy, sensitivity,
specificity, etc.) and the results are then visualized (heatmaps,
lesion overlays, etc.). Lastly the stage of generation of a
report is done which summarizes the diagnostic results to
be used by the clinicians and the process is finalized.The
comprehensive documentation standards will be put in place
to ensure that a project has detailed records of all design
decisions, parameters of the algorithm, validation or results
and the regulatory compliance requirements across the project
life cycle.

**Dataset used for the project is APTOS dataset.**
**Before and After Preprocessing images comparison:**
<img width="188" height="355" alt="image" src="https://github.com/user-attachments/assets/f19a9db5-cf48-4218-9634-0adcd1b04e85" />


**Conclusion:**
The project Automated diabetic retinopathy (DR) detection
system using deep learning and specialized lesion enhancement
techniques presents a reliable and efficient approach to
early diagnosis of diabetic retinography, which is critical for
detecting and preventing vision loss at the inception stages
itself.The proposed framework’s uniqueness lies in its effective
utilzation of adaptive preprocessing and a MS-DRLBP-based
lesion enhancement module, which is used to highlight the
key pathological signs of Diabetic Retinography i.e microaneurysms,
haemorrhages, and exudates within the images of
retinal fundus.These preprocessed images are then fed into a
complex deep learning architecture which utilizes InceptionV3
as its backbone for dynamic multi-scale feature extraction,it
is also combined with a custom Radial Basis Function (RBF)
classifier which ensures accurate classification across the five
stages of diabetic retinopathy.The model achieves a final test
accuracy of 81 percent which demonstrates the viability of this
approach. A thorough analysis of the report reveals that the
model is capable in identifying healthy retinas (Class 0) with a
high accuracy of 81 percent . However, the findings also lead
us to one of the main issues in medical AI i.e the imbalance
between classes .The Minority classes (1, 3, and 4) perform
much worse, which shows that there is a affection towards
the more refined class the common No ’DR’ class and thus
emphasizes the importance of the strategies, such as targeted
data.









