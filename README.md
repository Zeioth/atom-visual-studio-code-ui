## Atom Visual Studio Code UI theme [![Build Status](https://travis-ci.org/atom/one-dark-ui.svg?branch=master)](https://travis-ci.org/atom/one-dark-ui)

![Banner Atom Visual Studio Code UI](https://cloud.githubusercontent.com/assets/3357792/10440872/3af1d882-7143-11e5-9df9-2c1d0aa5e919.png)

This theme aims to reproduce the exact feeling of work with Visual Studio Code. So you don't need to renounce to the features of Atom to enjoy a great workflow. It looks even better with monokai syntax. If you prefer, there is an [alternative version](https://atom.io/themes/atom-visual-studio-code-light-ui) in light colors.

Made by [@Zeioth](https://twitter.com/Zeioth)

---

![atom-visual-studio-code-ui](https://cloud.githubusercontent.com/assets/3357792/10440991/538ad92e-7144-11e5-8a93-b4752fa40f2b.png)

### Install your toolbar

After you install this theme you'll only have the color scheme of __Visual Studio Code__. To enjoy the full experience you must install the next packages.

1. `tool-bar` by suda - This will enable the sidebar. You can set the position to left.
2. `flex-tool-bar` by cakecatz - It will allow us to configure the elements of the tool-bar.
3. `git-plus` by akonwi - Having this you can run git commands from your toolbar.

### Customize your toolbar

You can't see the toolbar yet. To configure it, you must press ctrl+shift+p and write "Flex Tool Bar: Edit Config File". Then paste this code and save it. You should be able to see your new toolbar after restart Atom.

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
__My toolbar icons are too small!__
You can edit the size of the icons in "Preferences > Packages > Tool-bar".

__Something has an incorrect color or size?__
Go to our Github repository, and open an issue uploading an image of your problem. I will fix it as soon as possible. Also, this theme is based on One Dark UI, so if you need further help, please refer to the documentation of said theme.
