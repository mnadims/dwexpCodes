README: Setting Up a Quantum Computing Environment with D-Wave Integration
--------
This guide provides step-by-step instructions to set up a Python environment for quantum computing using D-Wave's quantum computing platform. The environment includes essential libraries for quantum computing, data manipulation, and machine learning. The setup also allows you to use Jupyter notebooks for an interactive coding experience.

Prerequisites
-------------
- Anaconda/Miniconda installed on your system.
- A D-Wave account and API token (required for accessing D-Wave's quantum computing services).

Steps to Set Up the Environment
-------------------------------

1. **Create a Conda Virtual Environment**

   First, create a new Conda environment named `venv_dw` with Python installed:

   ```bash
   conda create -n venv_dw python
   ```

2. **Activate the Environment**

   Activate the newly created environment:

   ```bash
   conda activate venv_dw
   ```

3. **Install Necessary Python Packages**

   Install the required Python packages using `pip`:

   ```bash
   pip install numpy==1.26.4
   pip install openml==0.14.2 dimod==0.12.16 dwave-system==1.25.0 dwave-ocean-sdk==7.1.0 imbalanced-learn==0.12.3 openpyxl==3.1.5 xlsxwriter==3.2.0
   ```

   - `numpy`: Fundamental package for numerical computing.
   - `openml`: Interface for accessing datasets and machine learning experiments.
   - `dimod`: Library for creating and manipulating binary quadratic models, used in quantum computing.
   - `dwave-system`: Interface to D-Wave's quantum computers.
   - `dwave-ocean-sdk`: SDK for developing quantum computing applications with D-Wave.
   - `imbalanced-learn`: Toolkit for handling imbalanced datasets.
   - `openpyxl`: Library for reading and writing Excel files.
   - `xlsxwriter`: Tool for writing Excel files.

4. **Set Up Jupyter Notebook**

   Install Jupyter and configure the environment for use in Jupyter notebooks:

   ```bash
   conda install jupyter
   pip install ipykernel
   python -m ipykernel install --user --name=venv_dw --display-name "VirDwave"
   ```

   - `jupyter`: Interactive notebook environment.
   - `ipykernel`: Kernel to use the Conda environment in Jupyter notebooks.
   - `python -m ipykernel install --user --name=venv_dw --display-name "VirDwave"`: Adds the `venv_dw` environment as a Jupyter kernel named "VirDwave".

5. **Set Up D-Wave API Token**

   Set your D-Wave API token to access their quantum computing services:

   ```bash
   set DWAVE_API_TOKEN=YOUR-ACTUAL-API-TOKEN-HERE
   ```

   Replace `YOUR-ACTUAL-API-TOKEN-HERE` with your actual D-Wave API token. This token is required to authenticate your access to D-Wave's quantum computers.

Usage
-----
- **Starting Jupyter Notebook:** 
  Run `jupyter notebook` in your terminal, and select the "VirDwave" kernel to start working with your quantum computing environment.
  
- **Accessing D-Wave's Quantum Computer:** 
  Make sure your API token is correctly set before running quantum computing scripts.

Notes
-----
- The environment is set up to work with specific versions of the packages for compatibility reasons. Adjustments might be needed if you plan to use different versions or additional packages.
- Keep your D-Wave API token secure and do not share it publicly.

Troubleshooting
---------------
- If you encounter issues with package installations, ensure that your Conda environment is active (`conda activate venv_dw`).
- For any problems with Jupyter kernel not appearing, run the kernel installation command again or restart your Jupyter notebook server. 

This setup is now ready for exploring quantum computing tasks with D-Wave and leveraging additional tools for data manipulation and machine learning. Enjoy your quantum journey!
