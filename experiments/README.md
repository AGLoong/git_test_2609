# Experiments

实验记录目录，用于跟踪不同模型配置、超参数组合的训练实验结果。

## 目录结构

```
experiments/
├── configs/        # 实验配置文件（YAML/JSON）
├── runs/           # 每次运行的日志与输出
└── README.md
```

## 使用方式

```yaml
# configs/experiment_001.yaml
model: "ResNet50"
learning_rate: 0.001
batch_size: 32
epochs: 50
optimizer: "Adam"
```

```python
# 示例：读取实验配置
import yaml

with open("experiments/configs/experiment_001.yaml") as f:
    config = yaml.safe_load(f)
print(config)
```

## 日志管理

推荐使用 MLflow、Weights & Biases 或 TensorBoard 记录实验指标。
- MLflow 输出到 `mlruns/`（已加入 .gitignore）
- TensorBoard 事件文件已加入 .gitignore
