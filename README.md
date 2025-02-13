
# Deep Learning Training Configurations 🚀

[![GitHub Stars](https://img.shields.io/github/stars/Flulike/Config?style=social)](https://github.com/Flulike/Config)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Flulike/Config/pulls)

统一收集与分享深度学习训练配置，涵盖 **目标检测/实例分割** 等任务，支持多框架迁移与快速复现。

---

## 🛠 当前支持

### MMYOLO 配置库
```text
configs/
└── mmyolo/
    ├── yolov5/
    │   ├── yolov5_s-v61_syncbn_8xb16-300e_coco.py
    │   └── ... (不同变体/超参组合)
    ├── yolov6/
    ├── yolov7/
    └── ... (持续更新)
```
- **预训练模型**: YOLOv5/YOLOv6/YOLOv7 全系列
- **数据集适配**: COCO/VOC 开箱即用
- **优化策略**: 学习率warmup、EMA、SyncBN 等最佳实践集成

---

## 🚧 近期计划

### 框架扩展
| 框架          | 进度      | 特性预告                          |
|---------------|-----------|----------------------------------|
| MMDetection   | 🔜 Q3 2024 | Mask R-CNN/Cascade R-CNN 等经典模型 |
| Ultralytics   | 🔜 Q4 2024 | YOLOv8/YOLOv9 官方配置迁移         |

### 功能升级
- [ ] 新增 `docker/` 目录提供多框架训练环境
- [ ] 添加 `tools/` 可视化配置对比脚本
- [ ] 支持自定义数据集迁移指南

---

## � 快速使用
以 MMYOLO 训练为例：
```bash
# 进入目标配置目录
cd configs/mmyolo/yolov5

# 修改数据路径（可选）
sed -i 's/data_root = .*/data_root = "YOUR_COCO_PATH"/' yolov5_*.py

# 启动训练
mim train mmyolo $(ls *.py) --work-dir outputs/
```

---

## 🤝 参与贡献
欢迎通过以下方式丰富配置库：
1. 提交 Pull Request 添加新模型配置
2. 创建 Issue 报告参数调优问题
3. 在 Discussions 分享您的训练结果对比

---

> 📄 **License**  
> 本仓库采用 [MIT License](LICENSE)，配置可自由用于学术/商业项目。
