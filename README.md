## Atom Visual Studio Code UI theme [![Build Status](https://travis-ci.org/atom/one-dark-ui.svg?branch=master)](https://travis-ci.org/atom/one-dark-ui)

The experience of Visual Studio Code, now in Atom.

![atom-visual-studio-code-ui](https://cloud.githubusercontent.com/assets/3357792/10409519/4a0a6c88-6f24-11e5-9316-95405d82038b.png)

### Install

You can install it using Atom under __Settings > Install__ and can be activated by going to the __Settings > Themes__ section and selecting "Atom Visual Studio Code" from the __UI Themes__ drop-down menu.

### Install your toolbar

After installing this theme you'll only have the color scheme of __Visual Studio Code__. To enjoy the full experience you must install the next packages.

1. `tool-bar` by Suda - This will enable the sidebar. You can set the position to left.
2. `Flex-tool-bar` - It will allow us to configure the elements of the tool-bar.

This theme will modify the color scheme of this packages to match Visual Studio Code.

### Customize your toolbar

To set the items of the toolbar, you must press right click in the toolbar and select "Edit toolbar". Then paste this code and save it. You should see the changes immediately.

```json
[
  {
    type: "button"
    iconset: "ion"
    icon: "ios-copy"
    callback: "tree-view:toggle"
    tooltip: "Toggle Project Tree"
  }
  {
    type: "button"
    iconset: "fa"
    icon: "columns"
    tooltip: "Split Screen"
    callback: ["pane:split-right"]
  }
  {
    type: "button"
    iconset: "devicon"
    icon: "git-plain"
    callback: "git-plus:menu"
    tooltip: "Git"
    style:
      color: "#0198E1"
  }
  {
    type: "url"
    iconset: "ion"
    icon: "bug"
    url: "http://localhost:8000"
    tooltip: "Debug Django Project"
    show: [ "Python", "HTML", "JavaScript" ]
  }
]
```

### FAQ
__Can I custumize this theme?__
Yes, you can change anything in your styles.less like this:
```
.theme-atom-visual-studio-code-ui {
  atom-text-editor {
    //background-color: #272822;
  }

  .tree-view {
    font-size: 1.1em;
    background-color: #252526;
  }
}
```
__Something has an incorrect color or size?__
Go to our Github repository, and open an issue uploading an image of your problem. I will fix it as soon as possible. Also, this theme is based on One Dark UI, so if you need further help, please refer to the documentation of said theme.
