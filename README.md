# ExplainableActiveLearning
## Installation 
- Bash setup.sh

```bash
# setup_env.sh
#!/bin/bash
conda create -y -n thesis python=3.10
source "$(conda info --base)/etc/profile.d/conda.sh"
conda activate thesis
pip install torch torchvision matplotlib scipy scikit-learn pandas tqdm seaborn
pip install grad-cam captum wandb h5py gdown ipykernel ipywidgets
pip install -U scikit-activeml
python -m ipykernel install --user --name=thesis --display-name "thesis"
conda deactivate
```
- ```top``` command used to monitor cpu usage in server.

## Pre-Processing
- As the datasets resolutions are different. CIFAR - 10 is resized to 96x96 to match with PCAM to train on the same model.
