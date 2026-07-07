## [[English]](README.md)

# Alice’s Adventures in Wonderland · LaTeX 排版版  

## 项目简介

本仓库是刘易斯·卡罗尔《爱丽丝梦游仙境》英文原版的全书 LaTeX 排版源代码。全文采用经典的 **EB Garamond** 字体，以传统书籍版式精排，追求优雅、舒适的阅读体验。项目为纯文字版，**不含插图**。

### 英文词汇量与阅读难度

- **总词数**：约 26,500 词（完整原版）
- **蓝思值（Lexile）**：约 890L
- **适用水平**：适合词汇量在 3,500–4,000 以上的英语学习者，大致相当于中国大学英语四级（CET‑4）以上或中级英语阅读水平。对于高级英语学习者或原版书爱好者，是欣赏经典文学与精美排版的上佳选择。

## 构建指南

**编译环境要求：**

- 完整的 TeX 发行版（推荐 [TeX Live](https://tug.org/texlive/) 2024 或更新版本，也支持 [MiKTeX](https://miktex.org/)）
- 已安装 `ebgaramond` 字体包（TeX Live 中通常位于 `texlive-fonts-extra` 内）
- **必须使用 LuaLaTeX 编译**（因项目依赖 `fontspec` 调用系统字体）

**编译步骤：**

1. 克隆仓库
```bash
git clone https://github.com/your-username/alice-latex.git
cd alice-latex
```
2. 使用 LuaLaTeX 编译主文件

```bash
lualatex alice.tex
```

重要提示：LaTeX 需要解析目录、页码和交叉引用，请至少连续编译两次，才能生成正确的目录与书签。例如：

```bash
lualatex alice.tex
lualatex alice.tex
```

或使用自动化工具一次性完成：

```bash
latexmk -lualatex alice.tex
```

编译成功后，主 PDF 文件为 `alice_in_wonderland.pdf`。
亦可使用仓库中附带的 `Makefile` 执行 `make` 自动编译。

## 项目结构

```text
.
├── alice_in_wonderland.aux
├── alice_in_wonderland.log
├── alice_in_wonderland.pdf                # 主PDF
├── alice_in_wonderland.synctex.gz
├── alice_in_wonderland.tex                # 主文档
├── alice_in_wonderland.toc
├── LICENSE                                # CC BY‑SA 4.0
├── README-CN.md
└── README.md
```

项目不含插图，所有文件为纯文本 LaTeX 源码。

## 许可证

- 原始英文文本：公共领域（Public Domain），刘易斯·卡罗尔于 1865 年出版。

- LaTeX 排版代码（包括 `.tex`、`.cls`、样式文件等）：
[Creative Commons 署名-相同方式共享 4.0 国际（CC BY‑SA 4.0）](https://creativecommons.org/licenses/by-sa/4.0/legalcode.zh-hans)

- [EB Garamond](https://github.com/georgd/EB-Garamond) 字体：以 [SIL Open Font License](https://openfontlicense.org/open-font-license-official-text/) 1.1 发布。

- 你可以自由分享、修改本排版代码，但必须保留署名，且衍生作品需以相同许可证分发。

## 致谢

- 原著：Lewis Carroll

- 排版设计与 LaTeX 实现：klkjkj-a

- 字体：EB Garamond by Georg Mayr-Duffner & Octavio Pardo
