# xsecurelock keyboard layout patch

Small local patch for XSecureLock v1.9.0.

## Problem

`XSECURELOCK_SHOW_KEYBOARD_LAYOUT=0` does not fully hide keyboard-related auth prompt text.

Even with the option disabled, the auth prompt can still show text such as:

- keyboard layout details
- Num Lock
- Scroll Lock
- Group 2
- keyboard switching hints

Related archived upstream issue: google/xsecurelock#163  
https://github.com/google/xsecurelock/issues/163

The upstream repository is archived/read-only, so this repo documents the local workaround.

## Patch

See:

`patches/hide-keyboard-status-when-layout-disabled.patch`

The patch makes `auth_x11` return no keyboard text when `show_keyboard_layout` is false.

## Tested environment

- Linux Mint 21.3 / Ubuntu Jammy base
- Cinnamon / X11
- XSecureLock v1.9.0 built from source
- Auth helper: `/usr/local/libexec/xsecurelock/auth_x11`

## License

This patch follows the upstream XSecureLock license: Apache-2.0.
