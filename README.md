# xsecurelock-keyboard-layout-patch
XSECURELOCK_SHOW_KEYBOARD_LAYOUT=0 in v1.9.0 does not fully hide keyboard auth text. It still shows Keyboard layout, Num/Scroll Lock, Group 2, and switch-layout hints. Local patch: return empty keyboard string when show_keyboard_layout=false. Related archived upstream: google/xsecurelock#163
