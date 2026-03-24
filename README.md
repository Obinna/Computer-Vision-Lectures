# Computer-Vision-Lectures

> 📚 Setup guide for the Computer Vision Lectures environment using PyTorch (CPU mode).

---

## 🚀 Quick Setup Guide

### Step 1: Install Miniconda
Miniconda is lightweight and recommended.

1. Go to the official Miniconda download page:  
   👉 https://docs.conda.io/en/latest/miniconda.html

2. Download the latest **Miniconda3** installer for your OS:
   - **Windows**: `Miniconda3 Windows 64-bit .exe`
   - **macOS**: `Miniconda3 macOS 64-bit .pkg` (or shell script)
   - **Linux**: `Miniconda3 Linux 64-bit .sh`

3. Run the installer:
   - **Windows**: Double-click the `.exe` and follow the wizard (accept defaults).
   - **macOS**: Double-click the `.pkg` and follow the wizard.
   - **Linux**: Open a terminal and run:
     ```bash
     bash Miniconda3-latest-Linux-x86_64.sh
     ```
     Follow prompts (type `yes` when asked).

4. **Restart your terminal** / Anaconda Prompt so the `conda` command becomes available.

5. **Verify installation**:
   ```bash
   conda --version


### Step 2 Create the Conda Environment

# Create environment
 ```bash
conda create -n pytorch-cv python=3.12 -y
 ```

# Activate the environment
 ```bash
conda activate pytorch-cv
 ```

You will now see (pytorch-cv) at the beginning of your prompt – this means you're inside the environment.


### Step 3: Install Required Libraries

# Install scientific Python packages
conda install -c conda-forge jupyterlab matplotlib scikit-learn numpy pandas pillow tqdm ipykernel -y

# Install PyTorch (CPU version - recommended for class)
pip install torch torchvision torchaudio



### Step 4: Verify the Installation


# Check Python and core packages
python -c "import sys; print('Python version:', sys.version)"

# Check PyTorch
python -c "
import torch
import torchvision
print('PyTorch version:', torch.__version__)
print('Torchvision version:', torchvision.__version__)
print('CUDA available:', torch.cuda.is_available())
"


### Step 5: Launch JupyterLab

jupyter lab

