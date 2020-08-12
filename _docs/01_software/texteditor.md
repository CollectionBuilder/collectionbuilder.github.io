---
title: Get a Text Editor
stub: text-editor
section: software
section_order: 1
---

{:.py-4 .mt-4 #text-editor}
***

## 1. Get a Text Editor

The CollectionBuilder team suggests these open-source, cross platform options for text editors:

- [Visual Studio Code](https://code.visualstudio.com/){:target="_blank" rel="noopener"} (VS Code)
- [Atom](https://atom.io/){:target="_blank" rel="noopener"}

If you don't have one of these text editors installed, visit their sites, download the software, and use their wizards to install the software on your computer. 

We mostly use Visual Studio Code, so if you don't know which one to pick, go ahead and get that one. 
For additional assistance, see our guides for [How to Install and Set Up Visual Studio Code](https://lib-static.github.io/howto/howtos/visualstudiocode.html){:target="_blank" rel="noopener"} and [How to Install and Set Up Atom](https://lib-static.github.io/howto/howtos/installatom.html){:target="_blank" rel="noopener"}

{% capture vscode %}
Visual Studio Code (VS Code) has a tremendous number of extensions that can be added to enhance it's functionality. We recommend [Rainbow CSV](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv){:target="_blank" rel="noopener"}, which will help you better read the CSVs within CollectionBuilder, and [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker){:target="_blank" rel="noopener"}, which will check your spelling. 

VS Code is incredibly customizable via its settings as well. When you first install VS Code, however, the default settings can be distracting. To configure the editor, click the *gear icon* in the bottom left corner of the VSCode window and choose *Settings*.
The searchable *Settings* pane has information about all the configuration options.

To make it easy to share settings, you can also paste values into your **settings.json** file which represents all the options customized on the *Settings* pane.
Click the *file icon* in the upper right of the *Settings* pane to view your configuration as JSON.
Copying and pasting the JSON snippet below into your settings will turn off some of the distraction. 

```
{
    "editor.minimap.enabled": false,
    "editor.wordWrap": "on",
    "html.format.maxPreserveNewLines": 2,
    "html.format.wrapLineLength": 0,
    "editor.codeLens": false,
    "outline.problems.badges": false,
    "outline.problems.enabled": false,
    "outline.problems.colors": false,
    "problems.decorations.enabled": false,
    "problems.autoReveal": false
}
```

Once you paste it in, save (`CTRL + S`) and close the **settings.json** file.
{% endcapture %}
{% include bootstrap/card.md text=vscode header="Configuring Visual Studio Code (Optional)" %}
