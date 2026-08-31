# Algorithms and AI Libraries

<!-- i18n:language-selector:start -->
[中文](README.md) | **English**
<!-- i18n:language-selector:end -->

## Arithmetic

### float_converter

**Link** - [Rounding, ceiling, floor, and exact-integer conversion - Gitee Code Snippet](https://gitee.com/Luyi365/codes/e5rg4nls0mda6831qb2i767)  
**Features** - A library for rounding and integer conversion of floating-point data.  

#### Notes

---

### LibBF

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Link** - [LibBF Library](https://bellard.org/libbf/)  
**Features** - A high-precision floating-point arithmetic library that provides values with greater precision than standard floating-point types such as *float* and *double*, with flexible control over precision and rounding modes.  

#### Notes

---

## Fundamental Algorithms

### FXT

**Link** - [jj's useful and ugly FXT page](https://www.jjj.de/fxt/)  
**Features** - A collection of C algorithms focused on bit manipulation, combinatorics, fast transforms, and more.  

#### Notes

- Meaning of combinatorics: [Combinatorics - Wikipedia](https://en.wikipedia.org/wiki/Combinatorics)

---

### xxHash

[![GitHub Repo stars](https://img.shields.io/github/stars/Cyan4973/xxHash)](https://github.com/Cyan4973/xxHash/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Cyan4973/xxHash)](https://github.com/Cyan4973/xxHash/commits) | [![GitHub License](https://img.shields.io/github/license/Cyan4973/xxHash)]()

**Link** - [xxHash - Extremely fast non-cryptographic hash algorithm](https://xxhash.com/)  
**Features** - An extremely fast non-cryptographic hash algorithm that works under RAM and speed constraints and suits more demanding use cases.  

#### Notes

---

### Terathon Math Library

[![GitHub Repo stars](https://img.shields.io/github/stars/EricLengyel/Terathon-Math-Library)](https://github.com/EricLengyel/Terathon-Math-Library/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/EricLengyel/Terathon-Math-Library)](https://github.com/EricLengyel/Terathon-Math-Library/commits) | [![GitHub License](https://img.shields.io/github/license/EricLengyel/Terathon-Math-Library)]()

**Link** - [EricLengyel/Terathon-Math-Library: C++ math library for 2D/3D/4D vector, matrix, quaternion, and geometric algebra.](https://github.com/EricLengyel/Terathon-Math-Library)  
**Features** - A C++ mathematics library containing classes for vectors, matrices, quaternions, and projective geometric algebra elements. It can be used in graphics, AI, games, and related fields.  

#### Notes

---

## AI Frameworks

### TinyMaix

[![GitHub Repo stars](https://img.shields.io/github/stars/sipeed/TinyMaix)](https://github.com/sipeed/TinyMaix/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/sipeed/TinyMaix)](https://github.com/sipeed/TinyMaix/commits) | [![GitHub License](https://img.shields.io/github/license/sipeed/TinyMaix)]()

**Link** - [sipeed/TinyMaix: TinyMaix is a tiny inference library for microcontrollers (TinyML).](https://github.com/sipeed/TinyMaix)  
**Features** - An AI neural-network inference framework designed for resource-constrained microcontrollers.  

#### Notes

1. Training models with [MaixHub](https://maixhub.com/welcome) is recommended.
2. Supports bare-metal environments.
3. In addition to loading models, it includes basic neural-network layers.
4. Models must ultimately be converted into header files for inclusion; the repository contains scripts to convert [.h5](./appendix.en.md#hdf5) or tmdl files to `.h` format.
5. The code uses GDB debugging by default, so the <ins>system-time retrieval function</ins> and <ins>print function</ins> must be changed.
6. An example of the `layer callback` is provided, but its purpose is still unknown.

---

### miniMNIST-c

[![GitHub Repo stars](https://img.shields.io/github/stars/konrad-gajdus/miniMNIST-c)](https://github.com/konrad-gajdus/miniMNIST-c/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/konrad-gajdus/miniMNIST-c)](https://github.com/konrad-gajdus/miniMNIST-c/commits) | [![GitHub License](https://img.shields.io/github/license/konrad-gajdus/miniMNIST-c)]()

**Link** - [konrad-gajdus/miniMNIST-c](https://github.com/konrad-gajdus/miniMNIST-c)  
**Features** - A two-layer miniature neural network implemented in C, suitable for learning and basic embedded applications.  

#### Notes

---

### Genann

[![GitHub Repo stars](https://img.shields.io/github/stars/codeplea/genann)](https://github.com/codeplea/genann/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/codeplea/genann)](https://github.com/codeplea/genann/commits) | [![GitHub License](https://img.shields.io/github/license/codeplea/genann)]()

**Link** - [C Neural Network Library: Genann - Code Plea](https://codeplea.com/genann)  
**Features** - A minimal, thoroughly tested neural-network library for training and using feedforward artificial neural networks (ANNs) in C.  

#### Notes

---

### uTensor

[![GitHub Repo stars](https://img.shields.io/github/stars/uTensor/uTensor)](https://github.com/uTensor/uTensor/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/uTensor/uTensor)](https://github.com/uTensor/uTensor/commits) | [![GitHub License](https://img.shields.io/github/license/uTensor/uTensor)]()

**Link** - [uTensor/uTensor: TinyML AI inference library](https://github.com/uTensor/uTensor)  
**Features** - An extremely lightweight machine-learning inference framework built on TensorFlow that imports trained models as C++ files.  

#### Notes

---

### NNoM

[![GitHub Repo stars](https://img.shields.io/github/stars/majianjia/nnom)](https://github.com/majianjia/nnom/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/majianjia/nnom)](https://github.com/majianjia/nnom/commits) | [![GitHub License](https://img.shields.io/github/license/majianjia/nnom)]()

**Link** - [majianjia/nnom: A higher-level Neural Network library for microcontrollers.](https://github.com/majianjia/nnom)  
**Features** - A framework for running neural networks on MCUs. It is similar to [TinyMaix](#tinymaix) but offers more features.  

#### Notes

---

### Paddle Lite

[![GitHub Repo stars](https://img.shields.io/github/stars/PaddlePaddle/Paddle-Lite)](https://github.com/PaddlePaddle/Paddle-Lite/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/PaddlePaddle/Paddle-Lite)](https://github.com/PaddlePaddle/Paddle-Lite/commits) | [![GitHub License](https://img.shields.io/github/license/PaddlePaddle/Paddle-Lite)]()

**Link** - [PaddlePaddle - Open-source deep learning platform from industrial practice](https://www.paddlepaddle.org.cn/lite)  
**Features** - A high-performance, lightweight, flexible, and extensible deep-learning inference framework targeting mobile, embedded, edge, and other hardware platforms.  

#### Notes

- Chinese documentation support is good.

---

### TVM

[![GitHub Repo stars](https://img.shields.io/github/stars/hyperai/tvm-cn)](https://github.com/hyperai/tvm-cn/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/hyperai/tvm-cn)](https://github.com/hyperai/tvm-cn/commits) | [![GitHub License](https://img.shields.io/github/license/hyperai/tvm-cn)]()

**Link** - [Apache TVM Chinese site](https://tvm.hyper.ai/)  
**Features** - An end-to-end deep-learning compiler framework for CPU, GPU, ARM, and other hardware architectures.  

#### Notes

1. Supports bare-metal environments.

---

### tflite-micro

[![GitHub Repo stars](https://img.shields.io/github/stars/tensorflow/tflite-micro)](https://github.com/tensorflow/tflite-micro/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tensorflow/tflite-micro)](https://github.com/tensorflow/tflite-micro/commits) | [![GitHub License](https://img.shields.io/github/license/tensorflow/tflite-micro)]()

**Link** - [tensorflow/tflite-micro: Infrastructure to enable deployment of ML models to low-power resource-constrained embedded targets (including microcontrollers and digital signal processors).](https://github.com/tensorflow/tflite-micro)  
**Features** - TensorFlow Lite for microcontrollers, enabling deployment of machine-learning frameworks on MCUs.  

#### Notes

---

### ncnn

[![GitHub Repo stars](https://img.shields.io/github/stars/Tencent/ncnn)](https://github.com/Tencent/ncnn/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/Tencent/ncnn)](https://github.com/Tencent/ncnn/commits) | [![GitHub License](https://img.shields.io/github/license/Tencent/ncnn)]()

**Link** - [Tencent/ncnn: ncnn is a high-performance neural network inference framework optimized for the mobile platform](https://github.com/Tencent/ncnn)  
**Features** - A high-performance neural-network forward-computation framework highly optimized for mobile platforms. It supports most common CNN networks and can be deployed on some embedded chips.  

#### Notes

---

### MNN

[![GitHub Repo stars](https://img.shields.io/github/stars/alibaba/MNN)](https://github.com/alibaba/MNN/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/alibaba/MNN)](https://github.com/alibaba/MNN/commits) | [![GitHub License](https://img.shields.io/github/license/alibaba/MNN)]()

**Link** - [alibaba/MNN: MNN is a blazing fast, lightweight deep learning framework, battle-tested by business-critical use cases in Alibaba](https://github.com/alibaba/MNN)  
**Features** - A lightweight deep neural-network engine that supports deep-learning inference and training on embedded devices with POSIX interfaces.  

#### Notes

---

### TensorFlow Lite

[![GitHub Repo stars](https://img.shields.io/github/stars/tensorflow/tensorflow)](https://github.com/tensorflow/tensorflow/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/tensorflow/tensorflow)](https://github.com/tensorflow/tensorflow/commits) | [![GitHub License](https://img.shields.io/github/license/tensorflow/tensorflow)]()

**Link** - [TensorFlow Lite | TensorFlow Chinese website](https://ai.google.dev/edge/litert?hl=zh-cn)  
**Features** - A well-known machine-learning library for deploying models to mobile devices, microcontrollers, and other edge devices for on-device machine learning.  

#### Notes

---

### Mediapipe

[![GitHub Repo stars](https://img.shields.io/github/stars/google-ai-edge/mediapipe)](https://github.com/google-ai-edge/mediapipe/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/google-ai-edge/mediapipe)](https://github.com/google-ai-edge/mediapipe/commits) | [![GitHub License](https://img.shields.io/github/license/google-ai-edge/mediapipe)]()

**Link** - [MediaPipe | Google for Developers](https://developers.google.com/mediapipe)  
**Features** - Google's open-source cross-platform machine-learning framework. It provides tools that can be deployed to mobile, web, PC, and IoT devices, including models for object detection, image classification, face recognition, gesture recognition, text classification, language detection, and audio classification.  

#### Notes

---

### Edge Impulse

**Link** - [Edge Impulse - The Leading edge AI platform](https://edgeimpulse.com/)  
**Features** - A popular embedded machine-learning development platform for data processing and analysis, model training, and model deployment.  

#### Notes

---

### YMCV

[![Gitee Repo stars](https://gitee.com/yao_mi/ymcv/badge/star.svg?theme=gvp)](https://gitee.com/yao_mi/ymcv/stargazers) | [![Gitee last commit](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yao_mi/ymcv&query=$.pushed_at&label=lastcommit)]() | [![Gitee License](https://img.shields.io/badge/dynamic/json?url=https://gitee.com/api/v5/repos/yao_mi/ymcv&query=$.license&label=license)]()

**Link** - [YMCV: A cross-platform miniature computer-vision library](https://gitee.com/yao_mi/ymcv)  
**Features** - A miniature computer-vision library written purely in C, with no dependencies, cross-platform support, and easy feature trimming.  

#### Notes

---

### NeuralNetwork

[![GitHub Repo stars](https://img.shields.io/github/stars/GiorgosXou/NeuralNetworks)](https://github.com/GiorgosXou/NeuralNetworks/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/GiorgosXou/NeuralNetworks)](https://github.com/GiorgosXou/NeuralNetworks/commits) | [![GitHub License](https://img.shields.io/github/license/GiorgosXou/NeuralNetworks)]()

**Link** - [GitHub - GiorgosXou/NeuralNetworks: A resource-conscious neural network library for microcontrollers, with partial bare-metal & native-os support.](https://github.com/GiorgosXou/NeuralNetworks)  
**Features** - A neural-network library for MCUs that runs RNN, GRU, and LSTM architectures with very few resources and supports bare metal and some operating systems.  

#### Notes

---

## AI Models and Algorithms

### Knn

**Link** - [Knn algorithm - Gitee Code Snippet](https://gitee.com/Luyi365/codes/svnarwquze6g3l8hpo19i36)  
**Features** - A very basic KNN algorithm written in C with no particular optimizations; it is not recommended.  

#### Notes

- It consumes substantial memory; see the source code for details.
- Training and test data: [数据集.zip](assets/数据集-20231019211912-ejopzz4.zip).
- ~~Algorithm explanation: ((20231010191715-c224yjx 'K-nearest neighbors (KNN)'));~~ (pending release)

---

### NanoDet-Plus

[![GitHub Repo stars](https://img.shields.io/github/stars/RangiLyu/nanodet)](https://github.com/RangiLyu/nanodet/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/RangiLyu/nanodet)](https://github.com/RangiLyu/nanodet/commits) | [![GitHub License](https://img.shields.io/github/license/RangiLyu/nanodet)]()

**Link** - [RangiLyu/nanodet: NanoDet-Plus⚡Super fast and lightweight anchor-free object detection model. 🔥Only 980 KB(int8) / 1.8MB (fp16) and run 97FPS on cellphone🔥](https://github.com/RangiLyu/nanodet)  
**Features** - A super-fast, high-precision, lightweight anchor-free object-detection model implemented on a mobile AI framework.  

#### Notes

---

### pico

[![GitHub Repo stars](https://img.shields.io/github/stars/nenadmarkus/pico)](https://github.com/nenadmarkus/pico/stargazers) | [![GitHub last commit](https://img.shields.io/github/last-commit/nenadmarkus/pico)](https://github.com/nenadmarkus/pico/commits) | [![GitHub License](https://img.shields.io/github/license/nenadmarkus/pico)]()

**Link** - [nenadmarkus/pico: A minimalistic framework for real-time object detection (with a pre-trained face detector)](https://github.com/nenadmarkus/pico)  
**Features** - A lightweight face-recognition algorithm based on pixel-intensity comparisons for object detection, suitable for single-purpose, low-traffic scenarios.  

#### Notes

- Introduction: [Sharing a lightweight open-source face-recognition algorithm](https://mp.weixin.qq.com/s/33VfAAxSOS_7VqLsgzqhkQ)

---
