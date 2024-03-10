---
tags:
  - linux
---
# How to display keyboard modifiers

The `xmodmap` utility is used to display (and edit) the keyboard modifiers map (e.g. `ALT`, `CTRL`, `SHIFT`,  `WIN`, etc).

This may be useful when we need to configure other applications (like `i3`) to use such keys.

To show current key modifiers, just run:

```shell
xmodmap
```

This command will tell us that, for example, the `WIN` key corresponds to `mod4` modifier.
