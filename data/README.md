# Data

存放项目所需的所有数据文件，按处理阶段分为两类：

## 目录结构

```
data/
├── raw/          # 原始数据（不提交到 git）
├── processed/    # 处理后的数据（可提交小规模数据）
└── sample_*.csv  # 示例/样本数据（可提交）
```

## 使用方式

```python
import pandas as pd

# 加载原始数据
df_raw = pd.read_csv("data/raw/dataset.csv")

# 加载处理后数据
df = pd.read_csv("data/processed/train.csv")
```

> **注意**：大体积原始数据文件请使用 `.gitignore` 排除，或使用 Git LFS 管理。
