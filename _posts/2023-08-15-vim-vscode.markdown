---
layout: post
title: An incomplete guide to setting up Vim in VS Code
date: 2023-08-15
permalink: /vim-vscode
---

I learned Vim 3 weeks ago. Since then I am using the Vim emulator in VS Code for programming. I also started using Obsidian because I wanted to practice Vim for writing prose as well.

I first learned about Vim about 2 years ago but didn't pay any attention it. I thought people using it learned it before modern IDEs are were just resistant to change.

I still don't think it's a good idea to use Vim as a full-blown IDE. Vim motions, however, are pretty cool and very helpful during programming.

With that, here are some tips for making Vim work for you in general and in VS Code.

### Learn Vim

Learn Vim using `vimtutor`. It's the best way to learn Vim. The exercises are to the point and short. You could go through the whole thing in half a day.

### Escape Key

Remap the `Caps Lock` key on your keyboard to `Ctrl`. The Ctrl key is used frequenly in Vim and also in other applications. You could easily switch from Insert to Normal Mode using `Ctrl + [` shortcut, instead of pressing the `Esc` which is harder to reach.

### VS Code Settings

Add the following to your `settings.json` file in VS Code:

```
"vim.handleKeys": {
    "<C-w>": false // Close file using Ctrl + w
  },
"vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["<C-j>"], // Move line down using Ctrl + j
      "commands": ["editor.action.moveLinesDownAction"]
    },
    {
      "before": ["<C-k>"], // Move line up using Ctrl + k
      "commands": ["editor.action.moveLinesUpAction"]
    }
  ],
```

### VS Code shortcuts

Make use these VS Code shortcuts to work with files and do IDE related tasks:

- `Ctrl + Tab` to switch between open files
- `Ctrl + 1/2/3` to go to nth positioned open file
- `` Ctrl + ` `` to open the integrated terminal
- `Ctrl + b` to open the file explorer
- `Ctrl + Shift + f` to search the entire codebase

Try Vim for a week. You'll learn something new and there's a good chance you'll like it.

Happy Vimming (????)
