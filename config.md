# Configuration

The `config.h` file lets you specify how many layers and macros are you using:

- N_LAYERS
- N_MACROS

But there are some other things you can change to tweak the behaviour of the
keyboard:

- MAX_MACRO_LENGTH: Maximum length for macros (in characters)
- TAP_TIMEOUT_MS: How many milliseconds a double-function key should be held
  before assuming you don't want it to do anything.
- LAYER_DROPPING_TIMEOUT_MS: How many milliseconds to wait after a layer drop
  before start accepting new keys to avoid unintentional pressing of default
  layer keys.
- ENABLE_DOUBLE_SHIFT_CAPS_LOCK: Pressing both left and right shift keys at the
  same time toggles *Caps Lock*.
