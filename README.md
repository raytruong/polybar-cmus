# polybar-cmus

Basic cmus module for polybar

/u/WozarZ's cmus script, but I cleaned up issues relating to capturing artist name and string dump when no track is running.

```ini
[module/cmus]
type = custom/script

exec = ~/.config/polybar/cmus.sh
exec-if = pgrep -x cmus
interval = 1

click-left = cmus-remote --next
click-right = cmus-remote --prev
click-middle = cmus-remote --pause
scroll-up = cmus-remote --volume +5%
scroll-down = cmus-remote --volume -5%

label-font = 3
format = <label>
format-underline = ${colors.foreground-alt}
label = %output%
label-maxlen = 50
```
