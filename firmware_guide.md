# Building Guide

## Firmware

The firmware that makes Venabili work is actually made of two parts:
the *bootloader* and the *main firmware*, where the actual useful stuff is.

When the microcontroller is brand-new, you need to flash both parts on it using
special (though very inexpensive) hardware. After that, only new versions of the
*main firmware* need to be flashed whenever you change your layers, macros, etc;
And the special programming hardware is no longer needed, you can do it pretty
easily and quickly with your keyboard plugged in as normal.

Throughout these documents, the process of flashing for the first time with
special hardware will be known as *"low level"* flashing. And the process of
flashing the main firmware each time you want to change your keyboard's
behaviour as *"user level"* flashing.


### Low Level Flashing

Because we're still building the keyboard, we're only going to address the
first-time-only low level flashing here and let the user level flashing for the
[Customizing Guide](customizing.md).