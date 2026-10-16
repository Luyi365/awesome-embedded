## HDF5

**File extensions**: `.h5` or `.hdf5`

This is a common model-storage format that can store a model's weights, architecture, and configuration.
In <ins>TensorFlow</ins> and <ins>Keras</ins>, save a model in HDF5 format with `model.save('model.h5')`.

Reference: [Introduction to HDF5 data files - Zhihu](https://zhuanlan.zhihu.com/p/104145585)

---

## K-Nearest Neighbors (KNN)

Short for K-Nearest Neighbor, meaning "the K nearest neighbors". The idea is simply to **follow the crowd**: for a data sample to be classified, the algorithm finds the few samples closest to it, i.e. its neighbors, and then looks at their labels. If most of those neighbors belong to one class, it decides the sample belongs to that class too. The parameter K is the number of neighbors, usually a number no greater than 20, such as 3, 5, or 7.

![knn-diagram](./knn-diagram.png)

---
