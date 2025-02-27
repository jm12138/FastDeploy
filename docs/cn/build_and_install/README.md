[English](../../en/build_and_install/README.md) | 中文

# FastDeploy安装

## FastDeploy预编译库安装
- [FastDeploy预编译库下载安装](download_prebuilt_libraries.md)

## 自行编译安装
- [GPU部署环境](gpu.md)
- [CPU部署环境](cpu.md)
- [IPU部署环境](ipu.md)
- [Jetson部署环境](jetson.md)
- [Android平台部署环境](android.md)
- [瑞芯微RV1126部署环境](rv1126.md)
- [瑞芯微RK3588部署环境](rknpu2.md)
- [晶晨A311D部署环境](a311d.md)
- [昆仑芯XPU部署环境](xpu.md)


## FastDeploy编译选项说明

| 选项                      | 说明                                                                        |
|:------------------------|:--------------------------------------------------------------------------|
| ENABLE_ORT_BACKEND      | 默认OFF, 是否编译集成ONNX Runtime后端(CPU/GPU上推荐打开)                                 |
| ENABLE_PADDLE_BACKEND   | 默认OFF，是否编译集成Paddle Inference后端(CPU/GPU上推荐打开)                             |  
| ENABLE_LITE_BACKEND     | 默认OFF，是否编译集成Paddle Lite后端(编译Android库时需要设置为ON)                          |
| ENABLE_RKNPU2_BACKEND   | 默认OFF，是否编译集成RKNPU2后端(RK3588/RK3568/RK3566上推荐打开)                           |
| WITH_XPU                | 默认OFF，当在昆仑芯XPU上部署时，需设置为ON                                                |
| WITH_TIMVX              | 默认OFF，需要在RV1126/RV1109/A311D上部署时，需设置为ON                                   |
| ENABLE_TRT_BACKEND      | 默认OFF，是否编译集成TensorRT后端(GPU上推荐打开)                                          |
| ENABLE_OPENVINO_BACKEND | 默认OFF，是否编译集成OpenVINO后端(CPU上推荐打开)                                          |
| ENABLE_VISION           | 默认OFF，是否编译集成视觉模型的部署模块                                                     |
| ENABLE_TEXT             | 默认OFF，是否编译集成文本NLP模型的部署模块                                                  |
| WITH_GPU                | 默认OFF, 当需要在GPU上部署时，需设置为ON                                                 |
| RKNN2_TARGET_SOC        | ENABLE_RKNPU2_BACKEND时才需要使用这个编译选项。无默认值, 可输入值为RK3588/RK356X, 必须填入，否则 将编译失败 |
| CUDA_DIRECTORY          | 默认/usr/local/cuda, 当需要在GPU上部署时，用于指定CUDA(>=11.2)的路径                        |
| TRT_DIRECTORY           | 当开启TensorRT后端时，必须通过此开关指定TensorRT(>=8.4)的路径                                |
| ORT_DIRECTORY           | 当开启ONNX Runtime后端时，用于指定用户本地的ONNX Runtime库路径；如果不指定，编译过程会自动下载ONNX Runtime库  |
| OPENCV_DIRECTORY        | 当ENABLE_VISION=ON时，用于指定用户本地的OpenCV库路径；如果不指定，编译过程会自动下载OpenCV库              |
| OPENVINO_DIRECTORY      | 当开启OpenVINO后端时, 用于指定用户本地的OpenVINO库路径；如果不指定，编译过程会自动下载OpenVINO库             |
