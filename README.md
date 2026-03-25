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
 ```bash
conda install -c conda-forge jupyterlab matplotlib scikit-learn numpy pandas pillow tqdm ipykernel -y
 ```

# Install PyTorch (CPU version - recommended for class)
 ```bash
pip install torch torchvision torchaudio
 ```



### Step 4: Verify the Installation


# Check Python and core packages
 ```bash
python -c "import sys; print('Python version:', sys.version)"
 ```

# Check PyTorch
 ```bash
python -c "
import torch
import torchvision
print('PyTorch version:', torch.__version__)
print('Torchvision version:', torchvision.__version__)
print('CUDA available:', torch.cuda.is_available())
"
```


### Step 5: Launch JupyterLab
 ```bash
jupyter lab
```


### Step 6 You can instal Visual Studio Code if you prefer it. 


---

## Windows

### Step 1: Download VS Code
1. Go to the official Visual Studio Code website:  
   [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Click the **Download** button (it automatically detects Windows).

### Step 2: Install
1. Open the downloaded file `VSCodeUserSetup-x64-*.exe`.
2. **Important**: Check the following options during installation:
   - [x] **Add "Open with Code" action to Windows Explorer file context menu**
   - [x] **Add "Open with Code" action to Windows Explorer directory context menu**
   - [x] **Register Code as an editor for supported file types**
   - [x] **Add to PATH** (this option is checked by default)
3. Click **Next** → **Install**.
4. Click **Finish** when installation completes.

### Step 3: Verify
- Press `Win + S`, type `Visual Studio Code`, and launch it.
- Or press `Win + R`, type `code`, and press Enter.

---

## macOS

### Step 1: Download VS Code
1. Go to: [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Click the **Download** button (it will download the macOS version).

### Step 2: Install
1. Open the downloaded file `Visual Studio Code.zip`.
2. Drag the **Visual Studio Code.app** to your **Applications** folder.
3. (Optional but recommended) Add VS Code to Dock:
   - Right-click the app → **Options** → **Keep in Dock**.

### Step 3: Open VS Code for the first time
1. Launch **Visual Studio Code** from Applications or Spotlight (`Cmd + Space`).
2. macOS may show a security warning the first time.  
   → Click **Open** to allow it.

### Step 4: Add `code` command to PATH (Recommended)
1. Open VS Code.
2. Press `Cmd + Shift + P` to open Command Palette.
3. Type and select: **Shell Command: Install 'code' command in PATH**
4. Enter your administrator password if prompted.

Now you can open folders or files from terminal with:
```bash
code .
 ```

