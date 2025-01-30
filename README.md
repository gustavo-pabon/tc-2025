# Steps to configure the environment using macos

## Prerrequisites

* Install docker desktop: https://www.docker.com/products/docker-desktop/
* Install VSCode: https://code.visualstudio.com/
* Install the following extensions in VSCode:
    * Docker
    * Python
    * Jupyter

## Configuration steps

1. Clone this repo locally:

    > `git clone https://github.com/gustavo-pabon/tc-2025.git`

2. Create the `.env` file:

    > `cd tc-2025`
    >
    > `cp .env.template .env`
    >
    > Edit .env and update the environment variables.

3. Build the `tc2025` image:

    > `make build-image`

4. Run a `tc2025` container:

    > `make run-container`

5. Copy the kernel url including the token string:
    > Copy the line in the log that looks like:
    > `http://127.0.0.1:8888/lab?token=8a3eb1ebf39038598e0b6ce7cc400bf841b2b3891998ceb4`

6. Open VSCode and from **File** menu, select **Open Folder...** and open the `tc-2025` folder.

7. Open the `01-create your copilot.ipynb` notebook.

8. In the top-left part of the notebook click on **Select Kernel**.

9. Click on **Select Another Kernel ...**

10. Select **Existing Jupyter Server...**

11. In **Enter remote url, or select jupter server...**, paste the url copied in step 5.

12. Select **Connect to the jupter server http://127.0.0.1:8888...** 

13. Leave all the default names 

14. Start executing the notebook