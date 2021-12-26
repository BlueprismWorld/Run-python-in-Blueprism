# Python VBO
By using this VBO we can run python code directly in blueprism without installing python in the user machine.
This VBO used python 3.9 version.

# Instructions
1. Place the Python_Interop.dll, Microsoft.CSharp.dll to Blueprism installed folder.
2. Import the .bprelese file.
3. In process provided example usage of each action of Python VBO.

# How to pass parameters from BP to python script.
 By using collection we can pass parameters to python script.
 Example python script:
 ```pythpn
 def exampleFunction(paramOne, paramTwo, paramThree):
    return paramOne +" * "+ paramTwo +" * "+ paramThree   #assume paramOne,paramTwo,paramThree are text.
 ```
In Blueprism collection:

 ![picture alt](https://raw.githubusercontent.com/BlueprismWorld/Run-python-in-Blueprism/main/params.JPG "Title is optional")
 
Above collection we can pass params to python function, param name do not have to be same but order is manadtory, given order params will passed to python function.<br>
After excetion of python script code output will be:
 ```pythpn
 This param one * Param names do not have to be same order is mandatory * This is param three.
 ```
# How to set modules path:
 Lets say for example you have bunch of modules in a folder and runtime you want use those modules in your python script in that case by using Set Module Path action we can set the path. Make sure first set module path before using.
 
# Note:
   First call IntialisePython action before using other actions from the Python VBO.
   
# How it works.
In Python_Interop.dll file embeded python standared library and python core files, when ever run IntialisePython action embeded core files will be extracted to AppData/Local folder or given path. Once extracted core files set the path where core files are extracted. and load the core files into memory.

