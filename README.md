# Yuvion Paper Templates

Yuvion Team, Alibaba Group 的论文模板，按版式独立存放。

| 版本 | 目录 | 主文件 |
| --- | --- | --- |
| CVPR 双栏 | [cvpr/](cvpr/) | `yuvion_team_template.tex` |
| NeurIPS 单栏 | [neurips/](neurips/) | `yuvion_team_neurips.tex` |

## 使用方式

- **CVPR**：将 `cvpr/` 目录中的文件打包上传到新的 Overleaf 项目，选择 `yuvion_team_template.tex` 为主文件。原模板内容保持不变，仅移动目录。
- **NeurIPS**：直接下载 [Overleaf ZIP](neurips/yuvion-neurips-template.zip)，也可先查看 [PDF 预览](neurips/yuvion-neurips-preview.pdf)。
- 本地编译前先进入对应目录，再运行 `latexmk -pdf <主文件>`；两套模板的资源文件均包含在各自目录中。

具体说明见 [CVPR README](cvpr/README.md) 和 [NeurIPS README](neurips/README.md)。
