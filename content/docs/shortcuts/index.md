---
title: "Shortcuts & Keybindings"
date: 2019-02-11T19:27:37+10:00
weight: 5
summary: "Useful short cuts for Editors, IDE's, and Tools"
---

### tmux shortcuts

start new:

```bash
tmux
```

start new with session name:

```bash
tmux new -s myname
```

attach:

```bash
tmux a  #  (or at, or attach)
```

attach to named:

```bash
tmux a -t myname
```

list sessions:

```bash
tmux ls
```

kill session:

```bash
tmux kill-session -t myname
```

Kill all the tmux sessions:

```
tmux ls | grep : | cut -d. -f1 | awk '{print substr($1, 0, length($1)-1)}' | xargs kill
```

In tmux, hit the prefix `ctrl+b` (my modified prefix is ctrl+a) and then:

#### Sessions

    :new<CR>  new session
    s  list sessions
    $  name session

#### Windows (tabs)

    c  create window
    w  list windows
    n  next window
    p  previous window
    f  find window
    ,  name window
    &  kill window

#### Panes (splits)

    %  vertical split
    "  horizontal split

    o  swap panes
    q  show pane numbers
    x  kill pane
    +  break pane into window (e.g. to select text by mouse to copy)
    -  restore pane from window
    ⍽  space - toggle between layouts
    <prefix> q (Show pane numbers, when the numbers show up type the key to goto that pane)
    <prefix> { (Move the current pane left)
    <prefix> } (Move the current pane right)
    <prefix> z toggle pane zoom
