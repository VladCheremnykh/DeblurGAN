# DeblurGAN
[arXiv Paper Version](https://arxiv.org/pdf/1711.07064.pdf)

Pytorch implementation of the paper DeblurGAN: Blind Motion Deblurring Using Conditional Adversarial Networks.

Our network takes blurry image as an input and procude the corresponding sharp estimate, as in the example:
<img src="images/animation3.gif" width="400px"/> <img src="images/animation4.gif" width="400px"/>

The model we use is Conditional Wasserstein GAN with Gradient Penalty + Perceptual loss based on VGG-19 activations. Such architecture also gives good results on other image-to-image translation problems (super resolution, colorization, inpainting, dehazing etc.)

### Prerequisites data
- cd ~/DeblurGAN
- ./install_data.sh
- or
- bash -x ./install_data.sh

### Train

- python3 ./train.py --dataroot ./data/combined --resize_or_crop crop --display_id -1 --cuda True


### Test

- python3 ./test.py --dataroot ./data/blurred --model test --dataset_mode single --cuda True --which_model_netG FPN101

### Model trained 2000 times
https://drive.google.com/file/d/1vGiqFXa177sCGHEuKhDKQ0VxvZZ2qpZg

### Help you understand code
http://fatalfeel.blogspot.com/2013/12/deblurgan-image-synthesis-and-analysis.html
