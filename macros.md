# Macros

Venabili lets you define keys that automatically press multiple keys in sequence
for you (a "macro"). This could be used to perform a sequence of key presses
that you normally do over and over again by hand, or to store commonly used text
strings like passwords, phone number, email addresses, etc.


## Defining macros

Macros are defined in the `venabili.c` file as arrays of keys.

Take a look at this macro that will do `Ctrl + c` and `Ctrl + v` on a single
keystroke:

```c
Macro m1 = { Rctrl(k_c), Rctrl(k_v), k_empty };
```

After you've defined some macros you need to register them with the
`add_macro(name)` function like so:

```c
// Macro m0 = ...
// Macro m1 = ...

add_macro(m0);
add_macro(m1);
```

If you need a macro that only consists of text strings, use the
`add_string_macro` instead:

```c
add_string_macro("email@example.com");
add_string_macro("08764208");
add_string_macro("Some street in some avenue");
add_string_macro("This@is_n0t_a_pa$$word");
```

Each macro you register will acquire an identifier that increments from 0.

Once you're happy with your macros, make sure to set the `N_MACROS` number in
the `config.h` file to match the number of macros you have registered.


## Using macros

In order to trigger macros, use the `MACRO(id)` key in your layers, where *id*
is the number of the macro you want to use.
