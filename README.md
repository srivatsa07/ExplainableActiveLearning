# ExplainableActiveLearning
- Bash setup.sh

```bash
#!/bin/bash
conda create -y -n thesis python=3.10
source activate thesis
pip install torch torchvision matplotlib 
python -m ipykernel install --user --name=thesis --display-name "Python (thesis)"