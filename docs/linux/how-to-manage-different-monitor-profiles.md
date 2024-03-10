---
tags:
  - linux
---
# How to manage different monitor profiles

We want to configure different monitor profiles, say:
- a "mobile" profile: the laptop display only;
- a "home" profile: a dual screen setup;
and we want to be able to quickly switch between the two from the command line.

We can use [autorandr](https://github.com/phillipberndt/autorandr) :  this tool will utomatically select a display configuration based on connected devices.
It can also save and load configuration profiles.

Install `autorandr`:
```shell
apt install autorandr
```

Show the current configuration:

```shell
autorandr --config
```

List available profiles:

```shell
autorandr
```

Save the current configuration into a named profile:

```shell
autorandr --save home
```

Load a named profile:

```shell
autorandr --load home
```

Autorandr saves its configuration profiles in the `~/.config/autorandr/<PROFILE_NAME>` folder.
