# D-pad ASCII input

## Overview

Specification and implementation of ASCII character input with a cross key on a gamepad.

## Motivation, purpose, characteristics

* Can be input on devices with few input keys
* You can enter all ASCII alphanumeric symbols
* Simple specifications
* Simple to implement
* You can enter at a practical speed
* You can enter without looking at the screen
* If you look at the screen, you can enter without remembering
* Input specifications are regular and easy to learn

## Specification

* Enter the four-way controller four times, combine each 2 bits into 1 byte, and enter it as an ASCII character code.
* ↑, ←, →, ↓ become 0, 1, 2, 3 respectively
* When you press that key, the remaining candidate characters will be displayed on the screen.
* If there is a bit in the middle of input, you can cancel by 2 bits in Backspace

## An example

```
Hello World
```

| Character | Input |
|---|---|
| H | ←↑→↑ |
| e | ←→←← |
| l | ←→↓↑ |
| l | ←→↓↑ |
| o | ←→↓↓ |
| Space | ↑→↑↑ |
| W | ←←←↓ |
| o | ←→↓↓ |
| r | ←↓↑→ |
| l | ←→↓↑ |
| d | ←→←↑ |

## Working demo

A demo that runs on the Web. (Check operation on Windows, Chrome84, Firefox79, XBox360 Controller) On the
keyboard, the arrow keys correspond to the cross keys and the Backspace key corresponds to the Backspace.
Also compatible with gamepads using the Gamepad API.
0-axis, 1-axis, 12-15 buttons correspond to the cross key, 0 button corresponds to Backspace.
Can measure WPM and CPM.

* https://htsnul.github.io/dpad_ascii_input/

## Input technique

You can enter faster if you enter as follows.

| Character | Input | Modified input |
| --- | --- | --- |
| a | ←→↑← | ←→↗↑↖ |
| b | ←→↑→ | ←→↑↗ |
| t | ←↓←↑ | ←↓↙←↖ |
| x | ←↓→↑ | ←↙↓↘→↗ |

## How fast can you get?

After doing 30 minutes of practice in 3 sessions,
I started to reach about 15 WPM.
(Situation where it gets stuck in places or makes a mistake)
The average average typing speed is 38-40 WPM.

So, in the end, it is expected that the performance will be about half that of general average typing.

## List

| Caracter | Input |
|---|---|
| Tab | ↑↑→← |
| Enter | ↑↑→→ |
| Space | ↑→↑↑ |
| ! | ↑→↑← |
| " | ↑→↑→ |
| # | ↑→↑↓ |
| $ | ↑→←↑ |
| % | ↑→←← |
| & | ↑→←← |
| ' | ↑→←↓ |
| ( | ↑→→↑ |
| ) | ↑→→← |
| * | ↑→→→ |
| + | ↑→→↓ |
| , | ↑→↓↑ |
| - | ↑→↓← |
| . | ↑→↓→ |
| / | ↑→↓↓ |
| 0 | ↑↓↑↑ |
| 1 | ↑↓↑← |
| 2 | ↑↓↑→ |
| 3 | ↑↓↑↓ |
| 4 | ↑↓←↑ |
| 5 | ↑↓←← |
| 6 | ↑↓←→ |
| 7 | ↑↓←↓ |
| 8 | ↑↓→↑ |
| 9 | ↑↓→← |
| : | ↑↓→→ |
| ; | ↑↓→↓ |
| < | ↑↓↓↑ |
| = | ↑↓↓← |
| > | ↑↓↓→ |
| ? | ↑↓↓↓ |
| @ | ←↑↑↑ |
| A | ←↑↑← |
| B | ←↑↑→ |
| C | ←↑↑↓ |
| D | ←↑←↑ |
| E | ←↑←← |
| F | ←↑←→ |
| G | ←↑←↓ |
| H | ←↑→↑ |
| I | ←↑→← |
| J | ←↑→→ |
| K | ←↑→↓ |
| L | ←↑↓↑ |
| M | ←↑↓← |
| N | ←↑↓→ |
| O | ←↑↓↓ |
| P | ←←↑↑ |
| Q | ←←↑← |
| R | ←←↑→ |
| S | ←←↑↓ |
| T | ←←←↑ |
| U | ←←←← |
| V | ←←←→ |
| W | ←←←↓ |
| X | ←←→↑ |
| Y | ←←→← |
| Z | ←←→→ |
| [ | ←←→↓ |
| \ | ←←↓↑ |
| ] | ←←↓← |
| ^ | ←←↓→ |
| _ | ←←↓↓ |
| ` | ←→↑↑ |
| a | ←→↑← |
| b | ←→↑→ |
| c | ←→↑↓ |
| d | ←→←↑ |
| e | ←→←← |
| f | ←→←→ |
| g | ←→←↓ |
| h | ←→→↑ |
| i | ←→→← |
| j | ←→→→ |
| k | ←→→↓ |
| l | ←→↓↑ |
| m | ←→↓← |
| n | ←→↓→ |
| o | ←→↓↓ |
| p | ←↓↑↑ |
| q | ←↓↑← |
| r | ←↓↑→ |
| s | ←↓↑↓ |
| t | ←↓←↑ |
| u | ←↓←← |
| v | ←↓←→ |
| w | ←↓←↓ |
| x | ←↓→↑ |
| y | ←↓→← |
| z | ←↓→→ |
| { | ←↓→↓ |
| Vertical bar | ←↓↓↑ |
| } | ←↓↓← |
| ^ | ←↓↓→ |


