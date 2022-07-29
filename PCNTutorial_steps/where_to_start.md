# Where to Start with the PCN-toolkit Tutorials?

This is a guide to starting out using the [PCN-toolkit](https://github.com/amarquand/PCNtoolkit). It has a beautifully made documentation, but sometimes it is easy to get lost in all the available tutorials. Hence, this is a guide which suggests with which one of them to start and where to run them for a smoother introduction to their tool!

## Steps to follow through while starting off their tutorials
1. Start off by knowing first hand what you wish to use the tool for so that you can be attentive to the most important parts for you while going through these next tutorials!
2. Get familiar with how their [PCNtoolkit-demo repository](https://github.com/predictive-clinical-neuroscience/PCNtoolkit-demo) is organized and fork it to your own repository. On my end (this is not a required substep), I applied this command in my local project repository so that their demo repository becomes a subtree:
    ```console
    user@LAPTOP-abcdefgh:~$ git subtree add --prefix PCNToolkitDemo {URL of original GitHub} main --squash                   
    ```

3. First, read this [README file](https://github.com/saigerutherford/CPC_ML_tutorial/blob/master/README.md) which contains very useful Google Colab info as well as 4 tasks that can be achieved directly on Google Colab
4. Link your Google Colab to GitHub so that you can commit changes directly from the Google Colab platform! See image below on where to find this feature:
    <div>
    <p style="text-align:center;"><img src="https://github.com/Andjelaaaa/dimitrijevic_project/blob/main/PCNTutorial_steps/GoogleColabGit.png?raw=1"  width="1000"  ></p>
    </div>  
5. To modify some newly added changes go to File --> save a copy in GitHub and write your commit message. It is normal that it will take some time to load the repository and then the changes via the Google Colab platform
6. Don't forget to add a link to the Google Colab by writing these lines in the first cell of your jupyter notebook:
    ```markdown
    [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb)               
    ```
    OR simply by clicking on *Include a link to Colaboratory* when copying to GitHub with a commit message via Google Colab. Some further explanations are available in [this Google Colab](https://colab.research.google.com/github/googlecolab/colabtools/blob/master/notebooks/colab-github-demo.ipynb)
7. Now go through the CPC_2020 tutorial then the HBR_FCON while saving your changes when working on the jupyter notebooks on Colab
8. Finish off with the BLR_protocol which does not install correctly the requirements.txt file because of the embedded Google Colab python version (3.7.13) while it should be 3.9.1. See the [related GitHub issue here](https://github.com/predictive-clinical-neuroscience/PCNtoolkit-demo/issues/6) that was created. 
9. Run this tutorial locally by first creating a conda environment like so:
    ```console
    user@LAPTOP-abcdefgh:~$ conda create --name new_environment_name python=3.9.1               
    ```
10. To finish, follow through the modified tutorial which can be found under PCNToolkitDemo in the [BrainHack school project repo](https://github.com/brainhack-school2022/dimitrijevic_project) which successfully runs all the cells and imports the right packages necessary for the PCNToolKit functions to work.

Congrats! :tada: You are now set to try to use it on your own data!
