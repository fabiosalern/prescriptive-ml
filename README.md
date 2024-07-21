# Integrating predictive and prescriptive modeling 

## Setting the package environment:

1. Initialize the conda environment:
    - `conda create --name gurobi-env python=3.9`

2. Activate the environment and setup the license:

    - **Activate the conda environment created:** `conda activate gurobi-env`

    - **Gurobi license:** 
        - Gurobi is installed using the pip or conda package distributors. These installations automatically include a size-limited license. This license also prints the message "Restricted license - for non-production use only" when running a Python program using Gurobi. Gurobi uses a restricted, size-limited license, and the model size exceeds these limits, i.e., 2000 variables, 2000 linear constraints, and 200 variables if quadratic terms are present. 
        - To unlock the ful usage of gurobi, you need to have a license. As a student you can ask for an academic license for free! Further details on the [Activate the Academic License section](#activate-the-academic-icense) below. 
        
        - If you don't need to unlock the full capabilties of gurobi solver move forward to the next bullet. If you have obtained the academic license, you will end up with with something like this: `grbgetkey 382398nsn-239320-dsds` this is the license token. 
    
    - Remember to be on your conda environment previously created and then activated. Run the following command: `conda install -c gurobi gurobi=11.0.1`

3. install the remaining dependencies: `pip install -r requirements.txt`

Now the environment is setted up and you are good to go!


## Obtain and Activate the Academic License

1. **Request the Academic license.**
    - Register as an "Academic user" on the [Gurobi website](https://www.gurobi.com/) and log into your account.

    - Connect your computer to the university network. You can connect your computer either directly or via a VPN that tunnels all traffic through the university network. Once the license file is set up, your computer does not need to be connected to the internet in order to use Gurobi. Visit the [License Request section of your User Portal](https://portal.gurobi.com/iam/licenses/request/), and select "GENERATE NOW" in the Named-User Academic block. 

    - You will obtain something like: `grbgetkey 382398nsn-239320-dsds`. Where `grbgetkey` is the command to run and `382398nsn-239320-dsds` is an example of license token.
    
    - Now in order to use the generated license, you need to: Install Gurobi on your local machine (next bullet). Install the Gurobi license (bullet 3).

2. **Install Gurobi on your local machine**. Depending on the type of operating system the procedure might change bit. Follow this guide: [LINK](https://support.gurobi.com/hc/en-us/articles/4534161999889-How-do-I-install-Gurobi-Optimizer) . 

3. **Install the Gurobi license**. 
    - Now that you have the license and installed gurobi, you can run the command: `grbgetkey 382398nsn-239320-dsds` on your terminal. This command will store locally the gurobi license. Please when you will be asked to specify the target folder for the license, setup the default location by pressing ENTER. 

    - You can check if the license is corrected loaded in your local machine, by running this command on the terminal: `gurobi_cl`. And if there are no errors, you are good to go!

4. **Useful references.**
    - [How do I resolve a "Model too large for size-limited Gurobi license" error?](https://support.gurobi.com/hc/en-us/articles/360051597492-How-do-I-resolve-a-Model-too-large-for-size-limited-Gurobi-license-error)

    - [Requesting an Academic Named-User license](https://support.gurobi.com/hc/en-us/articles/360040541251-How-do-I-obtain-a-free-academic-license)

    - [How do I install Gurobi Optimizer?](https://support.gurobi.com/hc/en-us/articles/4534161999889-How-do-I-install-Gurobi-Optimizer)

    - [How do I install Gurobi for Python?](https://support.gurobi.com/hc/en-us/articles/360044290292-How-do-I-install-Gurobi-for-Python)

    - Video - [How to Install Gurobi Python API with an Academic License](https://www.youtube.com/watch?v=k-iv5-c-U3E)
