# CodeMap - VSCode Extension

Interactive code map for quick visualization and navigation within  code DOM objects (e.g. classes, members).
<hr/>

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](http://www.csscript.net/Donation.html)
## Overview

This simple extension visualizes the code DOM objects defined in the active document. This extension is a for of the popular plugin that is available for:
* Sublime Text 3 - [Sublime CodeMap plugin](https://github.com/oleg-shilo/sublime-codemap/blob/master/README.md)
* Notepad++ - [Part of CS-Script.Npp plugin](https://github.com/oleg-shilo/cs-script.npp/blob/master/README.md)
* Visual Studio - [PyMap (python flavor extension)](https://marketplace.visualstudio.com/items?itemName=OlegShilo.PyMap)

The extension functionality is straight forward. Just click the code map item and it will trigger the navigation to the document where the corresponding code element is defined in the document.

_Features_:
* Supported syntaxes:
  * C#
  * TypeScript
  * JavaScript
  * Python
  * Java
  * Erlang
  * Markdown
  * PowerShell
  * R
  * JSON
  * XML
  * SVG
  * XAML  
* [Customization by adding support for new syntaxes via:](https://github.com/oleg-shilo/codemap.vscode/wiki/Adding-custom-mappers)
  * A generic mapptr thatis set of Regex expressions in user settings
  * A dedicated simple mapper JS script file.
* Auto-refreshing code map on document change.
* Navigation to code fragment associated with the clicked code map node.
* Refreshing on demand via "Refresh" toolbar button a and VSCode command.

![codemap_vscode.gif](https://raw.githubusercontent.com/oleg-shilo/codemap.vscode/master/resources/images/codemap_vscode.gif)

Note, the latest releases of CodeMap place the plugin view in its own activitrybar:

![image](https://user-images.githubusercontent.com/16729806/67156959-16bf4a80-f371-11e9-841b-dee1b9ba364e.png)

## Adding custom mappers
The most intriguing feature is the possibility to extend the plugin to support new and even more exotic syntaxes. Read more about the technique in this [Wiki page](https://github.com/oleg-shilo/codemap.vscode/wiki/Adding-custom-mappers). 

If you create mapping rules or dedicated mapper and want to share it with others. Create a pull request or just log the corresponding issue on this project and I will consider including your mapper into the plugin package. 

## Limitations

* The main objective of this plugin is not to provide the most accurate CodeDOM (syntax tree)  presentation but rather to assist with the navigation to the most important points in your code. Thus the default mappers deliberately avoid high resolution code parsing (e.g. local variables). 

* Currently VSCode has a defect associate with the expandable nodes selection:<br>
   https://github.com/Microsoft/vscode/issues/34130<br>
   https://github.com/patrys/vscode-code-outline/issues/24
   
   This defect makes it impossible to select a node (and consequently trigger the navigation) without toggling node's expanded state. While being cosmetic this defect can become quite annoying and affecting the overall User Experience.
   
   CodeMap offers a work around. You can enable the plugin `textMode` in the user setting:
   ```JASON
   "codemap.textMode": true
   ```
   In this mode the all nodes are made non-expandable and nesting is expressed via node text indent.

   _textMode disabled_<br>
   ![tree_mode.png](https://raw.githubusercontent.com/oleg-shilo/codemap.vscode/master/resources/images/tree_mode.png)

   _textMode enabled_<br>
   ![text_mode.png](https://raw.githubusercontent.com/oleg-shilo/codemap.vscode/master/resources/images/text_mode.png)
   




