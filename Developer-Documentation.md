**Zulip Terminal** is a light and fast terminal client for [Zulip](https://zulipchat.com). It's written in python and :snake: only.

## Overview
Zulip Terminal uses [Zulip's API](https://zulipchat.com/api/) to store and retrieve all the information it displays. It has an [MVC structure](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) overall. Here is a description of some of it's files:
 
| File/Folder                                           | Description                                   |
| ----------------------------------------------------- | --------------------------------------------- |
|zulipterminal/                                         | Root Folder - Contains all the source files   |
|              ui.py                                    | Controls where each component is displayed    |
|              core.py                                  | Runs the app and controls data flow into View |
|              model.py                                 | Fetches and stores data retrieved from server |
|              helper.py                                | Helper functions used at multiple places      |
|              config.py                                | Stores keybindings along with what they do    |
|              ui_tools                                 | Has all the UI elements displayed by View     |
|              cli/run.py                               | Runs the app                                  |

Zulip Terminal uses [urwid](http://urwid.org/) to render the UI components in terminal. Urwid is an awesome library through which you can render a decent terminal UI just using python. [Urwid's Tutorial](http://urwid.org/tutorial/index.html) is a great place to start for new contributors.

## Tests
Tests for zulip-terminal are written using [pytest](https://pytest.org/). You can read the tests in `/tests` folder to learn about writing tests for a new class/function. If you are new to pytest, reading it's documentation is definitely recommended.


## Tutorial - Adding typing indicator
This tutorial shows how typing indicator was implemented in the client. The process for adding a new feature to zulip terminal varies greatly depending on the feature. This tutorial is intended to make you familiar with the general process.

Since the typing indicator data for the other user in pm cannot be generated locally, it must something which should be received from the client.

A quick google search for `zulip typing indicator` points to https://zulip.readthedocs.io/en/latest/subsystems/typing-indicators.html. This document explains how typing indicator is implemented on the web client and is useful in understand how typing indicator works internally.

You can find most of the web features documented in https://zulip.readthedocs.io/en/latest/subsystems and understand how they work internally.

https://chat.zulip.org/api/ shows how to reach the endpoints and what response to expect from the server.