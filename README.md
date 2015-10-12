## Atom Visual Studio Code UI theme [![Build Status](https://travis-ci.org/atom/one-dark-ui.svg?branch=master)](https://travis-ci.org/atom/one-dark-ui)

![Banner Atom Visual Studio Code UI](https://cloud.githubusercontent.com/assets/3357792/10440872/3af1d882-7143-11e5-9df9-2c1d0aa5e919.png)

This theme aims to reproduce the exact feeling of work with Visual Studio Code. So you don't need to renounce to the features of Atom to enjoy a great workflow. It looks even better with monokai syntax.

Made by [@Zeioth](https://twitter.com/Zeioth)

---

![atom-visual-studio-code-ui](https://cloud.githubusercontent.com/assets/3357792/10440991/538ad92e-7144-11e5-8a93-b4752fa40f2b.png)

### Install your toolbar

After you install this theme you'll only have the color scheme of __Visual Studio Code__. To enjoy the full experience you must install the next packages.

1. `tool-bar` by suda - This will enable the sidebar. You can set the position to left.
2. `flex-tool-bar` by cakecatz - It will allow us to configure the elements of the tool-bar.

It's possible you need to restart Atom to see your toolbar.

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
```css
.theme-atom-visual-studio-code-ui {
  atom-text-editor {
    background-color: #272822;
  }
}
```
__Something has an incorrect color or size?__
Go to our Github repository, and open an issue uploading an image of your problem. I will fix it as soon as possible. Also, this theme is based on One Dark UI, so if you need further help, please refer to the documentation of said theme.

__Know bugs:__
There is a problem with the status bar where you can't read the last line of a text file. To solve this open your style.less and write:
```css
.theme-atom-visual-studio-code-ui {
  .status-bar{
    position: relative;
  }
}
```
