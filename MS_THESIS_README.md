# 孟帅论文 LaTeX 版说明

本目录已新增一套不覆盖模板示例的论文入口文件：

- `ms-thesis.tex`：最新版论文主入口；
- `ms-thusetup.tex`：题名、作者、院系、专业、导师、宏包与图片路径配置；
- `data/ms-*.tex`：摘要、正文 7 章、参考文献、附录、致谢、符号说明、综合论文训练记录表；
- `figures/ms_thesis/`：从最新版论文迁入的全部正文图片；
- `tools/build_thuthesis_from_latest.py`：位于仓库根目录，可从最新版 Markdown 重新生成上述 LaTeX 文件。

## 编译方式

如果当前 TeX 发行版已安装 `thuthesis` 类，直接在本目录运行：

```powershell
latexmk -xelatex ms-thesis.tex
```

如果本目录中还没有 `thuthesis.cls`，可先根据模板源码生成：

```powershell
xelatex thuthesis.ins
latexmk -xelatex ms-thesis.tex
```

也可以使用 TeX Live / MiKTeX 自带的 `thuthesis` 包编译。

## 本次转换口径

LaTeX 版内容来自 `docs/thesis_02/基于大数据的佛山市南海区旅游景区文旅融合潜力研究_md转化版.md`，已包含题目改为“基于多源数据”、权重敏感性检验、评论文化识别度抽样检验、图 4.2/4.3 放大图、图 6.9/6.10、表 7.1 及更新后的附录样例。

本机已安装 MiKTeX，并通过 Git 自带 Perl 运行 `latexmk` 完成本地编译；PDF 已导出为 `ms-thesis.pdf`。若在刚打开的旧终端里仍提示找不到 `xelatex` 或 `latexmk`，关闭后重新打开 PowerShell 即可刷新用户 PATH。
