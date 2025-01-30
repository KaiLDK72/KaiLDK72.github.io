---
title: ChessX laeuft nicht richtig unter Wayland
categories: [Blog,Knowledge,Linux]
tags: [Linux]
---

Bei mir lief ChessX nicht richtig unter Wayland.
Der Fehler war immer:
```bash
qt.qpa.wayland: Failed to load client buffer integration: "wayland-egl"
qt.qpa.wayland: Available client buffer integrations: ()
qt.qpa.wayland: No shell integration named "xdg-shell" found
qt.qpa.wayland: No shell integration named "xdg-shell-v6" found
qt.qpa.wayland: No shell integration named "wl-shell" found
qt.qpa.wayland: No shell integration named "ivi-shell" found
qt.qpa.wayland: Loading shell integration failed.
qt.qpa.wayland: Attempted to load the following shells ("xdg-shell", "xdg-shell-v6", "wl-shell", "ivi-shell")
```
Ich musste dann entweder umstellen auf X11 oder aber folgendes 
probieren:
```bash
export QT_QPA_PLATFORM=xcb
```

