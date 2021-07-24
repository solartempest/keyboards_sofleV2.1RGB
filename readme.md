# Sofle Keyboard

![SofleKeyboard version 2.1 RGB Keyhive](https://i.imgur.com/KdNmNCu.jpg)

Sofle is 6×4+5 keys column-staggered split keyboard. Based on Lily58, Corne and Helix keyboards.

More details about the keyboard on my blog: [Let me introduce you SofleKeyboard - a split keyboard based on Lily58 and Crkbd](https://josef-adamcik.cz/electronics/let-me-introduce-you-sofle-keyboard-split-keyboard-based-on-lily58.html)

The current (temporary) build guide and a build log is available here: [SofleKeyboard build log/guide](https://josef-adamcik.cz/electronics/soflekeyboard-build-log-and-build-guide.html)

* Keyboard Maintainer: [Solartempeest)  
* Hardware Supported: SofleKeyboard V2.1 RGB PCB, ProMicro / Elite-C
* Hardware Availability: [PCB & Case Data](https://keyhive.xyz/shop/sofle)

## Flashing

Flash using the correct command below:

```sh
# for pro micro-based builds
qmk flash -kb sofle/rev2 -km keyhive_via -bl avrdude-split-left
qmk flash -kb sofle/rev2 -km keyhive_via -bl avrdude-split-right

# for Elite C or dfu bootloader builds
qmk flash -kb sofle/rev2 -km keyhive_via -bl dfu-split-left
qmk flash -kb sofle/rev2 -km keyhive_via -bl dfu-split-right
```

These commands can be mixed if, for example, you have an Elite C on the left and a pro micro on the right.
Press reset button on he keyboard when asked.

Disconnect the first half, connect the second one and repeat the process.


# VIA keymap for Sofle

Features:

-   Symmetric modifiers (CMD/Super, Alt/Opt, Ctrl, Shift)
-   Modes for Qwerty and Colemak support
-   The OLED on master half shows selected mode and caps lock state and is rotated.
-   Left encoder controls volume up/down/mute. Right encoder PGUP/PGDOWN.
-   Via support
-   RGB underglow support


See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).
