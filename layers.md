# Layers

Venabili uses a nested layers mechanism to not only give you access to all the
keys that you might need, but also to distribute them in a way that is the most
comfortable and fast to reach, even if means duplicating keys just to have them
in different places for different situations.


## Declaring layers

Layers are declared in the `venabili.c` file as 4x12 matrices of keys that match
the position of the physical switches.

Take a look at the default layer:

```c
Layer l0 =
{
    { k_tab, k_q, k_w, k_e, k_r, k_t, k_y, k_u, k_i, k_o, k_p, k_hyphen},
    { HLctrl(k_escape), k_a, k_s, k_d, k_f, k_g, k_h, k_j, k_k, k_l, k_semicolon, HRctrl(k_enter)},
    { m_lshift, k_z, k_x, k_c, k_v, k_b, k_n, k_m, k_comma, k_dot, k_slash, m_rshift},
    { m_lsuper, m_lalt, m_ralt, LS(3, k_empty), LS(2, k_empty), LS(1, k_space), k_space, LS(2, k_empty), LS(4, k_empty), m_ralt, m_lalt, m_rsuper},
};
```

Each row is inside braces `{}` and each key is separated by a comma `,`, these
are just normal *C* arrays.

After you've defined some layers you need to register them with the
`add_layer(name)` function like so:

```c
// Layer l0 = ...
// Layer l1 = ...
// Layer numbers = ...
// Layer symbols = ...

add_layer(l0);
add_layer(l1);
add_layer(numbers);
add_layer(symbols);
```

Each layer you register will acquire an identifier that increments from 0.

Once you're happy with your layers, make sure to set the `N_LAYERS` number in
the `config.h` file to match the number of layers you have registered.


## Switching between layers

To allow you to switch between layers you need to include `Layer Selection` keys
`LS(id, key)`, where *id* is the layer number that key will take you to and
*key* is the normal key to be triggered if you press and release the key without
using any of the keys *inside* that layer. A great example of this is:

```c
LS(1, k_space)
```

This key will put a space if you press it and release it quickly, but will let
you access layer number 1 (that is the second layer) if you hold it and press
some other key at the same time.


### Locking

When you enter a layer by holding its `Layer Selection` key, you will go back to
the default layer (the very first layer that you declared) as soon as you
release it. There are however some use case scenarios where you might want to
stay in a layer without having to hold any key.

For instance, this is useful if you define a layer that has hotkeys for some
sort of editing software or video game in the left half  of the keyboard,
allowing you to use any keyboard shortcut you might need while holding the mouse
with your right hand.

You can achieve this by having a `Layer Lock` key *inside* the target layer:

```c
Layer l1 =
{
    { c_layer_lock, ... },
    // ...
};
```

This way if you hold your `LS(1, k_space)` key in layer 0 and then press the
your `c_layer_lock` key that is inside layer 1 the keyboard will stay in layer 1
when you release all the keys.

Now you can use any other key you have in layer 1 without having to keep holding
some other key at the same time.

To release the lock just press your `Layer Lock` key once again and you'll be
back to the default layer.
