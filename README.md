[![stand with Ukraine](https://img.shields.io/badge/stand_with-ukraine-ffd700.svg?labelColor=0057b7)](https://stand-with-ukraine.pp.ua)
# CodeMap - VSCode Extension

Interactive code map for quick visualization and navigation within code DOM objects (e.g. classes, members).
<hr/>

[![Github All Releases](https://github.com/oleg-shilo/codemap.vscode/releases)]()

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.cs-script.net/cs-script/Donation.html)

## Overview

This simple extension visualizes the code DOM objects defined in the active document. This extension is a for of the popular plugin that is available for:
* Sublime Text 3 - [Sublime CodeMap plugin](https://github.com/oleg-shilo/sublime-codemap/blob/master/README.md)
* Notepad++ - [Part of CS-Script.Npp plugin](https://github.com/oleg-shilo/cs-script.npp/blob/master/README.md)
* Visual Studio - [CodeMap (ex-PyMap)](https://marketplace.visualstudio.com/items?itemName=OlegShilo.PyMap)

The extension functionality is straightforward. Just click the code map item and it will trigger the navigation to the document where the corresponding code element is defined in the document.

_Features_:
* Supported syntaxes:
  * C#
  * TypeScript
  * JavaScript
  * React (TSX/JSX)
  * Python
  * Java
  * Erlang
  * Markdown
  * PowerShell
  * R
  * GO
  * JSON
  * XML
  * SVG
  * XAML  
  * TCL
  * VB.NET
  * PDL2 (Comau Robot Language)
  * LScript
  * Vericode
* [Customization by adding support for new syntaxes via:](https://github.com/oleg-shilo/codemap.vscode/wiki/Adding-custom-mappers)
  * A generic mapper that is a set of Regex expressions in user settings
  * A dedicated simple mapper JS script file.
* Auto-refreshing code map on document change.
* Navigation to code fragment associated with the clicked code map node.
* Refreshing on demand via "Refresh" toolbar button and VSCode command.

![codemap_vscode.gif](https://raw.githubusercontent.com/oleg-shilo/codemap.vscode/master/resources/images/codemap_vscode.gif)

Note, the latest releases of CodeMap place the plugin view in its own activity bar:

![image](https://github.com/user-attachments/assets/f29082b7-5ad1-4431-85d9-29c22f466b78)

## Adding custom mappers
The most intriguing feature is the possibility to extend the plugin to support new and even more exotic syntaxes. Read more about the technique in this [Wiki page](https://github.com/oleg-shilo/codemap.vscode/wiki/Adding-custom-mappers). 

If you create mapping rules or a dedicated mapper and want to share it with others. Create a pull request or just log the corresponding issue on this project and I will consider including your mapper in the plugin package. 

## Limitations

* The main objective of this plugin is not to provide the most accurate CodeDOM (syntax tree)  presentation but rather to assist with navigating to the most important points in your code. Thus the default mappers deliberately avoid high-resolution code parsing (e.g. local variables). 



