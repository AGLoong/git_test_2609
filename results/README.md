# Results

存放模型训练和实验的输出结果，包括可视化图表、预测结果和性能指标。

## 目录结构

```
results/
├── figures/        # 论文用图（loss 曲线、混淆矩阵、t-SNE 可视化等）
├── predictions/    # 模型预测结果（CSV/NPY）
├── metrics/        # 性能指标汇总（JSON/CSV）
└── README.md
```

## 使用方式

```python
import json
import matplotlib.pyplot as plt

# 保存指标
metrics = {"accuracy": 0.95, "f1": 0.93}
with open("results/metrics/exp_001.json", "w") as f:
    json.dump(metrics, f, indent=2)

# 保存图表
fig, ax = plt.subplots()
ax.plot([1, 2, 3], [0.5, 0.3, 0.1])
ax.set_title("Training Loss")
fig.savefig("results/figures/loss_curve.png", dpi=150)
```
