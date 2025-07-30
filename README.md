# To install Conda (specifically the Anaconda distribution) on Ubuntu Linux, follow these key steps:

1. **Download the latest Anaconda installer** for Linux from the official Anaconda repository. For example, you can download the installer with wget in your terminal:

   ```bash
   wget https://repo.anaconda.com/archive/Anaconda3-2024.06-1-Linux-x86_64.sh
   ```

2. **Verify the installer checksum** (optional but recommended) to ensure the file integrity:

   ```bash
   sha256sum Anaconda3-2024.06-1-Linux-x86_64.sh
   ```

   Compare the output with the official checksum provided on the Anaconda site.

3. **Run the Anaconda installer script**:

   ```bash
   bash Anaconda3-2024.06-1-Linux-x86_64.sh
   ```

   - Review and accept the license terms by typing `yes`.
   - Choose the installation location or accept the default (~your_home/anaconda3).
   - Opt to initialize Anaconda by default when prompted (recommended).

4. **Activate the installation** by sourcing the `.bashrc` file so changes take effect:

   ```bash
   source ~/.bashrc
   ```

   After this, you should see `(base)` in your terminal prompt indicating Conda base environment is active.

5. **Verify the installation** by running:

   ```bash
   conda info
   ```

   This will display information about your Conda installation if successful.

### Additional Notes:
- Anaconda installs a large collection of packages. If you prefer a minimal installation, you can install Miniconda instead.
- Conda can also be initialized for other shells like fish using `conda init fish`.
- To uninstall, simply remove the Anaconda installation directory and optionally cleanup Conda-related config files.

This approach works reliably on Ubuntu 22.04 and 24.04 LTS versions and newer Linux releases.

___

## To create and manage Conda environments with and without specifying a Python version, use these commands:

## 1. Create an Environment with a Specific Python Version

Replace `myenv` with your desired environment name and `3.10` with the Python version you want:
```bash
conda create --name myenv python=3.10
```
This creates a new environment named `myenv` with Python3.10 installed.

## 2. Create an Environment Without Specifying a Python Version

Just provide the environment name:
```bash
conda create --name myenv
```
This sets up an environment without any default Python installed. You can add Python or any package later.

## 3. Activate the Environment

To activate your environment:
```bash
conda activate myenv
```
After this, your terminal prompt will usually show the environment name (e.g., `(myenv)`), indicating it’s active.

## 4. Deactivate the Environment

To leave (deactivate) the current environment:
```bash
conda deactivate
```
This returns you to the base Conda environment or your system’s shell.

### Summary Table

| Command                                      | Purpose                                   |
|-----------------------------------------------|-------------------------------------------|
| `conda create --name myenv python=3.10`       | New env with Python3.10                   |
| `conda create --name myenv`                   | New env without default Python            |
| `conda activate myenv`                        | Activate the environment                  |
| `conda deactivate`                            | Deactivate (exit) the environment         |
