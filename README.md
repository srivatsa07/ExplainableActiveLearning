# ExplainableActiveLearning
- Bash setup.sh

```bash
# setup_env.sh
#!/bin/bash
conda create -y -n thesis python=3.10
conda activate thesis
pip install torch torchvision matplotlib numpy scipy scikit-learn pandas tqdm seaborn
pip install shap grad-cam captum modAL wandb
python -m ipykernel install --user --name=thesis --display-name "Python (thesis)"
```
- ```top``` command used to monitor cpu usage in server.