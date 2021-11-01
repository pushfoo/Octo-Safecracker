# Octojam-2021

A code-guessing game for [Octojam 2021](https://itch.io/jam/octojam-8) written
in the [Octo assembly language for Chip-8](https://github.com/JohnEarnest/Octo).

You play a safecracker with 12 chances to guess a 4-digit passcode. Luckily for
you, your tools and flaws in the safe will make it easier.

## How to Play

[A live version can be played on itch.io](https://pushfoo.itch.io/safecracker) with
optional touch or mouse controls. Click or tap the running game to enable the keypad.

### Emulator requirements

If you don't play the web version, this game requires a Chip-8 implementation
that that supports
[XO-Chip v1.0](http://johnearnest.github.io/Octo/docs/XO-ChipSpecification.html)
instructions, such as [Octo](https://github.com/JohnEarnest/Octo).

You can [run Octo in the browser](http://johnearnest.github.io/Octo/) and paste
the code in, or use another emulator with full XO-Chip support such as
[c-octo](https://github.com/JohnEarnest/c-octo) (requires knowledge of how
to build from C source).

### Rules

Your goal is to guess a 4-digit passcode in 12 tries or fewer. Your current guess is
the rightmost column of numbers.

The passcode will not use a digit more than once. If the currently passcode guess
repeats digits, an "X" will be displayed above it, and you won't be able to submit it.
A valid passcode will display "OK" above it. Decreasing or increasing a digit past 0
or 9 will wrap around to the other side. 

After every guess, you will see feedback above it using up to four dots:

- Every dark dot represents a digit in the correct location
- Every light dot represents a digit that is somewhere in the passcode, but currently in the wrong place
- Fewer than four dots means that not all of the digits in your guess are in the passcode
- 0 dots mean that none of the digits you guessed are in the code

After the 12th guess, the game is over, and you win or lose. You can win
earlier than the 12th guess if you deduce the passcode early.

### Controls

Use the following keys to play the game:

| PC Keyboard Key(s) | Chip-8 Keypad Key(s) |  Game Action                                                      |
|--------------------|----------------------|-------------------------------------------------------------------|
| F                  | E                    | Submit current passcode if valid ("OK" above the rightmost column)|
| 1 , 2              | 1 , 2                | Increment/decrement 1st digit                                     |
| Q , E              | 4 , 5                | Increment/decrement 2nd digit                                     |
| A , S              | 7 , 8                | Increment/decrement 3rd digit                                     |
| Z , X              | A , 0                | Increment/decrement 4th digit                                     |

## Additional Info

The font included is based on [Tom Thumb](https://robey.lag.net/2010/01/23/tiny-monospace-font.html),
which is used under
[CC0 Public Domain Dedication](https://creativecommons.org/share-your-work/public-domain/cc0/).

There is no sound at release time.
