# Bone & Bone Lesion Segmentation in SPECT/CT Using U-Net
This is an implementation of the bone and bone lesion segmentation, multi-modal U-Net in Nuclear Medicine Imaging, the network was trained on the simulated SPECT/Atten. Map images and tested on the patient PET/CT images.
#### Main script: boneSegUnet/run/train_UNet.py
# U-Net:
## Network Architecture
![](https://github.com/junyuchen245/SPECT_CT_UNet/blob/master/UNET.png)

Trainable Parameters: 15,317,115.
## Example Segmentation Results
### Validation Set (SPECT/CT simulations)
<img src="https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/sample_img/validation.png" width="400"/>
Dice similarity coefficient: 0.958 for lesion, 0.963 for bone

### Testing Set (PET/CT)
<img src="https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/sample_img/testing.png" width="300"/>
Resulting an undesired result with the unseen patient PET/CT images.

## Example Feature Maps of the Testing Set
Redundant feature maps were observed, meaning that we could reduce the number of filters/parameters.
### CT encoding stage, 4th layer:
<img src="https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/features/conv_ct_256.png" width="600"/>

### SPECT encoding stage, 4th layer:
<img src="https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/features/conv_spect_256.png" width="600"/>

# Res-U-Net:
This is almost the same as the U-Net segmentation project (<a href="https://github.com/junyuchen245/SPECT-CT-Seg-UNet">SPECT-CT-Seg-UNet</a>), but the U-Net was modified to the Residual U-Net discribed in:

<a href="https://ieeexplore.ieee.org/abstract/document/8309343">Zhange, Zhengxin, et al. "Road extraction by deep residual u-net." IEEE Geoscience and Remote Sensing Letters, vol. 15, no. 5, pp. 749-753, May 2018.</a>

## Sample Results:

