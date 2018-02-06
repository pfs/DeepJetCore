

DeepJetCore: Package for training and evaluation of deep neural networks for HEP
===============================================================================

"description here"

This package just provides the basic functions. The actual training data structures
and DNN models have to be defined in a user package. A script to set it up will be provided.


Setup (CERN)
==========
It is essential to perform all these steps on lxplus7. Simple ssh to 'lxplus7' instead of 'lxplus'

Pre-Installtion: Anaconda setup (only once)
Download miniconda3
```
cd <afs work directory: you need some disk space for this!>
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```
Please follow the installation process. If you don't know what an option does, please answer 'yes'.
After installation, you have to log out and log in again for changes to take effect.
If you don't use bash, you might have to add the conda path to your .rc file
```
export PATH="<your miniconda directory>/miniconda3/bin:$PATH"
```
This has to be only done once.


Installation:

```
mkdir <your working dir>
cd <your working dir>
git clone https://github.com/DL4Jets/DeepJetCore
cd DeepJetCore/environment
./setupEnv.sh deepjetLinux3.conda
```
For enabling gpu support add 'gpu' as an additional option to the last command.
This will take a while. Please log out and in again once the installation is finised.

When the installation was successful, the DeepJet tools need to be compiled.
```
cd <your working dir>
cd DeepJetCore
source lxplus_env.sh / gpu_env.sh
cd compiled
make -j4
```

After successfully compiling the tools, log out and in again.
The environment is set up.


Usage
==========

(to be updated)
