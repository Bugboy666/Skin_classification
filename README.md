# Skin_classification
## Background
使用改进的ConvNeXt模型对皮肤镜图像进行自动诊断

## 环境依赖
* python3.7
* pytorch 1.11.0
* torchvision 0.12.0

## Usage
1. 在`train.py`中将`--data-path`设置成数据集的路径，将`--weights`参数设成下载好的预训练权重路径，将`--num_classes`设置成相应的类别数
2. 在`create_confusion_matrix_convnext.py`中将 data_root 设置成测试集的路径，并将`model_weight_path`设置成训练好的模型权重路径，得到相应的混淆矩阵

## 目录结构描述
```
ConvNeXt
    │  create_confusion_matrix_convnext.py
    │  my_dataset.py
    │  predict.py
    │  README.md
    │  select_incorrect_samples.py
    │  self_defined_trunc_normal_.py
    │  train.py
    │  utils.py
    │  
    ├─attention_module
    │  │  NormalizationBased_Attention_Module.py
    │  │  SEAttention.py
    │  │  SE_Net.py
    │  └─ simam_module.py
    │       
    ├─data
    │ 
    ├─model
    │  │  model.py
    │  │  se_model.py
    │  │  simam_model0.py
    │  │  simam_model1.py
    │  │  simam_model2.py
    │  └─ simam_se_model.py
    │     
    └─weights
```
