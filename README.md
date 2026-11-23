# open-temporal-bias

An open set bias discovery technique for video generation models, borrowing from
[OpenBias](https://github.com/Picsart-AI-Research/OpenBias).

## Setup

```bash
uv sync
```

- Local machine needs CUDA 12.8 or newer.
- Sync yet to be tested on the cluster (A30). The cluster driver (550, CUDA 12.4)

```bash
uv run python -c "import torch; print(torch.__version__, torch.version.cuda, torch.cuda.is_available()); x=torch.randn(1024,1024,device='cuda',dtype=torch.bfloat16); print((x@x).sum().item())"
```

If the cluster reports `CUDA driver version is insufficient`, switch the index in
`pyproject.toml` to `https://download.pytorch.org/whl/cu126` (A30 only).
