# Octojam-2021

A code-guessing game for [Octojam 2021](https://itch.io/jam/octojam-8) written
in the [Octo assembly language for Chip-8](https://github.com/JohnEarnest/Octo).

## How to Play

### Emulator requirements

This game requires a Chip-8 implementation that that supports
[XO-Chip](http://johnearnest.github.io/Octo/docs/XO-ChipSpecification.html)
instructions, such as [Octo](https://github.com/JohnEarnest/Octo).

You can [run Octo in the browser](http://johnearnest.github.io/Octo/) and paste
the code in, or use another emulator with full XO-Chip support such as
[c-octo](https://github.com/JohnEarnest/c-octo) (requires knowledge of how
to build from C source).

### Rules

Your goal is to guess a four-digit combination to a lock in 12 tries or fewer.
The hidden combination will not use a digit more than once.

After every guess but the 12th, you will see feedback above it using up to four
dots. For every dark dot, your guess has a digit in the correct location. For 
every light dot, your guess has a digit out of place that belongs elsewhere in
the sequence. Less than four dots means that not all of the digits you entered
are in the sequence. No dots at all means that none of the digits you entered
are in the passcode.

After the 12th guess, you will either win, or lose and see the answer revealed
below your guesses.

### Controls

Use the following keys to play the game:

| Keyboard Key(s) | Chip 8 Key(s) |  Action                               |
|-----------------|---------------|---------------------------------------|
| 1 , 2           | 1 , 2         | Increment/decrement 1st number        |
| Q , E           | 4 , 5         | Increment/decrement 2nd number        |
| A , S           | 7 , 8         | Increment/decrement 3rd number        |
| Z , X           | A , 0         | Increment/decrement 4th number        |
| F               | E             | Submit current combination            |
