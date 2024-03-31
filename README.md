# Python VBO
By using this VBO we can run python code directly in blueprism.

# Instructions
1. Place the Python.Runtime.dll to Blueprism installed folder.
2. Import the .bprelese file.
3. In process provided example usage of each action of Python VBO.

# Features:
1. Run python script or .py files.<br>
2. Install or Uninstall modules from https://pypi.org/ in VBO only.<br>
3. Get installed modules List.<br>
4. Use mixer of python and .Net modules/libraries in python code.<br>
5. Ready to use Python VBO(almost main actions are available). <br>
6. Included example usage actions in process.

# How to pass parameters from BP to python script.
 By using collection we can pass parameters to python script.
 Example python script:
 ```python
 def exampleFunction(paramOne, paramTwo, paramThree):
    return paramOne +" * "+ paramTwo +" * "+ paramThree   #assume paramOne,paramTwo,paramThree are text.
 ```
In Blueprism collection:

 ![picture alt](https://raw.githubusercontent.com/BlueprismWorld/Run-python-in-Blueprism/main/params.JPG "Title is optional")
 
Above collection we can pass params to python function, param name do not have to be same but order is manadtory, given order params will passed to python function.<br>
After excetion of python script code output will be:
 ```python
 This param one * Param names do not have to be same order is mandatory * This is param three.
 ``` 
# How to install/uninstall modules:
By using Install Pip Module/Uninstall Pip Module actions can install/uninstall modules.

# How to set modules path:
 Lets say for example you have bunch of modules in a folder and runtime you want use those modules in your python script in that case by using Set Module Path action we can set the path. Make sure first set module path before using.
 
# Note:
   First call IntialisePython action before using other actions from the Python VBO.
   
# How it works.
In Python_Interop.dll file embeded python standared library and python core files, when ever run IntialisePython action embeded core files will be extracted to AppData/Local folder or given path. Once extracted core files set the path where core files are extracted. and load the core files into memory.

