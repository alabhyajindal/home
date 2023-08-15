---
layout: post
title: An incomplete guide to setting up Vim in VS Code
date: 2023-08-15
permalink: /vim-vscode
---

I learned Vim 3 weeks ago and have been using it since for all my editing tasks. I am using the Vim emulator in VS Code for programming. I started using Obsidian because of it has a Vim mode and I wanted to practice Vim for writing prose as well.

I first learned about Vim about 2 years ago but didn't pay any attention it. I disregared everyone's raving opinions on it by thinking to myself that those people are creatures of habit: that these people learned Vim some time ago before modern IDEs existed and are just resistant to change.

My opinion has not taken a 180 just yet. I am not yet convinced whether it's a good idea to use Vim as a full-blown IDE. But I am conviced that Vim motions are pretty cool and very helpful during programming.

With that, here are some tips for making Vim work for you in general and in VS Code.

### Learn Vim

Make all tips short and to the point, like Derek Sivers. eg. Learn Vim from vimtutor. (Explain why)

I learned Vim using `vimtutor` and I think it's the best way to learn Vim. The exercises are to the point and short. You could go through the whole thing in half a day.

### Escape Key

I would highly recommend it to map the Caps Lock key on your keyboard to Ctrl. I had mapped mine already to this before starting to use Vim and it's very helpful across all applications. A lot of Vim users map their Caps Lock to Escape which is also a decent option, which I tried for 2 days. The problem with this is that a lot of applications use Ctrl frequently, and the mapped Caps Lock comes in handy in those situations. We need to make use Ctrl from time to time in Vim as well for things like next suggestion (Ctrl + n) or previous suggestion (Ctrl + p).

### VS Code Settings

I have added the following to my `settings.json` file in VS Code:

```
"vim.handleKeys": {
    "<C-w>": false
  },
"vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["<C-j>"],
      "commands": ["editor.action.moveLinesDownAction"]
    },
    {
      "before": ["<C-k>"],
      "commands": ["editor.action.moveLinesUpAction"]
    }
  ],
```

The first setting ensures I can close open tabs in the editor using the shortcut `Ctrl + w`.

The second and third setting allow me to move lines up or down using the shortcuts `Ctrl + k` and `Ctrl + j` respectively.

### VS Code shortcuts

There are a great many VS Code shortcuts that I continue to use to do IDE related tasks. Some of the ones I use most frequently are:

- `Ctrl + Tab` to switch between open files
- `Ctrl + 1/2/3` to go to nth positioned open file
- `` Ctrl + ` `` to open the integrated terminal
- `Ctrl + b` to open the file explorer
- `Ctrl + Shift + f` to search the entire codebase

I'm able to move around pretty quickly in the IDE because of these shortcuts. I was using these earlier and continue to do so alongside Vim.

To me using Vim with VS Code feels like getting the best of both worlds. You get to use an editor with a long history specially made for programming and you get the benefits of fully-featured modern IDE with useful features like autocomplete and file explorer.

Extending Vim and overwriting it's shortcuts in VS Code is pretty easy. Play around with it and find a combination that works for you. If you are unsure then the tips mentioned above are a good starting point. Happy Vimming (????)
