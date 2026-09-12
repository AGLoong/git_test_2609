# AI Research Project

面向人工智能方向的科研论文写作项目，涵盖从数据处理、实验记录、模型训练到论文文档撰写的完整工作流。

## 目录结构

| 目录 | 用途 |
|------|------|
| [`data/`](data/) | 原始数据、处理后数据及样本数据 |
| [`src/`](src/) | 项目源代码 |
| [`notebooks/`](notebooks/) | Jupyter Notebook，用于数据分析与探索 |
| [`experiments/`](experiments/) | 实验配置与运行记录 |
| [`checkpoints/`](checkpoints/) | 模型权重与训练检查点 |
| [`results/`](results/) | 实验结果、指标与可视化图表 |
| [`docs/`](docs/) | 论文草稿、插图与参考文献 |

## 快速开始

```bash
# 克隆仓库
git clone https://github.com/AGLoong/git_test_2609.git
cd git_test_2609

# 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 安装依赖
pip install -r requirements.txt

# 启动 Jupyter Notebook
jupyter notebook
```

## Git 常用命令

### 基础操作

```bash
# 初始化仓库
git init

# 克隆远程仓库
git clone <repository-url>

# 查看状态
git status

# 查看提交历史
git log --oneline

# 查看文件变更
git diff

# 暂存文件
git add <file>          # 暂存单个文件
git add .               # 暂存所有文件

# 提交
git commit -m "提交信息"

# 推送到远程
git push origin main

# 拉取远程更新
git pull origin main
```

### 分支管理

```bash
# 查看所有分支
git branch -a

# 创建新分支
git checkout -b <branch-name>

# 切换分支
git checkout <branch-name>

# 合并分支
git merge <branch-name>

# 删除本地分支
git branch -d <branch-name>

# 删除远程分支
git push origin --delete <branch-name>
```

### 标签与版本

```bash
# 创建标签
git tag v1.0.0

# 推送所有标签
git push origin --tags

# 查看标签
git tag -l
```

### 撤销与回退

```bash
# 撤销工作区修改（未暂存）
git checkout -- <file>

# 撤销暂存
git reset HEAD <file>

# 回退到指定提交（保留工作区）
git reset --soft <commit-hash>

# 硬重置（丢弃所有后续修改，谨慎使用）
git reset --hard <commit-hash>
```

### 远程仓库

```bash
# 查看远程仓库
git remote -v

# 添加远程仓库
git remote add origin <url>

# 修改远程仓库地址
git remote set-url origin <new-url>
```

### 解决冲突

```bash
# 编辑冲突文件后标记为已解决
git add <file>

# 完成合并提交
git commit -m "解决冲突"
```

## Git 工作流

本项目采用 **GitHub Flow** 工作流：

```
main (受保护分支)
  ├── 创建 feature 分支
  ├── 开发并提交
  ├── 推送到远程
  ├── 创建 Pull Request
  ├── 代码审查
  └── 合并到 main
```

## 提交信息规范

建议遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
<type>(<scope>): <description>

feat:     新功能
fix:      修复 bug
docs:     文档更新
refactor: 代码重构
test:     测试相关
chore:    构建/工具变更
```

示例：

```
feat(data): 添加数据清洗脚本
fix(experiments): 修复训练损失计算错误
docs: 更新 README 使用说明
```

## License

MIT
