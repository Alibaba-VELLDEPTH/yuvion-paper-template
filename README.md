# Yuvion Paper Templates

Yuvion Team, Alibaba Group 的论文模板，按版式独立存放。

| 版本 | 目录 | 主文件 |
| --- | --- | --- |
| Double-column | [double-column/](double-column/) | `yuvion_team_template.tex` |
| Single-column | [single-column/](single-column/) | `yuvion_team_neurips.tex` |

## 使用方式

- **Double-column**：将 `double-column/` 目录中的文件打包上传到新的 Overleaf 项目，选择 `yuvion_team_template.tex` 为主文件。原模板内容保持不变，仅移动目录。
- **Single-column**：直接下载 [Overleaf ZIP](single-column/yuvion-neurips-template.zip)，也可先查看 [PDF 预览](single-column/yuvion-neurips-preview.pdf)。
- 本地编译前先进入对应目录，再运行 `latexmk -pdf <主文件>`；两套模板的资源文件均包含在各自目录中。

具体说明见 [Double-column README](double-column/README.md) 和 [Single-column README](single-column/README.md)。
