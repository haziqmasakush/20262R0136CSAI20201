# Assignment 4 execution record

Student ID: 2024320329  
Name: 무함마드 아미르 하지크 빈 마사쿠시

The submission notebook is `2024320329_무함마드 아미르 하지크 빈 마사쿠시_assignment4_Code.ipynb`.

The notebook was executed in a fresh local Jupyter kernel, from top to bottom, on an NVIDIA GeForce RTX 3050 Laptop GPU. All 35 code cells completed and every provided assertion passed. All 10 plots and other cell outputs are embedded in the notebook. All 20 original `END OF YOUR CODE` boundaries, their surrounding hashtag comments, and the provided check cells were retained. The written answers describe the measured results.

The `logs/` folder contains the 50 CSV files for the 25 training runs. Each run has per-step and per-epoch logs. The final notebook table reloads these files from disk. Early stopping is retrospective checkpoint selection from the logs, as specified by the assignment; the notebook does not save trained model checkpoints.

## Environment

- Python 3.12
- PyTorch 2.11.0+cu128
- torchvision 0.26.0+cu128
- NumPy 2.5.4
- Matplotlib 3.11.2
- Seed: 231 (as provided)

Open the notebook in Jupyter or Colab, select a GPU runtime if available, and run all cells in order. Required imports are PyTorch, torchvision, NumPy, and Matplotlib. The original CIFAR-10 setup cells are unchanged and download the dataset if needed. For this execution, the original server stalled, so the identical archive was downloaded from the [MIT Open Learning mirror](https://huggingface.co/datasets/MIT-OL-AI-D/cifar-10-python) and verified against torchvision's archive MD5, `c58f30108f718f92721af3b95e74349a`, before extraction. Dataset files and the local Python environment are excluded from the repository.

## Selected results

- Tiny-set sanity check: 100% training accuracy.
- Optimizer reference errors: SGD+Momentum 0; RMSProp 0; Adam approximately 7.2e-17.
- Constant versus step-decay final training losses: 2.158 versus 0.455.
- Baseline minimum-validation-loss epoch: 3; validation accuracy 40.7%.
- Combined regularization minimum-validation-loss epoch: 26; validation accuracy 43.6%.
- Baseline versus combined regularization final accuracy gap: 56.0 versus 5.32 percentage points.
- Augmentation alone has higher selected validation accuracy (45.5%) than the combined configuration, while the combined configuration has the smaller final gap. The written answer discusses this tradeoff.

KULMS submission remains a separate upload of the notebook.
