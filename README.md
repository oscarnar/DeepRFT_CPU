# Deep Residual Fourier Transformation for Single Image Deblurring for CPU
<!-- Xintian Mao, Yiming Liu, Wei Shen, Qingli Li and Yan Wang -->
Implementation for DeepRFT to CPU.


<!-- **Paper**: https://arxiv.org/abs/2111.11745 -->


## Network Architecture
<table>
  <tr>
    <td> <img src = "./images/framework.png" width="800"> </td>
  </tr>
  <tr>
    <td><p align="center"><b>Overall Framework of DeepRFT</b></p></td>
  </tr>
</table>

## Installation
<!-- The model is built in PyTorch 1.8.0 and tested on Ubuntu 18.04 environment (Python3.8, CUDA11.1). -->

For installing, follow these intructions, this is an implementation for CPU.
```
conda create -n pytorch python=3.10
conda activate pytorch
conda install pytorch==1.11.0 torchvision==0.9.0 torchaudio==0.8.0 cudatoolkit=11.1 -c pytorch -c conda-forge
pip install matplotlib scikit-image opencv-python yacs joblib natsort h5py tqdm kornia tensorboard ptflops
```

Install warmup scheduler

```
cd pytorch-gradual-warmup-lr; python setup.py install; cd ..
```

## Quick Run

To test the pre-trained models of Deblur and Defocus [Google Drive](https://drive.google.com/file/d/1FoQZrbcYPGzU9xzOPI1Q1NybNUGR-ZUg/view?usp=sharing) on your own images, run 
```
python test.py --weights ckpt_path_here --input_dir path_to_images --result_dir save_images_here --win_size 256 # deblur
python test.py --weights ckpt_path_here --input_dir path_to_images --result_dir save_images_here --win_size 512 # defocus
```
Here is an example to train:
```
python train.py
```


<!-- ## Results
Experiment for image deblurring.
<table>
  <tr>
    <td> <img src = "./images/psnr_params_flops.png" width="1200"> </td>
  </tr>
  <tr>
    <td><p align="center"><b>Deblurring on GoPro Datasets.</b></p></td>
  </tr>
</table> -->

## Reference Code:
- https://github.com/INVOKERer/DeepRFT
- https://github.com/yangyanli/DO-Conv
- https://github.com/swz30/MPRNet
- https://github.com/chosj95/MIMO-UNet
- https://github.com/codeslake/IFAN

<!-- ## Citation
If you use DeepRFT, please consider citing:

    @inproceedings{,
        title={Deep Residual Fourier Transformation for Single Image Deblurring},
        author={Xintian Mao, Yiming Liu, Wei Shen, Qingli Li, Yan Wang},
        booktitle={arXiv:2111.11745},
        year={2021}
    } -->

<!-- ## Contact
If you have any question, please contact mxt_invoker1997@163.com -->
