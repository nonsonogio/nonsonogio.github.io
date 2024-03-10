---
tags:
  - linux
---
# How to configure monitors from CLI

We may need to configure monitors from the command line in Linux. To the purpose we can use the `xrandr` utility.

Display available monitors:

```shell
xrandr --listmonitors
```

Use the monitor connected to _DisplayPort-6_ and set it as primary:

```shell
xrandr --output DisplayPort-6 --auto --primary
```

Add the monitor connected to _DisplayPort-7_  placed to the right of the first one connected to _DisplayPort-6_:

```shell
xrandr --output DisplayPort-7 --auto --right-of DisplayPort-6
```

Disconnect the native laptop display:

```shell
xrandr --output eDP --off
```

Enable the native laptop display:

```shell
xrandr --output eDP --auto
```

Reset displays:

```shell
xrandr -s 0
```


## References

- [Multihead - ArchWiki](https://wiki.archlinux.org/title/Multihead)

## See also

- [[how-to-manage-different-monitor-profiles]]
