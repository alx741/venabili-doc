# Keys

The `keys.h` file contains an exhaustive list of the keys you have available for
use in your layers. You could also take a look at the [Available
Keys](available_keys.md) section.

As you may have notice, normal keys have a `k_` prefix, there is no much about
them other than the fact that you have independent keys for lower and upper case
letters, and other symbols that would require to *shift* in a normal keyboard,
here you can have them as a key on their own, no *shift*ing needed.

If you want to leave a key unused, make it a `k_empty`, a special key
that does nothing.


## Modifiers

Modifiers like *Control*, *Shift*, *Alt*, *Super* have a `m_` prefix and act
like modifiers in a normal keyboard: you hold it and then press some other key
to *modify* it.

### Pre-modified

Venabili lets you define keys that are already *modified*, for instance this
key:

```c
Lctrl(k_c);
```

Will trigger `Ctrl + c` in a single key press.

### Multifunction modifiers

We can go further still and define keys that will act as a modifier when held,
but be a normal key when pressed and release quickly.

Take for instance the key:

```c
HLctrl(k_escape);
```

Will trigger `escape` when tapped (pressed and released quickly) but will behave
as `Ctrl` when you hold it and press some other key at the same time. This one
is particularly useful.


## Mouse control

There are 5 different mouse buttons prefixed by `m_click_`. The common ones
being:

- 1 = left click
- 2 = right click
- 3 = middle click

In order to move the pointer use the following keys:

- MU(speed): Up
- MD(speed): Down
- MR(speed): Right
- ML(speed): Left
- MWU(speed): Wheel up
- MWD(speed): Wheel down

Where `speed` is number between 0 and 15 to describe how fast the pointer should
move.


## Layers

As described in the [Layers](layers.md) section, the `Layer Selection` key
(`LS(id, key)`) lets you switch to the *id* layer when held or trigger *key*
when tapped.

The `Layer Lock` key (`c_layer_lock`) allows you to lock in the current layer
and release the lock when pressed again.


## Macros

As described in the [Macros](macros.md) section, the `Macro Selection` key
(`MACRO(id)`) lets you trigger the *id* macro.


## Special

If you want to be able to enter *Flash mode* without having to unplug the
keyboard, make sure to include the `c_flash_mode` key in one of your layers.
When pressed the keyboard will enter *Flash mode* and be ready to receive a
firmware update.
