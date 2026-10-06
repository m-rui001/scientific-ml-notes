# Scientific ML Notes · 科学机器学习手稿与笔记

围绕**算子学习与科学机器学习**的讲稿、实验报告、推导笔记与配套代码，兼有部分数学分析与工具链调研。

## 主要内容

### 算子学习与神经代理
- **随机傅里叶特征（RFF）**：`Random_fourier_features.{typ,ipynb}`、`RFF.typ`、`CA_RFF.typ`（交叉注意力 + RFF）、`SimpleFourier.ipynb`
- **DeepONet**：`DeepONet.{typ,ipynb}`（配套复现另见 [DeepONetJAX](https://github.com/m-rui001/DeepONetJAX)）
- **PINN 与尺度分析**：`PINN.tex`、`ScalePinn.ipynb`、`ScalePINNandTINN.ipynb`、`PsiNN.ipynb`、`Spectral_bias.{typ,pdf}`、`TimeDependentWeight.typ`
- **核方法与注意力**：`kernel.{typ,py}`、`KerneliedAttention.ipynb`、`Report.{typ,pdf}`（交叉注意力谱偏置）

### 数学基础与笔记
- `MyNote.{typ,pdf}`：个人数学笔记总集（卓里奇补遗、分析专题等）
- `MathNote.md`、`prob_note1.typ`、`Laplace_method.typ`、`裴礼文theorem4_13.typ`、`homework_*.typ`
- `MIL.lean`：Lean 形式化尝试；`SaintPetersburg.{typ,pdf}`：圣彼得堡悖论

### 数据与求解器代码
- Burgers 方程数据生成：`gen_Burgers.m`、`gen_burger_data.py`、`Burgers.m`、`GRF.m`（高斯随机场）
- Adams–Bashforth/Runge 与自治系统：`AC_Runge.py`、`AC_torch.py`、`AC.mat`、`Butcher_IRK100.txt`
- 回归与绘图：`regression.py`、`plot.py`、`autograd.tex`、`backprop.tex`

### 工具链调研与工作流（中文）
- PDF → TeX → EPUB 工作流：`规划-*`、`调研-*`、`选型-*`、`决策-*.md`
- OCR 与文本质检实测：`pdf-craft-吞吐诊断-*.md`、`文本质检与OCR提速-*.md`

## 说明

Typst 文稿多数依赖同目录的 `ori.typ` 等共享 preamble，编译时请保持在仓库根目录内。参数与原始论文不完全一致，以笔记性质为准。

## License

MIT
