# AGENTS.md — NWPU 本科毕业论文

## 构建与测试

```bash
make thesis              # 构建 bachelor.pdf (调用 latexmk -xelatex)
make view                # 构建并打开 PDF
make test                # 运行 l3build 测试套件
make clean               # 清理辅助文件
make wordcount           # 字数统计
```

- 引擎: **XeLaTeX** (不可用 pdfLaTeX/LuaLaTeX)
- 参考文献: **biber** (不可用 bibtex)
- 字体: `fontset = windows` (bachelor.tex 硬编码)

## 文件结构

```
bachelor.tex             # 入口 (documentclass → \input{thesis-body})
thesis-body.tex          # 正文骨架 (\frontmatter / \mainmatter / \backmatter)
content/thesis/undergraduate/
  info.tex               # 个人信息
  abstract.tex           # 摘要
  chapters.tex           # 各章节 \input 列表
  chapter1.tex           # 绪论
  chapter2.tex           # 相关技术基础
  ...
  chapter7.tex           # 总结与展望
  reference.bib          # 参考文献 (biblatex)
  appendix.tex           # 附录
  acknowledgements.tex   # 致谢
  designsummary.tex      # 毕业设计小结
```

## 编辑约定，必须遵守

- **任何修改必须先征得用户同意再执行**
- **任何任务都要遵守八荣八耻原则**
- **任何修改都要查证physlucid代码库和相关论文以确保准确性**
- **任何修改都要保持论文整体风格和技术细节的一致性**
- **任何修改都要确保论文内容的科学性和技术深度**
- Don't use AI-sounding phrases
- Write like a CVPR/ICCV/NeurIPS paper
- Be concise, direct, factual
- No "firstly, secondly" AI scaffolding**

# 八荣八耻
- 以瞎猜接口为耻，以认真查询为荣。
- 以模糊执行为耻，以寻求确认为荣。
- 以臆想业务为耻，以人类确认为荣。
- 以创造接口为耻，以复用现有为荣。
- 以跳过验证为耻，以主动测试为荣。
- 以破坏架构为耻，以遵循规范为荣。
- 以假装理解为耻，以诚实无知为荣。
- 以盲目修改为耻，以谨慎重构为荣。