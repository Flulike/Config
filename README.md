
# Deep Learning Training Configurations 🚀

[![GitHub Stars](https://img.shields.io/github/stars/Flulike/Config?style=social)](https://github.com/Flulike/Config)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Flulike/Config/pulls)

统一收集与分享深度学习训练配置，主要实现 **目标检测** 任务，支持多框架迁移与快速复现。

---

## 🛠 当前支持

### MMYOLO 配置库
```text
configs/
└── mmyolo/
    ├── yolov8_s_carclass.py # cctv v8s
    ├── yolov8_x_visdrone.py # visdrone v8s
    └── ... (持续更新)
└── ultralytics/ 
    ├── cfg/ 
    ├──── carclass.yaml  # dataset config 
    ├── train/ # 建议里面的文件拿出来放在与ultralytics包相同的文件下使用
    ├──── train_detr.py
    ├──── train_yolo.py  
    └── ... (持续更新)
```
- **预训练模型**: YOLO全系列
- **数据集适配**: COCO/yolo 开箱即用
- **优化策略**: 学习率warmup、EMA、SyncBN 等最佳实践集成

---

## 🚧 近期计划

### 框架扩展
| 框架          | 进度      | 特性预告                          |
|---------------|-----------|----------------------------------|
| MMDetection   | 🔜 2 2024 | RNN-based, DETR-base等方法 |
| Ultralytics   | 🔜 3 2024 | YOLOv10/YOLO11/RT-DETR 官方配置迁移,  包括一些基于ultralytics开发的       |

### 未来升级
- [ ] 新增 `docker/` 目录提供多框架训练环境
- [ ] 添加 `tools/` 可视化配置对比脚本
- [ ] 支持自定义数据集迁移指南

---

## � 快速使用
以 MMYOLO 训练为例：
```bash
#mmyolo例
python tools/train.py  config/mmyolo/yolov8_s_carclass.py

---

## 🤝 参与贡献
欢迎通过以下方式丰富配置库：
1. 提交 Pull Request 添加新模型配置
2. 创建 Issue 报告参数调优问题
3. 在 Discussions 分享您的训练结果对比

---

> 📄 **License**  
> 本仓库采用 [MIT License](LICENSE)，配置可自由用于学术/商业项目。
