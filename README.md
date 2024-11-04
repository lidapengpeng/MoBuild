# 🚀 MoBuild

<div align="center">

[![Python 3.7+](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)
[![Documentation Status](https://readthedocs.org/projects/mobuild/badge/?version=latest)](https://mobuild.readthedocs.io)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/yourname/mobuild/pulls)

**一个模块化的多模态目标检测和分割框架**

[📘使用文档](docs/getting_started.md) | [🛠️安装指南](docs/install.md) | [📊模型库](docs/model_zoo.md) | [🤝贡献指南](docs/contribute.md)

</div>

## 🌟 主要特性

- 🔧 **模块化设计**：每个组件都是独立的，易于扩展和修改
- 🔄 **多模态支持**：
  - 🖼️ 图像处理：支持 ResNet、Swin Transformer 等主干网络
  - ☁️ 点云处理：支持 PointNet、DGCNN 等网络
- 🎯 **多任务支持**：
  - 📦 目标检测：支持 FCOS、Anchor-based 等检测器
  - 🎨 语义分割：支持 FCN、PSP 等分割模型
- 🔗 **特征融合**：提供注意力机制和简单拼接等多种特征融合方式
- 📊 **灵活的数据处理**：统一的数据加载和预处理接口
- 📈 **丰富的评估指标**：支持检测和分割的多种评估方式

## 📁 项目结构

```plaintext
MoBuild/
├── configs/                    # 配置文件目录
│   ├── __init__.py            # 配置初始化
│   └── base/
│       └── default.py         # 默认配置
├── data/                      # 数据处理模块
│   ├── __init__.py           # 数据处理初始化
│   ├── transforms/           # 数据变换
│   │   └── compose.py       # 组合变换
│   └── modalities/          # 多模态数据处理
│       └── point.py         # 点云数据处理
├── models/                   # 模型定义
│   ├── __init__.py          # 模型初始化
│   ├── backbones/           # 主干网络
│   │   ├── image/          # 图像主干网络
│   │   │   └── __init__.py
│   │   └── point/          # 点云主干网络
│   │       ├── __init__.py
│   │       ├── pointnet.py # PointNet系列
│   │       └── dgcnn.py    # DGCNN网络
│   └── heads/              # 任务头
│       └── detection/      # 检测头
│           └── fcos_head.py # FCOS检测头
├── tools/                   # 工具脚本
│   └── visualize.py        # 可视化工具
└── utils/                  # 通用工具
    ├── losses/            # 损失函数
    │   ├── __init__.py
    │   ├── focal_loss.py # Focal Loss
    │   └── seg_loss.py   # 分割损失
    └── metrics/          # 评估指标
        ├── __init__.py
        ├── detection.py  # 检测评估
        └── segmentation.py # 分割评估
```

## 🚀 快速开始

1. **安装依赖**
```bash
pip install -r requirements.txt
```

2. **准备数据**
请参考[数据准备文档](docs/data_preparation.md)

3. **训练模型**
```bash
python tools/train.py configs/your_config.py
```

4. **评估模型**
```bash
python tools/test.py configs/your_config.py checkpoints/your_model.pth
```

## 📚 文档

详细文档请访问我们的[在线文档](https://mobuild.readthedocs.io/)。

## 🤝 贡献

我们欢迎任何形式的贡献，包括但不限于:

- 提交问题和建议
- 提交代码改进
- 改进文档
- 分享使用经验

请参考[贡献指南](docs/contribute.md)了解更多细节。

## 📄 开源协议

本项目采用 [Apache 2.0 开源协议](LICENSE)。
```

