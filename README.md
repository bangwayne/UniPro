<div align="center">

<h1>UniPro</h1>
<h3>Unified Multi-Mode Medical Image Segmentation<br>from 2D Images to 3D Volumes via Propagation</h3>

<p>
  <a href="https://arxiv.org/abs/2610.06938"><img src="https://img.shields.io/badge/NeurIPS-2026-2563eb" alt="NeurIPS 2026"></a>
  <a href="https://arxiv.org/abs/2610.06938"><img src="https://img.shields.io/badge/arXiv-2610.06938-b31b1b" alt="arXiv paper"></a>
  <a href="#code-release"><img src="https://img.shields.io/badge/Code-In%20Preparation-d97706" alt="Code in preparation"></a>
</p>



<p><a href="https://arxiv.org/abs/2610.06938"><b>Paper</b></a> · <a href="https://arxiv.org/pdf/2610.06938"><b>PDF</b></a> · <a href="#citation"><b>Citation</b></a></p>

</div>

## Overview

**One model, four segmentation modes, across 2D images and 3D volumes.**

UniPro brings automatic prediction, reference-guided segmentation, interactive correction, and volumetric propagation into a shared framework. Its key idea is simple: **propagation is in-context segmentation over neighboring slices**. The same model can use an annotated example from another image or a previously segmented slice within a scan to guide its next prediction.

<p align="center">
  <img src="assets/unipro_overview.png" alt="UniPro architecture and two-stage training: a shared model supports semantic, in-context, interactive, and propagation-based segmentation." width="100%">
</p>

<p align="center"><em>UniPro's unified segmentation pipeline and two-stage training strategy.</em></p>

### Four ways to segment

| Mode | Guidance | Capability |
| :--- | :--- | :--- |
| **Semantic** | Target anatomical class | Automatically segment a known structure. |
| **In-context** | Reference images and masks | Segment a target using annotated examples. |
| **Interactive** | User clicks | Create or refine a segmentation through local corrections. |
| **Propagation** | Segmented neighboring slices | Extend an initial segmentation through a 3D scan. |

### Highlights

- **A shared model across modes and dimensions.** One slice-based framework supports native 2D images and 3D volumes while retaining local editability.
- **Two-stage training.** Joint training across semantic, in-context, and interactive tasks is followed by propagation adaptation with bidirectional and 3D consistency supervision.
- **Evaluation on 14 medical imaging datasets.** Experiments cover diverse modalities and anatomies, with fewer clicks and slices requiring correction in simulated interactive 3D editing.

## Code release

> [!NOTE]
> **The code is currently being organized and documented for public release.**
> We will publish the implementation and usage instructions in this repository once they are ready. Thank you for your interest and patience!

## Citation

If you find this work useful, please consider citing our paper:

```bibtex
@article{guo2026unipro,
  title={UniPro: Unified Multi-Mode Medical Image Segmentation from 2D Images to 3D Volumes via Propagation},
  author={Guo, Bangwei and Gao, Yunhe and Ye, Meng and Zhou, Yang and Gu, Difei and Zhang, Guoning and Axel, Leon and Metaxas, Dimitris},
  journal={arXiv preprint arXiv:2610.06938},
  year={2026}
}
```
