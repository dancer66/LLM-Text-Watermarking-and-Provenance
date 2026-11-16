# LLM-Text-Watermarking-and-Provenance
Research on large language model (LLM) text watermarking for AI-generated content provenance, with a focus on watermark detection, robustness evaluation, and resistance to text manipulation attacks.

## A Watermark for Large Language Models

论文：John Kirchenbauer, Jonas Geiping, Yuxin Wen, Jonathan Katz, Ian Miers, Tom Goldstein. *A Watermark for Large Language Models*, ICML 2023.

- [论文](https://arxiv.org/abs/2301.10226)
- [作者官方代码仓库](https://github.com/jwkirchenbauer/lm-watermarking)
- 本仓库代码位置：[lm-watermarking/](lm-watermarking/)
- 导入分支：上游 `main`
- 上游提交：[`82922516930c02f8aa322765defdb5863d07a00e`](https://github.com/jwkirchenbauer/lm-watermarking/commit/82922516930c02f8aa322765defdb5863d07a00e)
- 导入日期：2026-11-16

`lm-watermarking/` 是该提交的完整文件快照，保留原始代码、README 和目录结构。上游仓库同时包含后续论文 *On the Reliability of Watermarks for Large Language Models* 的实现，位于 `watermark_reliability_release/`。

### 主要入口

| 路径（相对于 lm-watermarking/） | 用途 |
| --- | --- |
| `watermark_processor.py` | 基础水印生成与检测实现 |
| `extended_watermark_processor.py` | 扩展水印生成与检测实现 |
| `demo_watermark.py`、`app.py` | 演示入口 |
| `experiments/` | 原论文实验代码；上游已标记为旧版 |
| `watermark_reliability_release/` | 后续可靠性研究的实验与评估代码 |

### 启动演示

使用 Python 3.9 或以上版本，在独立环境中运行：

```bash
cd lm-watermarking
python -m pip install -r requirements.txt
python app.py
```

首次运行需要下载 Hugging Face 模型，具体参数及硬件需求参见[上游说明](lm-watermarking/README.md)。本次仅导入代码并核对文件完整性，尚未运行模型推理或复现实验。

### 许可证与来源

本仓库原有 [MIT LICENSE](LICENSE) 保留。导入的 `lm-watermarking/` 代码遵循上游 [Apache License 2.0](lm-watermarking/LICENSE.md)，原有版权与第三方来源声明一并保留；根目录 MIT 许可证不替代该目录的上游许可。
