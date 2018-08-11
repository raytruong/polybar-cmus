# polybar-cmus

Basic cmus module for polybar

/u/WozarZ's cmus script, but I cleaned up issues relating to capturing artist name and string dump when no track is running.

```ini
[module/cmus]
type = custom/script

exec = sh ~/.config/polybar/cmus.sh
exec-if = pgrep -x cmus
interval = 1

click-left = cmus-remote --pause
click-right = cmus-remote --stop

format = <label>
format-underline = ${colors.primary}
label = %output%
```
