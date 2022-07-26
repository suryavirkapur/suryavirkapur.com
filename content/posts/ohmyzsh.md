---
title: "ZSH Profile"
description: "Something"
date: 2022-02-26T08:47:11+01:00
draft: false
---

My profile for improving the default terminal.

## How to change?

```bash
vi ~/.zshrc
```

Open the config file and paste the settings below. You may need to edit for ZSH locations.

```bash
export ZSH="/root/.oh-my-zsh"

ZSH_THEME="robbyrussell"
CASE_SENSITIVE="true"

DISABLE_LS_COLORS="false"
ENABLE_CORRECTION="true"

HIST_STAMPS="mm/dd/yyyy"

plugins=(git)
source $ZSH/oh-my-zsh.sh

# Very important for me
export LANG=en_US.UTF-8
export UPDATE_ZSH_DAYS=7

# Use vim on servers and mvim on wsl
if [[ -n $SSH_CONNECTION ]]; then
  export EDITOR='vim'
else
  export EDITOR='mvim'
fi

export ARCHFLAGS="-arch x86_64"
```
