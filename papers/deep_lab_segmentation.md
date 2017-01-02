# DeepLab Segmentation

paper: https://arxiv.org/abs/1606.00915

Title: "DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs"

## Challenges
There are 3 challenges in segmentation using Deep CNNs
- reduced feature resolutions due to presence of multiple max-pooling and striding(downsampling). Feature maps resulting from this have reduced feature resolutions. [Solution]: instead of downsampling, use Upsampling to increase resolution in last few layers. (Atrous Convolution + bilinear interpolation) to recover original image resolution.  
- multiple scales objects present in image. [Solution]: Using Atrous spatial pyramid pooling, multiple filters are used to collect complementary field of view as a result capture multiple scales, including context and object.
- presence of DCNN invariance reduces localization accuracy. [Solution]: use of fully connected CRF to assimilate fine details.

## Advantages
Finally, some advantages of DeepLab
- high speed of 8 FPS.
- state-of-art accuracy.
- simple structure.     

## Related Works
DCNN based segmentation have following major categories
- cascade of bottom-up segmentation with DCNN based region segmentation[7], [49], [50]
- Coupling a convolutionally computed DCNN for image labelling and an independent segmentation. [39, 21, 51]
- segmentation free approach by computing dense category-level pixel labels.[14, 52]

Works using CRF with DCNN
- [22]
- [53]
- [39]
- [57]

## Advances in Segmentation
End-to-End training for structured prediction
- [40, 59, 62, 64, 65] proposed methods for joint learning of DCNN and CRFs.

Weaker Supervision based methods
- [58, 69, 70, 71] relaxes assumption of availability of pixel-level semantic annotations for training whole set.

## Model Description
![Model Description](imgs/deeplab_img1.tiff)

## Results
![Results](imgs/deeplab_img2.tiff)
