# 论文完成度与知网查重识别检查报告

检查时间：2026-05-31 14:09

## 一、模板与通知中的关键要求

1. 学校通知强调电子版论文应提交 PDF 版本，避免 Word/WPS 在不同机器上出现格式变化。
2. 查重系统对 PDF 的关键要求是文本能被正确解析。通知中特别提醒，部分 LaTeX 生成的 PDF 可能识别失败，因此应做复制文本或另存 TXT 的自检。
3. 自检标准：PDF 内容能正确复制到 Word，或 PDF 转 TXT 后文字顺序和中文内容基本正确，即可认为具备查重识别基础。
4. 查重统计通常不含目录、声明、参考文献，附录部分不查重；系统字符数过短或过长会影响检测。
5. 模板结构包括封面、授权说明、中文摘要、英文摘要、目录、插图清单、附表清单、符号说明、正文、参考文献、附录、致谢、声明等。

## 二、当前 PDF 识别性检查

论文 PDF：
`C:\Users\ms\Desktop\thesis\ms_thuthesis\ms-thesis.pdf`

检查结果：

- PDF 已重新编译成功，当前为 70 页，A4 页面，未加密。
- `pdffonts` 检查显示主要中文和英文字体均为 `emb yes`、`sub yes`、`uni yes`，说明字体已嵌入并带 Unicode 映射。
- `pdftotext -enc UTF-8 -nopgbrk` 可正常抽取中文文本。
- TXT 抽取文件：
  `C:\Users\ms\Desktop\thesis\ms_thuthesis\_completion_check\ms-thesis_pdftotext.txt`
- 抽取文本约 62,052 字符，其中中文字符约 27,822 个；未发现替换字符 `�` 或 `(cid:)` 乱码标记。
- 目录中的 `3.2.5 政府普查文化载体` 已正常显示，原来的“主桥梁清单”未再出现。

结论：当前 PDF 不是扫描图像版，而是可复制、可检索、可抽取文本的 PDF，满足学校通知中对 LaTeX PDF 提交前的识别性自检要求。

## 三、本次已修正的问题

1. 删除目录小节标题中的“（主桥梁清单）”，保留为“政府普查文化载体”。
2. 修正第 3 章表号顺序：
   - 表 3.2 评论平台来源与覆盖构成
   - 表 3.3 165 条核心文化载体按类型分布
3. 修复“附表清单”为空的问题。当前 `.lot` 已写入 21 个表条目，PDF 中附表清单页已正常显示。
4. 前置页复核截图已重新导出：
   `C:\Users\ms\Desktop\thesis\ms_thuthesis\_completion_check\frontmatter_page_after_content_audit-10.png`
   `C:\Users\ms\Desktop\thesis\ms_thuthesis\_completion_check\frontmatter_page_after_content_audit-11.png`
   `C:\Users\ms\Desktop\thesis\ms_thuthesis\_completion_check\frontmatter_page_after_content_audit-12.png`

## 四、提交前仍需人工确认

1. 封面信息：题目、姓名、学号、导师姓名、日期是否完全符合学院最终要求。
2. 授权说明与声明页：如系统或学院要求签字版，需要另行处理签名/扫描要求。
3. “在学期间参加课题的研究成果”和“综合论文训练记录表”：模板中有相应页面或表格，但它们通常属于归档/签字材料；除非学院明确要求放入查重 PDF，否则不建议并入查重稿。
4. 参考文献真实性与格式仍建议最后人工核对 DOI、期刊、年份、页码等细节。
5. 提交知网前，建议直接上传当前 `ms-thesis.pdf`，不要再经过 Word 二次转换，以免破坏版面或字体映射。
