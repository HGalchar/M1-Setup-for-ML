
# Plant Disease detection ML project and Mac M1 setup from scracth.



## Running steps:

To run tests, run the following command.

First we need to check one folder ~/opt/ or /opt with cmd+space and type "/opt", 
if you want proper installation then remove that folder and then follow below steps.

step-1: 
M1 chip status checking with GPU and CPU, Install Home Brew for Mac os.
open terminal and Type in terminal 

```bash 
"/bin/bash -c $(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"  
```

step-2: Now we will install Miniforge3: 

```bash
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate
``` 

step-3: Restart terminal.

step-3: let's create directory to add our packages for tensorflow env

```bash
mkdir tensorflow_demo
cd tensorflow_demo
```

step-4: Make and activate Conda environment:
```bash
conda create --prefix ./env python=3.8
conda activate ./env
```

step-5: Now Install TensorFlow dependencies from Apple Conda channel.
```bash
conda install -c apple tensorflow-deps
```

step-6: Install base TensorFlow (Apple's fork of TensorFlow is called tensorflow-macos).
```bash
python -m pip install tensorflow-macos
```
step-7: Install Apple's tensorflow-metal to use Apple Metal (Apple's GPU framework) for M1, M1 Pro, M1 Max GPU acceleration.

```bash
python -m pip install tensorflow-metal
```




