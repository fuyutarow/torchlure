# Torch Lure


<a href="https://www.youtube.com/watch?v=wCzCOYCfY9g" target="_blank">
  <img src="http://img.youtube.com/vi/wCzCOYCfY9g/maxresdefault.jpg" alt="Chandelure" style="width: 100%;">
</a>


# Depndencies

```
pip install git+https://github.com/Farama-Foundation/Minari.git@19565bd8cd33f2e4a3a9a8e4db372044b01ea8d3
```


```sh
pip install torchlure
```

# Usage
```py
import torchlure as lure

# Optimizers
lure.SophiaG(lr=1e-3, weight_decay=0.2)

# Functions
lure.tanh_exp(x)
lure.TanhExp()

lure.quantile_loss(y_pred, y_target, quantile=0.5)
lure.QuantileLoss(quantile=0.5)

lure.RMSNrom(dim=256, eps=1e-6)

# Noise Scheduler
lure.LinearNoiseScheduler(beta=1e-4, beta_end=0.02, num_timesteps=1000)
lure.CosineNoiseScheduler(max_beta=0.999, s=0.008, num_timesteps=1000):
```

### Dataset

```py
from torchlure.datasets import OfflineRLDataset, D4RLDataset

dataset = D4RLDataset(
    dataset_id="hopper-exppert-2405.1",
    dataset_name="d4rl_hopper-expert-v2",
    env_id="Hopper-v4",
)

dataset = D4RLDataset(
    dataset_id="d4rl_halfcheetah-expert-2405",
    dataset_name="d4rl_halfcheetah-expert-v2",
    env_id= "HalfCheetah-v4",
)

ataset = D4RLDataset(
    dataset_id="d4rl_walker2d-expert-2405",
    dataset_name="d4rl_walker2d-expert-v2",
    env_id= "Walker2d-v4",
)
```