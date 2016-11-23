[Tmux](http://tmux.sourceforge.net/) is a terminal multiplexer. Tested with tmux 1.5 and 1.6.

This config has support for [tmux-mem-cpu](http://github.com/thewtex/tmux-mem-cpu-load).

Prefix mapped to Ctrl-Q for `emacs` users sanity.

Installation
------------

  Download:

```bash
git clone https://github.com/thearthur/tmux-config.git ~/.tmux-config
```

  Copy tmux config to home:

```bash
ln -s ~/.tmux-config/.tmux.conf ~/.tmux.conf
```

  Go to config dir:

```bash
cd ~/.tmux-config
```

  Prep ourself to download submodule:

```bash
git submodule init
```

  Download submodule:

```bash
git submodule update
```

  Change dir to tmux-mem-cpu-load:

```bash
cd ~/.tmux-tony/vendor/tmux-mem-cpu-load
```

  General make file:

```bash
cmake .
```

  Compile our binary:

```bash
make
```

  Install our binary to `/usr/local/bin/tmux-mem-cpu-load`:

```bash
sudo make install
```

  Go home:

```bash
cd ~
```

  Update config:

```bash
tmux source-file ~/.tmux.conf
```

Start tmux
----------

  To start a session:

  `tmux`

  To reattach a previous session:

  `tmux attach`

  To reload config file

  `<Control + b>:` (which could Ctrl-B or Ctrl-A if you overidden it) then `source-file ~/.tmux.conf`

Commands
--------

  Our prefix/leader key is `Control + q` now. This sequence must be typed before any tmux shortcut.

  * `Control + q` before any command
  * `Control + q` then `?` to bring up list of keyboard shortcuts
  * `Control + q` then `"` to split window
  * `Control + q` then `<Space>` to change pane arrangement
  * `Control + q` then `o` to rotate panes
  * `Control + q` then `h`, `j`, `k`, `l` to move left, down, up, right. Respectively. (vim hjkl)
  * `Control + q` then `;` to go to last panel

  Beyond your first window:

  * `Control + q` then `c` to create a new window
  * `Control + q` then `n` to next window
  * `Control + q` then `p` to previous window
  * `Control + q` then `[0-9]` move to window number
  * `Control + q` then `&` to kill window


All the good stuff is by Tony Narlock (tony@git-pull.com)
This revision's bugs and arbitrary opinions provided by: Arthur Ulfeldt (arthur@ulfeldt.com)

Prais and appreciation goes to:
* Github: http://www.github.com/tony
* Website: http://www.git-pull.com

Complaints and critisims go to 
* Github: http://www.github.com/thearthur 
