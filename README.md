# BabyGAN

![logo](https://raw.githubusercontent.com/tg-bomze/BabyGAN/master/media/logo.png)

**注：该复刻自tg-bomze/BabyGAN，为其汉语翻译**

**在Google colab上运行:**
- Russian Language [![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/tg-bomze/BabyGAN/blob/master/BabyGAN_(RUS).ipynb)
- English Language [![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/tg-bomze/BabyGAN/blob/master/BabyGAN_(ENG).ipynb)
- Chinese Language [![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/SupersuROOT/BabyGAN/blob/master/BabyGAN_(CHN).ipynb)

<p>
基于stylegan并从理论上通过父母的照片预测孩子的长相。输入图像以获取潜在特征，然后按一定比例混合输入图像。神经网络模型基于GAN体系结构。你可以改变各种参数:年龄，面部位置，情绪和性别。
</p>  

**基于:** [StyleGAN](https://github.com/NVlabs/stylegan)

**编码器:** [StyleGAN-Encoder](https://github.com/pbaylies/stylegan-encoder)

![example1](https://raw.githubusercontent.com/tg-bomze/BabyGAN/master/media/example1.JPG)
![example2](https://raw.githubusercontent.com/tg-bomze/BabyGAN/master/media/example2.JPG)
![example3](https://raw.githubusercontent.com/tg-bomze/BabyGAN/master/media/example3.JPG)

## 训练需要的模型
按照 [LINK](https://drive.google.com/drive/folders/1xwqqG0HkLe2AiXxjC-XK8OfvMKT1jBlp) 将该文件夹快捷方式链接到Google Drive:

![shortcut](media/mount_eng.png)

文件夹结构为:
    
    .
    ├── data                    
    │   └── finetuned_resnet.h5 
    ├── karras2019stylegan-ffhq-1024x1024.pkl
    ├── shape_predictor_68_face_landmarks.dat.bz2
    ├── vgg16_weights_tf_dim_ordering_tf_kernels_notop.h5
    ├── vgg16_zhang_perceptual.pkl
    └── ...

## 要求
* Python 3.6 64位.
* TensorFlow 1.10.0 - GPU.
* 一个或多个高端NVIDIA gpu，至少11GB DRAM.
* NVIDIA驱动程序391.35或更新版本、CUDA工具包9.0或更新版本、cudn 7 . 3 . 1或更新版本.

## 生成图像的潜在特征
您可以使用两个脚本生成自己图像的潜在表示:
1) 为图片创建文件夹
> mkdir raw_images aligned_images

2) 从图片提取特征点
> python align_images.py raw_images/ aligned_images/

3) 查找图片的潜在特征
> python encode_images.py aligned_images/ generated_images/ latent_representations/

## Usage BabyGAN
- SOON
