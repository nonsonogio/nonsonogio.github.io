---
tags:
  - linux
---
# How to change keyboard layout from CLI

The keyboard layout can be changed from the command line using the `setxkbmap` utility.

Set the US layout:

```shell
setxkbmap -layout us
```

Set the US layout with dead keys:

```shell
setxkbmap -layout us -variant intl
```

Set the Italian layout:

```shell
setxkbmap -layout it
```

## Show key modifiers

To show current key modifiers, just run:

```shell
xmodmap
```
