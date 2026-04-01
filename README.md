# Mousse: Rectifying the Geometry of Muon with Curvature-Aware Preconditioning

[![Paper](https://img.shields.io/badge/Paper-Arxiv-red.svg)](https://arxiv.org/abs/2603.09697) [![Blog](https://img.shields.io/badge/Blog-Post-blue.svg)](https://anti-entrophic.github.io/posts/10054.html)

This repo is modified from [Dion](https://github.com/microsoft/dion/tree/main). We sincerely thank the authors for their great work!

## Quick Start

Clone or unpack the repository, then install the package from the `dion/` directory:

```bash
cd dion
pip install -e .[train]
```

To download a pretokenized FineWeb subset used by the training script:

```bash
cd dion
python data/cached_fineweb100B.py 200
```

Run one of the provided training configurations with:

```bash
cd dion
torchrun --standalone --nproc_per_node=8 train.py --config configs/mousse_160m.yaml
```

The detailed project documentation can be found in `dion/README.md`.
