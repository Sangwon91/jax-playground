# Installation

> Source: https://milkclouds.work/jogaggeul-poetryro-jax-pytorch-seolci/
```
poetry source add -p supplemental jaxlib https://storage.googleapis.com/jax-releases/jax_cuda_releases.html
poetry add "jax[cuda11_pip]"
poetry source add pypi
```
> 마지막 줄이 필요한 이유: Warning: In a future version of Poetry, PyPI will be disabled automatically if at least one custom source is configured with another priority than 'explicit'. In order to avoid a breaking change and make your pyproject.toml forward compatible, add PyPI explicitly via 'poetry source add pypi'. By the way, this has the advantage that you can set the priority of PyPI as with any other source.
> poetry<1.5에서는 secondary, 1.5부터는 explicit 사용
> pytorch url의 경우, cuda/cpu 중 필요한 것으로 변경
> cpu url: https://download.pytorch.org/whl/cpu
```
poetry source add -p explicit pytorch https://download.pytorch.org/whl/cu118
poetry add --source pytorch torch torchvision torchaudio
```