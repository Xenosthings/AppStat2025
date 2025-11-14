[Back to main page](../README.md)

### Minimal installation: VS code and Miniconda

- 1: Install Miniconda following [these steps](https://www.anaconda.com/docs/getting-started/miniconda/install). The _anaconda.com/download_ website will ask you to create an account if you want to download the graphical installer. You can bypass this step by directly downloading the latest version for your system [here](https://repo.anaconda.com/miniconda/).


    **Extra step (Mac/Linux)**: the recommended initialization option makes Miniconda start automatically every time you open a new terminal. This is good as the conda environment will be recognised  by VS code, but you will now enter a conda environment every time you open a terminal. To stop this, run in a terminal:
    ```bash
    conda config --set auto_activate_base false
    ```


- 2: [Install Git](https://git-scm.com/install/) to easily download the latest exercises from the AppStat GitHub. The default installation options are good for us.

- 3: Download the GitHub repository: On the GitHub page, click on the green `<>code` button, select `HTTPS` and copy the https link.
In your machine terminal, go to the directory where you want to save the exercises and download the GitHub content:
    ```bash
    git clone <PASTE HTTPS LINK HERE>
    ```

    Later, when new exercises appear, you can automatically update your local copy by going in your AppStat directory and run:
    ```bash
    git pull
    ```
    **Important:** Always make a copy of the notebook with a different name (e.g. *filename_yourname.ipynb*) before working on it, so your changes don't get overwritten when you pull the new exercises.
 
- 4: Create a new conda environment: Download the .yaml file with the packages list from the [course website](https://www.nbi.dk/~petersen/Teaching/Stat2025/pythonpackages.html). Then from the Anaconda Prompt app (Windows) or your terminal (Mac/Linux), setup your conda environment with:
    ```bash
    conda env create -f /path/to/file/AppStat25_environment.yaml
    ```

- 5: [Install VS code](https://code.visualstudio.com/download)

- 6: Start VS code<span style="color:blue;">\*</span> and click on the "Extensions" icon on the left and search for "Jupyter" in the search bar. Select and install the Jupyter extension by Microsoft. Install the "Python" extension as well to get access to all the smart features (auto-completion, debugger, etc.).

    <span style="color:blue;">\*</span>On Windows, start VS code by typing the `code` command in the Anaconda Prompt app, this makes sure VS code will detect the conda environment.


- 7: Open a Jupyter notebook. In the top right corner of a notebook, click on `Select kernel -> Python environment`. Your `appstat` conda environment should appear, select it. You can now run the Jupyter notebooks inside of VS code with your conda environment!

- (Optional): At some point, you may want to install new packages in the conda environment. From the Anaconda Prompt app (Windows) or your terminal (Mac/Linux), enter the conda environment and run the standard pip install command for the package you want to install:
    ```bash
    conda activate appstat25
    pip install <PACKAGE NAME>
    ```
