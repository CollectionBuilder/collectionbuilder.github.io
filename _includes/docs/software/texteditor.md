{:.py-4 .mt-4 #text-editor}
***

## 1. Get a Text Editor

All code is [plain text](https://en.wikipedia.org/wiki/Plain_text), and all plain text can be edited by a "text editor." 
Word processors, such as MS Word, can not be used to create or edit code, as they  do not handle plain text without altering it.
For basic editing, Windows [Notepad++](https://notepad-plus-plus.org/), Mac TextEdit, or Linux Gedit are sufficient.
However, for a Jekyll project such as CollectionBuilder, a more complete code editor is recommended. 

The CollectionBuilder team suggests these open-source, cross platform options for text editors:

- [Visual Studio Code](https://code.visualstudio.com/) (VS Code)
- [Atom](https://atom.io/)

If you don't have one of these text editors installed, visit their sites, download the software, and use their wizards to install the software on your computer. 
We mostly use Visual Studio Code, so if you don't know which one to pick, go ahead and get that one. 
For additional assistance, see our guides for [How to Install and Set Up Visual Studio Code](https://lib-static.github.io/howto/howtos/visualstudiocode.html){:target="_blank"} and [How to Install and Set Up Atom](https://lib-static.github.io/howto/howtos/installatom.html){:target="_blank"}

{% capture vscode %}
When you first install VS Code, the default settings can be distracting. 
To configure the editor, click the *gear icon* in the bottom left corner of the VSCode window and choose *Settings*.
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
{% include bootstrap/card.md text=vscode header="Configuring Visual Studio Code" %}