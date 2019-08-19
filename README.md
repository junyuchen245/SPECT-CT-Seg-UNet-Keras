# Bone & Bone Lesion Segmentation in SPECT/CT Using U-Net

## Network Architecture
![](https://github.com/junyuchen245/SPECT_CT_UNet/blob/master/UNET.png)

Trainable Parameters: 15,317,115
## Example Segmentation Results
### Validation Set (SPECT/CT simulations)
![](https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/sample_img/validation.png)
Dice similarity coefficient: 0.958 for lesion, 0.963 for bone

### Testing Set (PET/CT)
![](https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/sample_img/testing.png)
Resulting an undesired results with unseen patient PET/CT images.

## Example Feature Maps
![](https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/features/conv_ct_256.png)
CT encoding stage, 4th layer.

![](https://github.com/junyuchen245/SPECT_CT_Seg_UNet/blob/master/features/conv_spect_256.png)
SPECT encoding stage, 4th layer.
