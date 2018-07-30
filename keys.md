# Keys

These are the available keys at your disposal for defining layers in the
`venabili.c` file.


## Layers control keys

Layer `n = 0` is the first (main) layer.

- LS(n): Select `n`th layer (0 <= n < 256)
- c_layer_lock
- c_flash_mode



## Mouse control keys

### Movement

Valid `speed`s are numbers between `0` and `15`

- MU(speed): Up
- MD(speed): Down
- MR(speed): Right
- ML(speed): Left
- MWU(speed): Wheel up
- MWD(speed): Wheel down

### Clicks

- m_click_1
- m_click_2
- m_click_3
- m_click_4
- m_click_5



## Macro keys

- MACRO(id): select `id` macro (0 <= id < 26)


## Modifiers

### Apply modifiers to a key

e.g.   Rctrl(Lshift(k_a)) = CTRL + SHIFT + a

- Lctrl(key)
- Lshift(key)
- Lalt(key)
- Lsuper(key)
- Key Rctrl(key)
- Key Rshift(key)
- Key Ralt(key)
- Key Rsuper(key)



### Make a key behave like a modifier when held

e.g.  HRshift(k_a) = 'a' when tapped, RShift when held

- HLctrl(key)
- HLshift(key)
- HLalt(key)
- HLsuper(key)
- Key HRctrl(key)
- Key HRshift(key)
- Key HRalt(key)
- Key HRsuper(key)



## Normal keys

### Empty key

A key that does nothing

- k_empty


### Letters

#### Lower case

- k_a
- k_b
- k_c
- k_d
- k_e
- k_f
- k_g
- k_h
- k_i
- k_j
- k_k
- k_l
- k_m
- k_n
- k_o
- k_p
- k_q
- k_r
- k_s
- k_t
- k_u
- k_v
- k_w
- k_x
- k_y
- k_z

#### Upper case

- k_A
- k_B
- k_C
- k_D
- k_E
- k_F
- k_G
- k_H
- k_I
- k_J
- k_K
- k_L
- k_M
- k_N
- k_O
- k_P
- k_Q
- k_R
- k_S
- k_T
- k_U
- k_V
- k_W
- k_X
- k_Y
- k_Z


### Numbers

- k_0
- k_1
- k_2
- k_3
- k_4
- k_5
- k_6
- k_7
- k_8
- k_9


### Symbols

- k_back_quote
- k_double_quote
- k_single_quote
- k_tilde
- k_bang
- k_at
- k_hash
- k_dollar
- k_percent
- k_caret
- k_ampersand
- k_asterisk
- k_hyphen
- k_under_score
- k_equal
- k_plus
- k_semicolon
- k_colon
- k_dot
- k_comma
- k_slash
- k_question_mark
- k_backslash
- k_pipe
- k_greater_than
- k_less_than
- k_open_paren
- k_close_paren
- k_open_bracket
- k_close_bracket
- k_open_brace
- k_close_brace


### Modifiers

These only send a key press of a modifier key, but will not actually *modify*
any Key.

- m_lctrl
- m_lshift
- m_lalt
- m_lsuper
- m_rctrl
- m_rshift
- m_ralt
- m_rsuper



### Non-printables

- k_print_screen
- k_scroll_lock
- k_pause
- k_insert
- k_delete
- k_home
- k_end
- k_pageup
- k_pagedown
- k_arrow_up
- k_arrow_down
- k_arrow_left
- k_arrow_right
- k_menu
- k_select
- K_stop
- k_enter
- k_escape
- k_backspace
- k_tab
- k_space
- k_caps
- k_undo
- k_cut
- k_copy
- k_paste
- k_find
- k_mute
- k_vol_up
- k_vol_down
- k_again
- k_f1
- k_f2
- k_f3
- k_f4
- k_f5
- k_f6
- k_f7
- k_f8
- k_f9
- k_f10
- k_f11
- k_f12
- k_f13
- k_f14
- k_f15
- k_f16
- k_f17
- k_f18
- k_f19
- k_f20
- k_f21
- k_f22
- k_f23
- k_f24
