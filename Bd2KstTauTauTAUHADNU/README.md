# Examples
Log in to lxplus and move to a directory with enough disk space

```
git clone git@github.com:HEP-FCC/FCCAnalyses.git
cd FCCAnalyses
source ./setup.sh
```

Need to locally install zfit. First specify the location where you want those to be instal by setting this enviroment variable (please adapt MYPATH to where you want the packages to be installed):
```
export PYTHONUSERBASE=/MYPATH/.local
```

for example
```
mkdir localPythonTools
export PYTHONUSERBASE=localPythonTools/.local
```

First we need to upgrade pip:
```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
```

and add it to the path so that we run the new installed version
```
export PATH=/MYPATH/.local/bin:$PATH
```

or following the example

```
export PATH=localPythonTools/.local/bin:$PATH
```

Then install zfit in the local python dir:

```
python -m pip install --user zfit
```
and add it to the pythonpath

```
export PYTHONPATH=/MYPATH/.local/lib/python3.7/site-packages:$PYTHONPATH
```

or following the example

```
export PYTHONPATH=localPythonTools/.local/lib/python3.7/site-packages:$PYTHONPATH
```

For using it later on after the installation is done, simply run:

```
export PATH=localPythonTools/.local/bin:$PATH
export PYTHONPATH=/MYPATH/.local/lib/python3.7/site-packages:$PYTHONPATH
```

or following the example

```
export PATH=localPythonTools/.local/bin:$PATH
export PYTHONPATH=localPythonTools/.local/lib/python3.7/site-packages:$PYTHONPATH
```

Then you can run the example. First clone the repository:
```
git clone git@github.com:clementhelsens/Examples.git
cd Examples
````
then run
```
cd Bd2KstTauTauTAUHADNU
python run.py
```
