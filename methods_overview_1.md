# Deep Learning Depth Estimation Methods Overview by Categories

This is essentially a simplified version of [_Monocular Depth Estimation Based on Deep Learning: An Overview_](https://arxiv.org/pdf/2003.06620.pdf) by Zhao et al. with some comments. 

---

## Supervised

### Methods based on different architectures and loss functions

1. Eigen. Depth map prediction from a single image using a multi-scale deep network
2. Eigen. Predicting depth, surface normals and semantic labels with a common multi-scale convolutional architecture
3. Mayer. A large dataset to train convolutional networks for disparity, **optical flow**, and scene flow estimation
4. Shelhamer. **Scene intrinsics** and depth from a single image
5. Laina. Deeper depth prediction with fully convolutional residual networks
	- residual learning
	- reverse Huber loss (berhu) for better result than L2
6. Mancini. Fast robust monocular depth estimation for obstacle detection with fully convolutional networks
	- use image and optical flow to estimate depth
7. Chen. Single image depth prediction in the wild (2016, DIW)
	- new DIW dataset and relative depth annotations
8. Fu. Deep ordinal regression network for monocular depth estimation (DORN)

### Methods based on conditional random fields

1. Li. Depth and surface normal estimation from monocular images using regression on deep features and hierarchical CRFs
	- conditional random fields
	- super pixel?
2. Liu. Learning depth from single monocular images using deep convolutional neural fields
3. Wang. Towards unified depth and semantic prediction from a single image
	- utilizing semantic consistency between depth and semantic labels
4. Zhang. Joint task-recursive learning for semantic segmentation and depth estimation
5. Xu. Structured attention guided convolutional neural fields for monocular depth estimation

### Methods based on adversarial learning

1. Feng. SGANVO: Unsupervised deep visual odometry and depth estimation with stacked generative adversarial networks (IEEE, 2019)
2. Jung. Depth prediction from a single image with conditional adversarial networks (ICIP, 2017)
3. Gwn Lore. Generative adversarial networks for depth map estimation from RGB video (CVPR, 2018)

---

## Unsupervised

### Basic model

Trained using monocular sequences, these methods project the prediction of one frame to the next. The camera intrinsics need to be known.

1. Zhou. Unsupervised learning of depth and ego-motion from video
2. Godard. Unsupervised monocular depth estimation with left-right consistency (CVPR, 2017)

### Methods based on explainability mask

The aforementioned models are based on the static-object assumption. To solve the problem that the assumption may not hold in real world, explainability masks are proposed to identify only the static objects.

### Methods based on traditional visual odometry

TBA

### Methods based on multi-tasks framework

TBA

### Methods based on adversarial learning

TBA

---

## Semi-supervised monocular depth estimation

### Basic model

Trained on stereo images, semi-supervised methods use inverse warping guided by the predicted disparity.

### Methods based on stereo matching

1. Luo. Single view stereo matching (CVPR, 2018)

### Methods based on adversarial learning and knowledge distillation

1. Pilzer. Refine and distill: Exploiting cycle-inconsistency and knowledge distillation for unsupervised monocular depth estimation
