# Yuvion 单栏论文模板（NeurIPS 风格）

基于团队现有 CVPR 双栏模板，新增 NeurIPS 2026 风格的单栏技术报告模板。
保留 Alibaba Security / Yuvion 双 Logo 页眉、页脚页码、团队署名以及原有发表流程说明。

[下载 Overleaf ZIP](yuvion-neurips-template.zip) · [查看 PDF 预览](yuvion-neurips-preview.pdf)

本目录为独立的单栏版本，仓库根目录的 CVPR 双栏模板保持不变。
从仓库运行本地编译前，请先 `cd neurips`。

## Overleaf

1. New Project → Upload Project，上传本模板 ZIP。
2. 将 `yuvion_team_neurips.tex` 设置为 Main document。
3. 编译器选择 pdfLaTeX；替换标题、作者、邮箱、摘要和正文。
4. 在 `references.bib` 中维护参考文献。

## 本地编译

```sh
latexmk -pdf yuvion_team_neurips.tex
```

没有 latexmk 时：

```sh
pdflatex yuvion_team_neurips.tex
bibtex yuvion_team_neurips
pdflatex yuvion_team_neurips.tex
pdflatex yuvion_team_neurips.tex
```

也支持 `tectonic yuvion_team_neurips.tex`。

## 文件

| 文件 | 用途 |
| --- | --- |
| `yuvion_team_neurips.tex` | 主文件，包含公式、图、表、算法、引用和附录示例 |
| `neurips_2026.sty` | 官方样式文件，原样保留 |
| `yuvion-neurips.sty` | 品牌页眉及团队技术报告脚注 |
| `references.bib` | 示例参考文献 |
| `team_publication_workflow.tex` | 从原模板保留的内部发表及开源流程说明 |
| 两张 PNG | 从原模板保留的团队品牌素材 |

默认正文为 5.5 × 9 英寸单栏，US Letter，10pt 正文/11pt 行距；作者用 `\And` 分隔。
使用 `\linewidth` 指定图表宽度，无须使用 `figure*`、`table*` 或 `twocolumn`。

这是带团队身份的技术报告模板。正式匿名投稿请使用会议原始 author kit，
移除团队页眉、内部流程说明和身份信息，并按会议要求配置 checklist。
正文中的原始内部流程链接随源模板保留，公开发布前请检查是否应移除。

## 来源

- 团队原始双栏模板：https://github.com/Alibaba-VELLDEPTH/yuvion-paper-template
- 原始版本：`acc481afe3308def1caafbf662d2f3690290f7ab`
- NeurIPS 2026 官方 CFP：https://neurips.cc/Conferences/2026/CallForPapers
- CFP 链接的官方 author kit：https://media.neurips.cc/Conferences/NeurIPS2026/Formatting_Instructions_For_NeurIPS_2026.zip

官方样式的原始作者说明保留在文件头。品牌素材及原团队内容归原权利人所有；
本模板不另行授予这些素材的商标或版权许可。

## 编译验证

已使用 Tectonic 0.17.0 完成编译，并逐页检查 4 页 PDF 的页眉、公式、图表、引用和附录。
