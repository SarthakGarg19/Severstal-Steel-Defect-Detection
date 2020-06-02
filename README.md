# Severstal-Steel-Defect-Detection

Steel is one of the most important building materials of modern times. Steel buildings are resistant to natural and man-made wear which has made the material ubiquitous around the world. To help make production of steel more efficient, this competition will help identify defects.

Severstal is leading the charge in efficient steel mining and production. They believe the future of metallurgy requires development across the economic, ecological, and social aspects of the industry—and they take corporate responsibility seriously. The company recently created the country’s largest industrial data lake, with petabytes of data that were previously discarded. Severstal is now looking to machine learning to improve automation, increase efficiency, and maintain high quality in their production.

The production process of flat sheet steel is especially delicate. From heating and rolling, to drying and cutting, several machines touch flat steel by the time it’s ready to ship. Today, Severstal uses images from high frequency cameras to power a defect detection algorithm.

## TensorRT

The core of NVIDIA® TensorRT is a C++ library that facilitates high-performance inference on NVIDIA graphics processing units (GPUs). It is designed to work in a complementary fashion with training frameworks such as TensorFlow, Caffe, PyTorch, MXNet, etc. It focuses specifically on running an already-trained network quickly and efficiently on a GPU for the purpose of generating a result (a process that is referred to in various places as scoring, detecting, regression, or inference).

Some training frameworks such as TensorFlow have integrated TensorRT so that it can be used to accelerate inference within the framework. Alternatively, TensorRT can be used as a library within a user application. It includes parsers for importing existing models from Caffe, ONNX, or TensorFlow, and C++ and Python APIs for building models programmatically.

<p align="center">
<img src = "https://github.com/SarthakGarg13/Severstal-Steel-Defect-Detection/blob/master/images/tensorrt.png">
</p>


TensorRT engine could be converted from the following frameworks using UFF parser, ONNX parser or TFTRT. The TensorRT API includes implementations for the most common deep learning layers. You can also use the C++ Plugin API or Python Plugin API to provide implementations for infrequently used or more innovative layers that are not supported out-of-the-box by TensorRT.

We have used the ONNX-Parser for the conversion Pytorch-TensorRT.
- Model is trained on Pytorch, and is saved as model.pth file. 
- Followed by converting .pth -> .onnx present in -simplify onnx model.html- 
- After converting model to onnx, we simplify it using the [Onnx-Simplifier](https://github.com/daquexian/onnx-simplifier).
-



<p align="center">
<img src = "https://github.com/SarthakGarg13/Severstal-Steel-Defect-Detection/blob/master/images/onnx-tensorrt.png">
</p>





## References

TensorRT Doc: https://docs.nvidia.com/deeplearning/tensorrt/developer-guide/index.html
Onnx simplifier https://github.com/daquexian/onnx-simplifier
Dataset link https://www.kaggle.com/c/severstal-steel-defect-detection/data
