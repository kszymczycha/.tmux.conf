# tmux-conf

Custom tmux configuration file:

```vim
# Start window index from 1
set -g base-index 1

# Change history limit
set -g history-limit 10000

# Set mouse on
set -g mouse on

# Widgets
wg_prfx="#{?client_prefix,<Prefix>,}"
wg_time="#[bold]%H:%M"
wg_date="#[bold]%d-%b-%Y"
set -g status-right "${wg_prfx} ${wg_date} ${wg_time}"

# Appearance
set -g status-style bg=colour235,fg=colour10
set -g window-status-current-style bg=colour236,fg=colour255,bold

# Reload configuration after select prefix + r
bind r source-file ~/.tmux.conf \; display "Tmux configuration reloaded"
```