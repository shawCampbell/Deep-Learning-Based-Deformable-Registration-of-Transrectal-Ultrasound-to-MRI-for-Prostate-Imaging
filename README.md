![image](https://github.com/shawCampbell/Deep-Learning-Based-Deformable-Registration-of-Transrectal-Ultrasound-to-MRI-for-Prostate-Imaging/blob/main/VECTOR_FIELDS.drawio.png)

# Deep-Learning-Based-Deformable-Registration-of-Transrectal-Ultrasound-to-MRI-for-Prostate-Imaging
This repository contains some of the main Jupyter Notebooks used to conduct research on deep-learning deformable registration of transrectal ultrasound to magnetic resonance imaging deformable registration.

The thesis associated with this code is included in this repository , which has the following abstract:

*"This study investigates weakly supervised deformable registration of transrectal ultrasound
(TRUS) and magnetic resonance imaging (MRI) for prostate imaging. The work focuses
on evaluating the effectiveness of intensity-based similarity metrics versus label-driven
loss formulations, the impact of affine preprocessing, and the role of data augmentation
in improving model robustness. Using the MuRegPro dataset and a modified VoxelMorph
framework, the research systematically explores how architectural and preprocessing
choices affect multimodal registration accuracy. The findings demonstrate that intensity based unsupervised registration using metrics such as mean squared error and normalized
cross-correlation fails to capture anatomical correspondence across modalities, while weakly
supervised models driven by label similarity produce anatomically consistent results.
Affine preprocessing was shown to be essential in achieving stable deformation fields, and
non-rigid augmentation improved robustness without degrading generalization. These
results establish a practical foundation for anatomically faithful multimodal registration
and highlight key methodological considerations for similar applications in medical image
analysis."*

## Description of Jupyter Notebooks:

- 3D_WS_US-MRI_NCC.ipynb and 2D_WS_US-MRI_NCC.ipynb are weakly supervised models that were used in testing. They output sample validation images to view progress after each epoch, as well as samply output ddf fields for a validation pair. 3D_Evaluate.ipynb and 2D Evaluate.ipynb can be used to view the performance of a certain epoch from the models in accordance to the metrics outlined in the thesis.
- Preprocess_Affine.ipynb is used to create another dataset from the non-affinely preprocessed nifti_data dataset that is affinely preprocessed using ANTs as described in the thesis.
- 3D_WS_US-MRI_NCC.ipynb, MMDIR_H1_Part1_MSE.ipynb, MMDIR_H1_Part1_NCC.ipynb and MMDIR_H2.ipynb investigate the hypothesese mentioned in the thesis.
