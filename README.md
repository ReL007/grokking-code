# 支持命令行参数的神经网络训练脚本

该脚本提供了一个灵活的框架，用于训练神经网络模型，允许通过命令行参数自定义超参数和配置,旨在验证深度学习中的 **Grokking 现象**。

Grokking 是指神经网络在训练数据上达到完全拟合后，经过较长时间的训练，突然在测试集上也达到了高性能。该现象通常出现在规则性或结构性较强的数据集上。

---

## 主要特点

- **专为验证 Grokking 现象设计**：支持在数学任务K个数模加法上观察 Grokking。
- **可配置的训练超参数**：例如学习率、批量大小、权重衰减等，方便实验设计。
- **支持多种模型架构**：如 Transformer，MLP和 LSTM。
- **多种优化器选项**：提供 AdamW、Sophia 、RMSprop、Momentum等优化器。
- **支持 Dropout 正则化**：调整以观察其对 Grokking 现象的影响。
- **设备可选择**：支持在 CPU 或 GPU（`cuda`）上运行。
- **使用实验追踪工具**：集成 Weights and Biases (`wandb`) 进行实验可视化和结果记录。

---

## 使用方法

本项目使用 [Weights & Biases](https://wandb.ai/site) 来追踪实验进度。运行 `wandb login` 登录以使用在线仪表板，或者运行 `wandb offline` 将数据存储在本地计算机上。

请确保您的 Python 版本为 **3.9.19**，以确保脚本的兼容性。您可以通过以下命令检查 Python 版本：

```bash
python --version
```

通过以下命令在命令行运行脚本：
```bash
python main.py
