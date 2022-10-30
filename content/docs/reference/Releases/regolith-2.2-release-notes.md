---
title: "2.2 Release Notes"
linkTitle: "2.2 Release Notes"
weight: 5
description: >
  Release notes for Regolith 2.2
---

# NOTE: Regolith 2.2 is in beta testing.  This release announcement is a work in progress.

[Regolith 2.2](https://github.com/orgs/regolith-linux/projects/25) is a minor release focusing on bug fixes and Ubuntu 22.10 support.

## New Features

* Wallpaper may be changed in `regolith-control-center` on Ubuntu Kinetic and Debian Bookworm.

## Bug Fixes

* `i3-swap-focus` now available as released in 2.1

## Known Issues

* No localization for `ilia` 

## Changelog Delta from Regolith Desktop 2.1 to 2.2

### Changes in `regolith-session`:
```
0047f4d File checks allow symlinks. Address https://github.com/regolith-linux/regolith-desktop/issues/732
```

### Changes in `i3-wm`:
```
39afa033 release i3 4.21.1
```

### Changes in `i3-gaps-wm`:
```
a8546a08 release i3-gaps 4.21
```

### Changes in `regolith-i3-config`:
```
9acba1a Add work around for border issue https://github.com/i3/i3/issues/5149
72045f8 Add padding to workspace indicator on bar for simple looks
7865f93 Simplify font spec in i3 workspace label. Allow xres override of bar font to address https://github.com/regolith-linux/regolith-desktop/issues/730
b1cf838 Allow resize increment to be specified via xres. Address https://github.com/regolith-linux/regolith-i3-config/issues/11
3deafab Change float modifier due to change in gtk4
cfe26d7 Fix keybinding comment for swap focus
```

### Changes in `regolith-look-default`:
```
0577cbe Simplify font spec in i3 workspace label. Allow xres override of bar font to address https://github.com/regolith-linux/regolith-desktop/issues/730
deba53b Add conflicts to prevent package install failure
ff98eb4 Decompose look and loader script for cleaner dependency. Use virtual package for resource loading to generalize between x11 and wayland
1942cee Added support for wayland
```

### Changes in `regolith-look-extra`:
```
fa39ffe More color mapping fixes
e5e786b Fix missing color specs
add5508 Simplify font spec in i3 workspace label. Allow xres override of bar font to address https://github.com/regolith-linux/regolith-desktop/issues/730
408fa51 Cleanup dependencies to default look
f3da9b9 Fix package metadata for regolith-look-2 virtual package, found by Matt Fischer
c3076f0 Make gruvbox i3xrocks values a brighter color
e0e049a Fix paths to compositor
a7018ec Decouple picom from looks. relates to https://github.com/regolith-linux/regolith-look-extra/pull/8
f70c4de Remove picom as a dependency of Nord and Nevil looks
632c175 updated Debian package metadata to install moka-icon-theme
1287be9 Add missing regolith-look-ayu-mirage look to debian packaging
```

### Changes in `i3-next-workspace`:
```
e886bf5 Predicate list building on presence of seperator character. Attempt building from anon workspace
```

### Changes in `regolith-i3xrocks-config`:
```
c524c6e Remove floating flags for gtk4 breaking change in regolith-control-center
963c2b8 Add scrolling as inputs to media-player (#141)
425fe9e Try to use bluetooth device alias instead of name (#142)
f3e9e48 Depend on netcat-openbsd due to bsd specific options used.  Address https://github.com/regolith-linux/regolith-desktop/issues/635
e7d7c3f volume: extract toggle, volume_up, volume_down functions for easy rebinding (#140)
7ec4e6c Exit 0 if network device unfound to avoid spamming logs
659f13e Fixed volume and microphone mixer_value to display values below 10 and (#137)
2d09694 Rename install file for tailscale (#138)
```

### Changes in `regolith-ftue`:
```
b8255d6 Add missing dependency
```

### Changes in `regolith-compositor-compton-glx`:
```
7980eb1 Allow config to be specified by Xres. Relates to https://github.com/regolith-linux/regolith-look-extra/pull/8
```

### Changes in `regolith-compositor-picom-glx`:

```
ee673f1 Allow config to be specified by Xres. Relates to https://github.com/regolith-linux/regolith-look-extra/pull/8
```


### Changes in `ilia`:
```
d1573ff Update version in build. Do not sort textlist entries. Add flag for no icon in textlist.
6e4de4a Update selection logic to address https://github.com/regolith-linux/ilia/issues/44. Misc cleanup
4683479 Simply use URI to launch selected app from tracker page. Address https://github.com/regolith-linux/regolith-desktop/issues/716
f9eacc0 Move from XDG_DATA_DIRS to dconf source for desktop app paths
f1dd370 Ignore i3bar explicitly with looser filter
d151347 Include windows in window list containing empty value for 'window_type'. Addresses https://github.com/regolith-linux/ilia/issues/43
753160d Close dialog on selection for tracker page. exit regardless of error state in desktop app and tracker pages. Address https://github.com/regolith-linux/ilia/issues/39
```

### Changes in `xrescat`:

```
bd6a6cb Add virtual package regolith-resource-loader for future wayland support```
```