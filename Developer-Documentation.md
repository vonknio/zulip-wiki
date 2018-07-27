**Zulip Terminal** is a light and fast terminal client for [Zulip](https://zulipchat.com). It's written in python and :snake: only.

## Overview
Zulip Terminal uses [Zulip's API](https://zulipchat.com/api/) to store and retrieve all the information it displays and uses [MVC structure](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller). Here is a description of some of it's files:
 
| File/Folder                                           | Description                                   |
| ----------------------------------------------------- | --------------------------------------------- |
|zulipterminal/                                         | Root Folder - Contains all the source files   |
|              ui.py                                    | Controls where each component is displayed    |
|              core.py                                  | Runs the app and controls data flow into View |
|              model.py                                 | Fetches and stores data retrieved from server |
|              helper.py                                | Helper functions used at multiple places  |
|              config.py                                | Stores keybindings along with what they do    |
|              ui_tools                                 | Has all the UI elements displayed by View     |
|              cli/run.py                               | Runs the app                                  |