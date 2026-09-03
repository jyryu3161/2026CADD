## 📌 Overview and Installation Guide for Anaconda

### 1. What is Anaconda?

Anaconda is an open-source package management and distribution platform designed to easily set up environments for data science, machine learning, and artificial intelligence, using Python and R programming languages. It simplifies installing and managing numerous libraries widely used in Python, such as NumPy, Pandas, and Matplotlib.

- **Purpose**: Easy management and reproducible setup of data science and machine learning environments.
- **Developer**: Anaconda, Inc. (Texas, USA)

---

### 2. Why Install Anaconda?

Benefits of installing Anaconda include:

- **Simplified Environment Setup**: Automatically resolves dependencies between packages.
- **Easy Management of Virtual Environments**: Independent environments for different projects.
- **Comprehensive Package Provision**: Comes preloaded with essential data science and machine learning packages.
- **Cross-platform Compatibility**: Available on Windows, macOS, Linux, and other operating systems.

---

### 3. How to Install Anaconda (Manual Installation Guide, Ubuntu example)

Execute the following commands **one by one** in your terminal to install Anaconda.

#### Step 1. Download Anaconda Installation Script

```bash
wget https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh -O anaconda.sh
```

#### Step 2. Run Installation Script

Start the Anaconda installation with the following command:

```bash
bash anaconda.sh
```

When prompted with license terms:

- **Press the ENTER** for license agreement.
- **Press the arrow-down (↓) key** to scroll down to the end of the license agreement.
- After reaching the end, you'll see the prompt:

```bash
Do you accept the license terms? [yes|no]
```

- Type `yes` and press Enter.

Next, you'll see the default installation path:

```bash
Anaconda3 will now be installed into this location:
/home/username/anaconda3

- Press ENTER to confirm the location
- Press CTRL-C to abort the installation
- Or specify a different location below
```

- Press Enter to use the default installation location, or type a different path if preferred.

Wait until the installation is complete.

#### Step 3. Initialize Environment Variables

After installation, execute the following commands to activate Anaconda immediately:

```bash
eval "$(~/anaconda3/bin/conda shell.bash hook)"
conda init
```

Running `conda init` automatically configures your shell to use conda commands on future terminal sessions.

#### Step 4. Delete Installation Script

After installation is completed, remove the downloaded installation script:

```bash
rm anaconda.sh
```

#### Step 5. Apply Settings and Finish Installation

To finalize installation, restart your terminal or run the following command to reload environment variables:

```bash
source ~/.bashrc
```

Verify successful installation by checking the Anaconda version:

```bash
conda --version
```

If the Anaconda version number is displayed, your installation was successful.

---

### 4. Essential Anaconda Commands

#### Environment Management Commands

```bash
# Create environment
conda create -n env_name python=3.11

# Activate environment
conda activate env_name

# Deactivate environment
conda deactivate

# Remove environment
conda remove -n env_name --all

# List all environments
conda env list

# Export environment to YAML file
conda activate env_name
conda env export > environment.yml

# Create new environment from exported YAML file
conda env create -f environment.yml

# (Optional) Create environment from YAML with a new name
conda env create -n new_env_name -f environment.yml
```

#### Package Installation and Management Commands

```bash
# Install packages
conda install numpy pandas matplotlib

# Install from specific channel
conda install -c conda-forge package_name

# List installed packages
conda list

# Update a package
conda update package_name

# Update all packages
conda update --all
```

#### Conda Practice: Creating and Managing Environments

1. Create a new conda environment named "my_env" with Python version 3.10.
2. Install biopython package using conda.
3. Export the created environment into a YAML file.

Note: A YAML file is a human-readable text format used for data serialization, commonly used for configuring software applications and environments. YAML files typically have the `.yml` or `.yaml` extension.
---

Utilize this guide to efficiently install and make the most of Anaconda.

