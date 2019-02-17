# Compiling & Flashing

When you're happy with your new `venabili.c`, compile it with:

```
$ cd src
$ make
```

Notice that some checks will run and let you know if you forgot to put some
important keys in your layers.

If everything went right and no errors are displayed, you may now flash the new
firmware into your keyboard. To do so, the keyboard needs to be in *flash mode*
first, there are two ways:

1. Plug in the keyboard while pressing the top left key (the keyboard needs to
be unplugged beforehand)
2. Use the *flash mode key* (`c_flash_mode`) if it's already declared in your
layers (No need to unplug the keyboard)

Then flash the new firmware with:

```
$ cd src
$ make burn
```

When the process is finished your keyboard will be back online and ready to use.
