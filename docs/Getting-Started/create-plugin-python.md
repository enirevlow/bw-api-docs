---
id: Create-plugin-python
title: Creating Python plugin
---

## Prerequisites
Install Python 3.7.8 if you do not already have it installed. </br>

## Basic plugin
Browzwear supports writing a plugin in Python 3.7.8. Follow these steps to create a basic plugin:

1. Install VStitcher.
2. Go to VStitcher's plugins folder: <br/>
```cpp
Windows:  %localappdata%\Browzwear\VStitcher\plugins
Mac:  ~/Library/Application Support/Browzwear/VStitcher/Plugins
``` 
   Note: If the Plugins folder doesn't exist, create it.
3. Create a new folder for your plugin.
4. Create another folder to contain the python plugin files - this will be the plugin package.
5. Create two new files within the plugin package folder: <br/>
```cpp
__init__.py
sample.py

```
5. Using your favorite Python editor, edit the files as follows: <br/>
```python
# __init__.py file

from sample import *
```

```python
# sample.py file

# import Browzwear API library
import BwApi

# implement initialization function
def BwApiPluginInit():
  # return 1 for successful initialization
  return 1
```
6. Create a file named plugin.json in the plugin folder. refer to "..\BWPlugin\schema\plugin_manifest.json" for more information.</br>
   Example of plugin.json file:
```json
{
  "identifier": {Your identifier},
  "name": {Your plugin name},
  "type": "python",
  "main": {Your plugin path},
}
```
  Note:'type' should always be python if you using python to create your plugin.

For this example, the file structure should look like this

```
SamplePlugin
│   plugin.json    
└───{Python package folder name}
    |   __init__.py
    |   sample.py
```

That's it! You just created your first plugin (which doesn't do anything yet). Go to 'API Usage' on the main page to extend your plugin. -->



## Debugging your plugin within Browzwear
1. Add VStitcher or Lotta as external tool in Eclipse: Click **Run > External Tools > External Tools Configurations..."**
2. Add new configuration: Click the **New** button
3. Under the **Name** write `Browzwear`
4. Under the **Location** field enter VStitcher / Lotta executable file
5. Click **Close**
6. Go back to your `sample.py` file and add the following code to the initialize function:

```python
import sys
sys.path.append(<path to pydevd/pysrc>)

def BwApiPluginInit() -> int:
  try:
    import pydevd

    # this line will cause the debugger to stop here and you will be able
    # to debug the plugin
    pydevd.settrace('localhost', port=5678)
  except:
    pass

  # add menu item to the plugin menu
  BwApi.MenuFunctionAdd('Hello World', callbackMenu, 1)
  return 1
```
7. Open the **Debug** perspective: Click **Window > Perspective > Open Perspective > Other ...**
8. Select the **Debug** perspective.
9. Set PyDev to listen to 5678 port: Click **Pydev > Start Debug Server**, you should see the following line on the console - `Debug Server at port: 5678`.
10. Launch VStitcher / Lotta from Eclipe using the configuration set at step #1:</br> Click **Run > External Tools > Browzwear**.
