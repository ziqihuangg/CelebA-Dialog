# CelebA-Dialog

**Talk-to-Edit: Fine-Grained Facial Editing via Dialog** </br>
[Yuming Jiang*](https://yumingj.github.io/),
[Ziqi Huang*](https://ziqihuangg.github.io/),
[Xingang Pan](https://xingangpan.github.io/),
[Chen Change Loy](https://www.mmlab-ntu.com/person/ccloy/)
and
[Ziwei Liu](https://liuziwei7.github.io/) </br>
In IEEE International Conference on Computer Vision (**ICCV**), 2021.

From [MMLab@NTU](https://www.mmlab-ntu.com/index.html) affliated with S-Lab, Nanyang Technological University and SenseTime Research.

<img src="./assets/celeba_dialog.png" width="50%">

[**[Project Page]**](https://www.mmlab-ntu.com/project/talkedit/) | [**[Paper]**](https://arxiv.org/abs/2109.04425) | [**[Code]**](https://github.com/yumingj/Talk-to-Edit) | [**[Video]**](https://www.youtube.com/watch?v=ZKMkQhkMXPI)

**CelebA-Dialog** is a large-scale visual-language face dataset with the following features:
- Facial images are annotated with rich **fine-grained labels**, which classify one attribute into multiple degrees according to its semantic meaning.
- Accompanied with each image, there are **captions** describing the attributes and a **user request** sample.


<img src="./assets/dataset.png" width="100%">

The dataset can be employed as the training and test sets for the following computer vision tasks: fine-grained facial attribute recognition, fine-grained facial manipulation, text-based facial generation and manipulation, face image captioning, natural language based facial recognition and manipulation, and broader multi-modality learning tasks.
The dataset is proposed in [Talk-to-Edit](https://github.com/yumingj/Talk-to-Edit).

## Download Links
You can download using the following links:

| Path | Size | Files | Format | Description
| :--- | :---- | ----: | :----: | :----------
| [CelebA-Dialog-combined](https://drive.google.com/drive/folders/1YRRaC3LWLHorVhFNJPzVqLrUlA10eLEJ?usp=sharing) | ~4.4 GB | - | | main folder
| &boxvr;&nbsp; [image](https://drive.google.com/file/d/1A2dNWabg6_um-V3lhw1tyead5hCpjaW8/view?usp=sharing) | ~2.7 GB | 30,000 | JPG | images from CelebA-HQ
| &boxvr;&nbsp; [classification_label](https://drive.google.com/drive/folders/1aEBwVe4syZjCayambAnonfAI2m3JsMcP?usp=sharing) | ~4.1 MB | 2 | txt | manually annotated parsing labels
| &boxvr;&nbsp; [text](https://drive.google.com/drive/folders/1CzTZm8suzDWdoN6DQmv11tsZotYo1Yfu?usp=sharing) | ~27 MB | 4 | TXT and JSON | natural language captions and editing requests
| &boxvr;&nbsp; [mask](https://drive.google.com/drive/folders/1bRZmrUBz8y0ObTr8AlkbVfyUco5R2I0z?usp=sharing) | ~1.8 GB | - | PNG | segmentation masks (1) [binary](https://drive.google.com/file/d/1MUYHw-IGP5FHy0yJzgvXNZojlcnCq7IE/view?usp=sharing) (2) [colorized](https://drive.google.com/file/d/1w8DMOW8tXsCGUD99-VsdzXmXjL2BGlp9/view?usp=sharing)


### Image

* 30,000 face images selected from the CelebA dataset by following CelebA-HQ
* High resolution of 1024 x 1024

### Classification Label

* 40 binary attributes annotations per image
* 5 fine-grained attributes annotations per image: Bangs, Eyeglasses, Beard, Smiling, and Age

### Text

* Textual captions for each image
* A user editing request per image

### Mask

We preprocess the facial segmentation masks of [CelebAMask-HQ](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebAMask_HQ.html) to ease future research.
* You can directly download the ***binary masks for individual labels*** for each image. These are the same as the ones provided in CelebAMask_HQ. ([Download link]())
* We produce the ***combined colorized mask*** for each image following the parsing of [CelebAMask-HQ](https://mmlab.ie.cuhk.edu.hk/projects/CelebA/CelebAMask_HQ.html). ([Download link]())




Below is the color-to-label parsing information:

| Label list | | | | |
| ------------ | ------------- | ------------ | ------------- | ------------ |
| 0: 'background' | 1: 'skin' | 2: 'nose' |  3: 'eye_g' | 4: 'l_eye' |
| 5: 'r_eye' | 6: 'l_brow' | 7: 'r_brow' | 8: 'l_ear' | 9: 'r_ear' |
| 10: 'mouth' | 11: 'u_lip' | 12: 'l_lip' | 13: 'hair' | 14: 'hat' |
| 15: 'ear_r' | 16: 'neck_l' | 17: 'neck' | 18: 'cloth' | | |

```python
color_list = [
    [0, 0, 0], [204, 0, 0], [76, 153, 0], [204, 204, 0], [51, 51, 255],
    [204, 0, 204], [0, 255, 255], [255, 204, 204], [102, 51, 0], [255, 0, 0],
    [102, 204, 0], [255, 255, 0], [0, 0, 153], [0, 0, 204], [255, 51, 153],
    [0, 204, 204], [0, 51, 0], [255, 153, 51], [0, 204, 0]]
label_dict = {
    0: 'background',	1: 'skin',	2: 'nose', 3: 'eye_g',	4: 'l_eye',
    5: 'r_eye', 6: 'l_brow',	7: 'r_brow',	8: 'l_ear', 9: 'r_ear',
    10: 'mouth',	11: 'u_lip', 12: 'l_lip',	13: 'hair',	14: 'hat',
    15: 'ear_r',	16: 'neck_l',	17: 'neck', 18: 'cloth',}
```

## Agreement
* The CelebA-Dialog dataset is available for non-commercial research purposes only.
* You agree not to reproduce, duplicate, copy, sell, trade, resell or exploit for any commercial purposes, any portion of the images and any portion of derived data.
* You agree not to further copy, publish or distribute any portion of the DeepFashion-MultiModal dataset. Except, for internal use at a single site within the same organization it is allowed to make copies of the dataset.

## Citation

If you find this dataset useful for your research and use it in your work, please consider cite the following papers:

```bibtex
@InProceedings{CelebA-Dialog,
  title = {Talk-to-Edit: Fine-Grained Facial Editing via Dialog},
  author = {Jiang, Yuming and Huang, Ziqi and Pan, Xingang and Loy, Chen Change and Liu, Ziwei},
  booktitle = {Proceedings of the IEEE/CVF International Conference on Computer Vision},
  year={2021}
}

@inproceedings{CelebAMask-HQ,
  title = {MaskGAN: Towards Diverse and Interactive Facial Image Manipulation},
  author = {Lee, Cheng-Han and Liu, Ziwei and Wu, Lingyun and Luo, Ping},
  booktitle = {IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year = {2020}
}

@inproceedings{CelebA-HQ,
  title={Progressive Growing of {GAN}s for Improved Quality, Stability, and Variation},
  author={Tero Karras and Timo Aila and Samuli Laine and Jaakko Lehtinen},
  booktitle={International Conference on Learning Representations},
  year={2018},
}

@inproceedings{CelebA,
  title = {Deep Learning Face Attributes in the Wild},
  author = {Liu, Ziwei and Luo, Ping and Wang, Xiaogang and Tang, Xiaoou},
  booktitle = {Proceedings of International Conference on Computer Vision (ICCV)},
  month = {December},
  year = {2015}
}
```
