# Getting Started with Brain Imaging Tools via the Neurodesktop Container
This file shows how to use neuroimaging tools thanks to a [neurodesk container](https://www.neurodesk.org/), but more specifically FreeSurfer package. How to install this data analysis environment is beautifully explained in great detail in their [documentation](https://www.neurodesk.org/docs/). 

An interesting [test server]( https://play.neurodesk.org/v2/gh/neurodesk/jupyter-neurodesktop-image/main?urlpath=neurodesktop) was used to test out how the container works. It contains multiple tools such as ANTs, fsleyes and FreeSurfer. This server looks as shown below:

<div>
<p style="text-align:center;"><img src="https://github.com/Andjelaaaa/dimitrijevic_project/tree/main/BrainHackCloud_steps/NeuroDesk.png?raw=1"  width="1000"  ></p>
</div>  

After opening the test server, in order to use FreeSurfer a license needs to be obtained. A detailed explanation on how to do it can be found [here](https://www.neurodesk.org/docs/faq/#freeview-720-crashes-when-i-open-files). Other more specific details on adding the license are explained in [issue 56](https://github.com/brainhackorg/brainhack_cloud/issues/56) and [issue 59](https://github.com/brainhackorg/brainhack_cloud/issues/59) on GitHub. 

Hence, activating FreeSurfer version 7.2.0 can be done with this command:
```console
    ml freesurfer/7.2.0  
```
Now, all the usual FreeSurfer commands are accessible and can be directly written in the command line. Also, data can even be downloaded from the internet in this test server tool!