# Computer-Vision-Lectures
Step 1: Install Miniconda (if you don’t already have Conda/Anaconda)
Miniconda is lightweight and recommended.

Go to the official Miniconda download page: https://docs.conda.io/en/latest/miniconda.html
Download the latest Miniconda3 installer for your operating system:
Windows: Miniconda3 Windows 64-bit .exe
macOS: Miniconda3 macOS 64-bit .pkg (or the shell script if you prefer)
Linux: Miniconda3 Linux 64-bit .sh

Run the installer:
Windows: Double-click the .exe and follow the wizard (accept defaults).
macOS: Double-click the .pkg and follow the wizard.
Linux: Open a terminal, run bash Miniconda3-latest-Linux-x86_64.sh, follow prompts (type yes when asked).

Close and reopen your terminal / Anaconda Prompt so the conda command becomes available.

Verification: Open a new terminal / Anaconda Prompt and type:
Bashconda --version
You should see a version number.
Step 2: Create the special Conda environment
In your terminal / Anaconda Prompt, run these commands one by one:
Bash# Create the environment with Python 3.12
conda create -n pytorch-cv python=3.12 -y

# Activate the environment
conda activate pytorch-cv
You will now see (pytorch-cv) at the beginning of your prompt – this means you’re inside the environment.
Step 3: Install all required libraries
Still inside the activated environment, run:
Bash# Install core scientific libraries via conda (fast and stable)
conda install -c conda-forge jupyterlab matplotlib scikit-learn numpy pandas pillow tqdm ipykernel -y

# Install PyTorch + torchvision (CPU version – official recommended way)
pip install torch torchvision torchaudio
This may take a few minutes – be patient.
Step 4: Verify the installation
Run these commands inside the environment:
Bash# Check Python version and key packages
python -c "import sys; print('Python:', sys.version)"

# Check PyTorch
python -c "import torch; import torchvision; print('PyTorch version:', torch.__version__); print('Torchvision version:', torchvision.__version__); print('CUDA available:', torch.cuda.is_available())"

# Expected output: CUDA available should be False (CPU mode)
If you see no errors and versions are printed, everything is working!
Step 5: Launch JupyterLab and test
Still inside the environment, run:
Bashjupyter lab

A browser window should open automatically.
