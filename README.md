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

## 长篇设定与大纲（非技术内容）

仓库根目录另有 12 个 Markdown 文件，是一部长篇科幻小说的设定与分卷大纲，与科学机器学习笔记无关，单独归档在这里：

| 文件 | 内容 |
|---|---|
| `00_宇宙总纲.md` | 世界观、编年史、势力、术语表、母题系统 |
| `01_标注.md` … `10_余数.md` | 十卷各自的大纲：文学技法、人物、章节与写作指令 |
| `99_写作总要求.md` | 给执行写作的总规范与禁忌 |
| `MEMORY.md` | 设定速记与进度索引 |

这组文件的路径与文件名为历史原样，未并入技术笔记的编号体系；引用时按文件名直接访问。

## 说明

Typst 文稿多数依赖同目录的 `ori.typ` 等共享 preamble，编译时请保持在仓库根目录内。参数与原始论文不完全一致，以笔记性质为准。工作流报告中的本机路径已替换为 `<来源库>`、`<EPUB 工作区>` 等占位符。

## 已知缺失资产

22 个 `.typ` 中 12 个引用了未随仓库提交的图片、模板或 bib 文件，在干净克隆里无法单独编译：`DeepONet.typ`、`MyNote.typ`、`RFF.typ`、`Random_fourier_features.typ`、`Report.typ`、`SaintPetersburg.typ`、`TimeDependentWeight.typ`、`gene_regulatory_network.typ`、`kernel.typ`、`main.typ`、`实验报告.typ`、`实验报告2.typ`。缺的是 `assets/`、`touying-template/`、`probes/`、`bib/` 下的素材，正文源码完整。其余 10 个文稿可独立编译，整理后页码与 PDF 文本指纹未变。

## License

MIT
