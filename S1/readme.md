Course GitHub. https://github.com/SkafteNicki/dtu_mlops

%%%%%%%%%%%
S1: SET UP
%%%%%%%%%%%


-----------------
M1.- The Terminal
-----------------

- Install Windows Subsystem Linux (WSL) https://learn.microsoft.com/en-us/windows/wsl/install
- Basic Commands: Navigating -> cd, overview of the files in folder -> ls, TAB COMPLETION.
- Additional Commands: which, echo, cat, wget, less and top. > operator.
- Nano editor familiarization.
- BASH. The editor programming language. Useful for sequential program execution. Example:

A bash script is written by saving a text file with .sh and the header of the file includes "#!/bin/bash"
after which simple command line commands can be writen.

#!/bin/bash
# A sample Bash script, by Ryan
echo Hello World!


-----------------
M2.- Conda & Venvs
-----------------

Conda is an environment manager that helps keep environments not-contaminated.
- Difference between conda and pip:
	PIP: Installs the new packages blindly with out checking compatibilities between packages versions. Prone to dependenci issues.
	CONDA: Conda checks for dependencies and therefore compatibility issues before proceeding with the sequential insatallation.

EX:
- Create an environment
- List the environments. [ conda env list ]
- List of packages installed in the environmet. [ codna list // conda list --explicit > "Name.txt" ]
- Creating an environment from an environment package list. [ conda env create --file "Name.txt" ]
- Export a list of the packages installed in the environment as "requirements.txt"
- [ pipreqs ] as a get around to create a package requirements file based on a script. pip install pipreqs


-----------------------
M3.- Editor [ VS Code ]
-----------------------
Parts of the editor.
- Action bar. Shows the extensions. 
- Side bar. Generally contains the file explorer.
- Editor. Where the code is shown.
- Terminal panel
- Status bar. Provides useful information based on the extensions.

** Jupyter Notebooks in production environments **
Good for development, for testing new ideas. Not useful for models deployment.

Solution: conda install nbconvert # or pip install nbconvert

jupyter nbconvert --to=script my_notebook.ipynb


---------------------------------------
M4.- Deep Learning Software [ PyTorch ]
---------------------------------------

Deep Learning has improved human life since its boom in 2012, but the TECHNICAL DEBT is an ML concept to refere to the 
costs of maintaining a DL production machine. Where ML models can be deployed in production with rather simple appraochs. 
Deep Learning comes with problems related to shear size of data and models.

DEEP LEARNING FRAMEWORKS

TensorFlow
Pytorch
JAX

The 2 former are the oldest, with bigger communities yet with older frameworks, improved by JAX, which is not mature enough.

Pytorch will be used as it is a bit simpler and it is eminently used in reaearchs & publications.

Pytorch uses Tensors in a similar way as Numpy uses Arrays. It makes it easy to use the GPU processing power, also gradients computation module and neural networks module.

NEURAL NETWORKS
Built with neurons,  which act as individual units, which has a number of inputs that are added together in order to get the unit output.
It looks like a vector product row*col.

TENSORS: They are multidimensional data container: vector (1D tensor), matrix (2D tensor), array with 3 indexes (3D Tensor).

unit_input = SUM(weights*features)+bias
unit_output = activation_fnc(unit_input)

Matrix multiplication can be done directly with torch.mm() or torch.matmul(). But it requires to the tensors to have the right shapes.

INPLACE OPERATIONS: Operations with TENSORS where the operation is followed by a underscore. "Operation_()"
* With Out making a copy *

















