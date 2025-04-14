# ExplainableActiveLearning
## Installation 
- Bash setup.sh

```bash
# setup_env.sh
#!/bin/bash
conda create -y -n thesis python=3.10
source "$(conda info --base)/etc/profile.d/conda.sh"
conda activate thesis
pip install torch torchvision matplotlib numpy scipy scikit-learn pandas tqdm seaborn
pip install shap grad-cam captum modAL wandb h5py gdown ipykernel ipywidgets
python -m ipykernel install --user --name=thesis --display-name "Python (thesis)"
```
- ```top``` command used to monitor cpu usage in server.

## Pre-Processing
- As the datasets resolutions are different. CIFAR - 10 is resized to 96x96 to match with PCAM to train on the same model.