# Scientific ML Notes · 科学机器学习手稿与笔记

围绕**算子学习与科学机器学习**的讲稿、实验报告、推导笔记与配套代码，兼有数学分析与工具链调研。

## 目录

```
notes/
  typst/       22 个 .typ：讲稿、笔记、作业、报告
  latex/        9 个 .tex：推导、图示、论文源文件
  jupyter/      9 个 .ipynb：RFF、DeepONet、PINN、核方法实验
  markdown/     MathNote.md：数学笔记
code/
  python/       9 个 .py：数据生成、PINN 训练、可视化
  matlab/       3 个 .m：Burgers 方程求解与随机场生成
  wolfram/      ProjectEuler.m：Project Euler 题解脚本
  lean/         MIL.lean：形式化尝试
  r/            R 语言与生信分析讲稿（.rmd）
data/           AC.mat、Butcher_IRK100.txt：求解器输入数据
pdf/            编译产物：MyNote、Report、SaintPetersburg、Spectral_bias、main、实验报告、R 讲稿
reports/        工作流调研：PDF→TeX→EPUB 规划、选型、OCR 实测
novel/          《除不尽》设定与十卷大纲（与笔记无关，单独归档）
```

## 主要内容

### 算子学习与神经代理
- **随机傅里叶特征（RFF）**：`notes/typst/Random_fourier_features.typ`、`RFF.typ`、`CA_RFF.typ`（交叉注意力 + RFF）、`notes/jupyter/SimpleFourier.ipynb`
- **DeepONet**：讲稿源文件已删除（原文件是空模板），复现代码另见 [DeepONetJAX](https://github.com/m-rui001/DeepONetJAX)
- **PINN 与尺度分析**：`notes/latex/PINN.tex`、`ScalePinn.ipynb`、`ScalePINNandTINN.ipynb`、`PsiNN.ipynb`、`notes/typst/Spectral_bias.typ`、`TimeDependentWeight.typ`
- **核方法与注意力**：`notes/typst/kernel.typ`、`code/python/kernel.py`、`KerneliedAttention.ipynb`、`Report.typ`（交叉注意力谱偏置）

### 数学基础与笔记
- `notes/typst/MyNote.typ`：个人数学笔记总集（卓里奇补遗、分析专题等）
- `notes/markdown/MathNote.md`、`prob_note1.typ`、`Laplace_method.typ`、`裴礼文theorem4_13.typ`、`homework_*.typ`、`weistrass.typ`
- `code/lean/MIL.lean`：Lean 形式化尝试；`SaintPetersburg.typ`：圣彼得堡悖论

### 数据与求解器代码
- Burgers 方程数据生成：`code/matlab/gen_Burgers.m`、`code/python/gen_burger_data.py`、`Burgers.m`、`GRF.m`
- 自治系统 PINN：`code/python/AC_Runge.py`、`AC_torch.py`；数据在 `data/AC.mat`、`data/Butcher_IRK100.txt`，脚本按文件位置解析路径
- 回归与绘图：`code/python/regression.py`、`plot.py`、`time.py`、`玫瑰图.py`；`notes/latex/autograd.tex`、`backprop.tex`

### 工具链调研与工作流（中文）
- PDF → TeX → EPUB 工作流：`reports/规划-*`、`调研-*`、`选型-*`、`决策-*.md`
- OCR 与文本质检实测：`reports/pdf-craft-吞吐诊断-*.md`、`文本质检与OCR提速-*.md`

### 长篇设定与大纲（非技术内容）
`novel/` 下是长篇科幻小说的设定与分卷大纲：`00_宇宙总纲.md`、`01_标注.md` … `10_余数.md`、`99_写作总要求.md`、`MEMORY.md`。

## 编译

Typst 文稿统一在 `notes/typst/`，共享 preamble `ori.typ` 同目录，从仓库根编译：

```sh
typst compile --root . notes/typst/Spectral_bias.typ
```

LaTeX 文稿在 `notes/latex/`，`pdflatex main.tex` 两遍。

## 本次整理记录

- 根目录 94 个文件按类型归入 `notes/`、`code/`、`data/`、`pdf/`、`reports/`、`novel/`。
- 删除：空模板 `DeepONet.typ`、空笔记本 `DeepONet.ipynb`、运行产物 `errors_list.pkl`、编辑器配置 `Work.code-workspace`、与本仓库无关的 `目录结构.md`（描述的是另一个 EPUB 工作区）和 2 字节占位文件 `ZaiHuan/1`。
- 与仓库主题无关的 SillyTavern 角色卡 `灵灵.json` 已移出仓库。
- 工作流报告中的本机路径替换为 `<来源库>`、`<EPUB 工作区>` 等占位符。
- 可独立编译的 10 个 `.typ` 按统一规则整理了排版，页码与 PDF 文本指纹逐文件一致；引用缺失素材的 12 个文件保持原样。

## 已知缺失资产

`notes/typst/` 中 11 个 `.typ` 引用了未随仓库提交的图片、模板或 bib 文件，在干净克隆里无法单独编译：`MyNote.typ`、`RFF.typ`、`Random_fourier_features.typ`、`Report.typ`、`SaintPetersburg.typ`、`TimeDependentWeight.typ`、`gene_regulatory_network.typ`、`kernel.typ`、`main.typ`、`实验报告.typ`、`实验报告2.typ`。缺的是 `assets/`、`touying-template/`、`probes/`、`bib/` 下的素材，正文源码完整。其余 10 个文稿可独立编译。

## License

MIT
