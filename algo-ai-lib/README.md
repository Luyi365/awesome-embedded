# 算法与AI库

## 算术

### float_converter

**链接**：[四舍五入、向上取整、向下取整、精确取整 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/e5rg4nls0mda6831qb2i767)  
**特征**：浮点数据四舍五入、取整处理库。  

#### 要点

---

### LibBF

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**链接**：[LibBF Library](https://bellard.org/libbf/)  
**特征**：高精度浮点运算的库，提供比标准浮点数（如 *float* 和 *double*）精度更高的数值，并且可以灵活地控制精度和舍入模式。  

#### 要点

---

## 基础算法

### FXT

**链接**：[jj's useful and ugly FXT page](https://www.jjj.de/fxt/)  
**特征**：C 语言的算法库集合，专注于位运算、组合数学、快速变换等。  

#### 要点

- 组合数学含义：[Combinatorics - Wikipedia](https://en.wikipedia.org/wiki/Combinatorics)

---

### xxHash

[![GitHub Repo stars](https://img.shields.io/github/stars/Cyan4973/xxHash)](https://github.com/Cyan4973/xxHash/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Cyan4973/xxHash)](https://github.com/Cyan4973/xxHash/commits) | [![GitHub License](https://img.shields.io/github/license/Cyan4973/xxHash)]()

**链接**：[xxHash - Extremely fast non-cryptographic hash algorithm](https://xxhash.com/)  
**特征**：是一种速度极快的非加密哈希算法，可在 RAM 、速度限制下工作，适合更专业的使用场景。  

#### 要点

---

### Terathon Math Library

[![GitHub Repo stars](https://img.shields.io/github/stars/EricLengyel/Terathon-Math-Library)](https://github.com/EricLengyel/Terathon-Math-Library/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/EricLengyel/Terathon-Math-Library)](https://github.com/EricLengyel/Terathon-Math-Library/commits) | [![GitHub License](https://img.shields.io/github/license/EricLengyel/Terathon-Math-Library)]()

**链接**：[EricLengyel/Terathon-Math-Library: C++ math library for 2D/3D/4D vector, matrix, quaternion, and geometric algebra.](https://github.com/EricLengyel/Terathon-Math-Library)  
**特征**：一个用C++写成的数学库，包含向量、矩阵、四元数和射影几何代数元素的类。可用于图形、AI、游戏等领域。  

#### 要点

---

## AI 框架

### TinyMaix

[![GitHub Repo stars](https://img.shields.io/github/stars/sipeed/TinyMaix)](https://github.com/sipeed/TinyMaix/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/sipeed/TinyMaix)](https://github.com/sipeed/TinyMaix/commits) | [![GitHub License](https://img.shields.io/github/license/sipeed/TinyMaix)]()

**链接**：[sipeed/TinyMaix: TinyMaix is a tiny inference library for microcontrollers (TinyML).](https://github.com/sipeed/TinyMaix)  
**特征**：专为低资源的单片机设计的 AI 神经网络推理框架。  

#### 要点

1. 配合 [MaixHub](https://maixhub.com/welcome) 使用训练模型更佳；
2. 支持裸机；
3. 除了可以加载模型外，还带有基本的神经网络层；
4. 模型最后需要转换成头文件被读取，文件里有 [.h5](./appendix.md#hdf5) 或 tmdl 格式转换成 .h 格式的脚本；
5. 代码默认使用 GDB 调试，因此需要修改<ins>系统时间获取函数</ins>和<ins>打印函数</ins>；
6. 其中层回调（`layer callback`）有示例，但还不知道作用是什么；

---

### miniMNIST-c

[![GitHub Repo stars](https://img.shields.io/github/stars/konrad-gajdus/miniMNIST-c)](https://github.com/konrad-gajdus/miniMNIST-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/konrad-gajdus/miniMNIST-c)](https://github.com/konrad-gajdus/miniMNIST-c/commits) | [![GitHub License](https://img.shields.io/github/license/konrad-gajdus/miniMNIST-c)]()

**链接**：[konrad-gajdus/miniMNIST-c](https://github.com/konrad-gajdus/miniMNIST-c)  
**特征**：C 语言实现了一个迷你神经网络（两层），可用于学习和基础嵌入式领域。  

#### 要点

---

### Genann

[![GitHub Repo stars](https://img.shields.io/github/stars/codeplea/genann)](https://github.com/codeplea/genann/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/codeplea/genann)](https://github.com/codeplea/genann/commits) | [![GitHub License](https://img.shields.io/github/license/codeplea/genann)]()

**链接**：[C Neural Network Library: Genann - Code Plea](https://codeplea.com/genann)  
**特征**：极简的神经网络库，经过充分测试，用于在 C 中训练和使用前馈人工神经网络（ANN）。  

#### 要点

---

### uTensor

[![GitHub Repo stars](https://img.shields.io/github/stars/uTensor/uTensor)](https://github.com/uTensor/uTensor/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/uTensor/uTensor)](https://github.com/uTensor/uTensor/commits) | [![GitHub License](https://img.shields.io/github/license/uTensor/uTensor)]()

**链接**：[uTensor/uTensor: TinyML AI inference library](https://github.com/uTensor/uTensor)  
**特征**：基于 TensorFlow 构建的极其轻量级的机器学习推理框架，并将训练模型生成C++文件导入使用。  

#### 要点

---

### NNoM

[![GitHub Repo stars](https://img.shields.io/github/stars/majianjia/nnom)](https://github.com/majianjia/nnom/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/majianjia/nnom)](https://github.com/majianjia/nnom/commits) | [![GitHub License](https://img.shields.io/github/license/majianjia/nnom)]()

**链接**：[majianjia/nnom: A higher-level Neural Network library for microcontrollers.](https://github.com/majianjia/nnom)  
**特征**：专门为了神经网络在 MCU 上运行的框架，使用起来和 [TinyMaix](#tinymaix) 类似。很像，但功能更多。  

#### 要点

---

### Paddle Lite

[![GitHub Repo stars](https://img.shields.io/github/stars/PaddlePaddle/Paddle-Lite)](https://github.com/PaddlePaddle/Paddle-Lite/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/PaddlePaddle/Paddle-Lite)](https://github.com/PaddlePaddle/Paddle-Lite/commits) | [![GitHub License](https://img.shields.io/github/license/PaddlePaddle/Paddle-Lite)]()

**链接**：[飞桨 PaddlePaddle-源于产业实践的开源深度学习平台](https://www.paddlepaddle.org.cn/lite)  
**特征**：高性能、轻量级、灵活性强且易于扩展的深度学习推理框架，定位于支持包括移动端、嵌入式以及边缘端在内的多种硬件平台。  

#### 要点

- 中文文档支持良好；

---

### TVM

[![GitHub Repo stars](https://img.shields.io/github/stars/hyperai/tvm-cn)](https://github.com/hyperai/tvm-cn/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hyperai/tvm-cn)](https://github.com/hyperai/tvm-cn/commits) | [![GitHub License](https://img.shields.io/github/license/hyperai/tvm-cn)]()

**链接**：[Apache TVM 是一个端到端的深度学习编译框架，适用于 CPU、GPU 和各种机器学习加速芯片。 | Apache TVM 中文站](https://tvm.hyper.ai/)  
**特征**：内置深度学习编译器，适用于 CPU、GPU、ARM 等多种硬件架构，提供一条龙服务。  

#### 要点

1. 支持裸机；

---

### tflite-micro

[![GitHub Repo stars](https://img.shields.io/github/stars/tensorflow/tflite-micro)](https://github.com/tensorflow/tflite-micro/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tensorflow/tflite-micro)](https://github.com/tensorflow/tflite-micro/commits) | [![GitHub License](https://img.shields.io/github/license/tensorflow/tflite-micro)]()

**链接**：[tensorflow/tflite-micro: Infrastructure to enable deployment of ML models to low-power resource-constrained embedded targets (including microcontrollers and digital signal processors).](https://github.com/tensorflow/tflite-micro)  
**特征**：适用于微控制器的 TensorFlow Lite，也就是在单片机上部署机器学习框架。  

#### 要点

---

### ncnn

[![GitHub Repo stars](https://img.shields.io/github/stars/Tencent/ncnn)](https://github.com/Tencent/ncnn/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Tencent/ncnn)](https://github.com/Tencent/ncnn/commits) | [![GitHub License](https://img.shields.io/github/license/Tencent/ncnn)]()

**链接**：[Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform](https://github.com/Tencent/ncnn)  
**特征**：是一个为移动端极致优化的高性能神经网络前向计算框架，支持大部分常用的 CNN 网络，可部署在部分嵌入式芯片上。  

#### 要点

---

### MNN

[![GitHub Repo stars](https://img.shields.io/github/stars/alibaba/MNN)](https://github.com/alibaba/MNN/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/alibaba/MNN)](https://github.com/alibaba/MNN/commits) | [![GitHub License](https://img.shields.io/github/license/alibaba/MNN)]()

**链接**：[alibaba/MNN: MNN is a blazing fast, lightweight deep learning framework, battle-tested by business-critical use cases in Alibaba](https://github.com/alibaba/MNN)  
**特征**：轻量级的深度神经网络引擎，支持深度学习的推理与训练，支持具有 POSIX 接口的嵌入式设备。  

#### 要点

---

### TensorFlow Lite

[![GitHub Repo stars](https://img.shields.io/github/stars/tensorflow/tensorflow)](https://github.com/tensorflow/tensorflow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tensorflow/tensorflow)](https://github.com/tensorflow/tensorflow/commits) | [![GitHub License](https://img.shields.io/github/license/tensorflow/tensorflow)]()

**链接**：[TensorFlow Lite | TensorFlow 中文官网](https://ai.google.dev/edge/litert?hl=zh-cn)  
**特征**：极有名的机器学习库，可用于在移动设备、微控制器和其他边缘设备上部署模型，以便实现设备端机器学习。  

#### 要点

---

### Mediapipe

[![GitHub Repo stars](https://img.shields.io/github/stars/google-ai-edge/mediapipe)](https://github.com/google-ai-edge/mediapipe/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/google-ai-edge/mediapipe)](https://github.com/google-ai-edge/mediapipe/commits) | [![GitHub License](https://img.shields.io/github/license/google-ai-edge/mediapipe)]()

**链接**：[MediaPipe  |  Google for Developers](https://developers.google.com/mediapipe)  
**特征**：谷歌开源的跨平台机器学习框架。它是一个能够轻松部署到移动端、Web、PC 和物联网设备的机器学习工具库，包含了物体检测、图像分类、人脸识别、手势识别、文本分类、语言检测、音频分类等模型。  

#### 要点

---

### Edge Impulse

**链接**：[Edge Impulse - The Leading edge AI platform](https://edgeimpulse.com/)  
**特征**：流行的嵌入式机器学习开发平台，可以完成数据处理和分析、模型训练、部署模型等工作。  

#### 要点

---

### YMCV

[![Gitee Repo stars](https://gitee.com/yao_mi/ymcv/badge/star.svg?theme=gvp)](https://gitee.com/yao_mi/ymcv/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yao_mi/ymcv&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yao_mi/ymcv&query=$.license&label=license)]()

**链接**：[YMCV: 跨平台迷你计算视觉库，可裸奔在免操作系统的单片机上，集成了近150个demo，并附带测试视频以便大家使用参考。它是ymkv-2.0版本（可移植任意平台）,平台从codeblocks迁移到vs，并经过一些架构调整和算法优化，取消了user层的集合封装，以便链接器能进行优化，对未使用的部分不进行加载，减少不必要内存消耗。](https://gitee.com/yao_mi/ymcv)  
**特征**：纯C写的迷你计算机视觉库，无依赖、跨平台，可方便裁剪所需功能。  

#### 要点

---

### NeuralNetwork

[![GitHub Repo stars](https://img.shields.io/github/stars/GiorgosXou/NeuralNetworks)](https://github.com/GiorgosXou/NeuralNetworks/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GiorgosXou/NeuralNetworks)](https://github.com/GiorgosXou/NeuralNetworks/commits) | [![GitHub License](https://img.shields.io/github/license/GiorgosXou/NeuralNetworks)]()

**链接**：[GitHub - GiorgosXou/NeuralNetworks: A resource-conscious neural network library for microcontrollers, with partial bare-metal & native-os support.](https://github.com/GiorgosXou/NeuralNetworks)  
**特征**：专用于单片机的神经网络库，仅需极少的资源即可运行RNN、GRU和LSTM等架构，支持裸机和部分操作系统。  

#### 要点

---

## AI 模型＆算法

### Knn

**链接**：[Knn 算法 - 代码片段 - Gitee.com](https://gitee.com/Luyi365/codes/svnarwquze6g3l8hpo19i36)  
**特征**：用 C 语言编写的 Knn 算法，十分基础，没有什么优化，不太推荐使用。  

#### 要点

- 十分消耗内存，具体可查看代码；
- 训练测试集：[数据集.zip](assets/数据集-20231019211912-ejopzz4.zip)；
- ~~算法讲解：((20231010191715-c224yjx 'K最近邻算法（KNN）'))；~~（待发布）

---

### NanoDet-Plus

[![GitHub Repo stars](https://img.shields.io/github/stars/RangiLyu/nanodet)](https://github.com/RangiLyu/nanodet/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/RangiLyu/nanodet)](https://github.com/RangiLyu/nanodet/commits) | [![GitHub License](https://img.shields.io/github/license/RangiLyu/nanodet)]()

**链接**：[RangiLyu/nanodet: NanoDet-Plus⚡Super fast and lightweight anchor-free object detection model. 🔥Only 980 KB(int8) / 1.8MB (fp16) and run 97FPS on cellphone🔥](https://github.com/RangiLyu/nanodet)  
**特征**：超快速、高精度的轻量级无锚物体检测模型，基于移动端 AI 框架实现。  

#### 要点

---

### pico

[![GitHub Repo stars](https://img.shields.io/github/stars/nenadmarkus/pico)](https://github.com/nenadmarkus/pico/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nenadmarkus/pico)](https://github.com/nenadmarkus/pico/commits) | [![GitHub License](https://img.shields.io/github/license/nenadmarkus/pico)]()

**链接**：[nenadmarkus/pico: A minimalistic framework for real-time object detection (with a pre-trained face detector)](https://github.com/nenadmarkus/pico)  
**特征**：轻量级的人脸识别算法，基于像素强度比较的目标检测，适合单一、流量较小的场景。  

#### 要点

- 使用介绍：[分享一个轻量级的开源人脸识别算法](https://mp.weixin.qq.com/s/33VfAAxSOS_7VqLsgzqhkQ)

---
