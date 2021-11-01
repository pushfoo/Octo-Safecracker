# Octojam-2021

A code-guessing game for [Octojam 2021](https://itch.io/jam/octojam-8) written
in the [Octo assembly language for Chip-8](https://github.com/JohnEarnest/Octo).

You play a safecracker with 12 chances to guess a 4-digit passcode. Luckily for
you, your tools give you some information about how correct each guess is.

See the Rules section for more information about how to play.

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

Your goal is to guess a 4-digit passcode in 12 tries or fewer. 

Each digit in the code is unique. The hidden passcode will not use a digit
more than once.

Your tools will help you. If you try to enter a passcode that repeats digits,
your tools will display an X and stop you from wasting an attempt. They will
display "OK" above any passcode that can be submitted. Be careful, because
your tools will not stop you from repeating a passcode that you have already
tried.

After every guess, you will see feedback above it using up to four
dots:

- Every dark dot represents a digit you guessed in the correct location
- Every light dot represents a digit you guessed that is in the passcode, but in the wrong place
- Fewer than four dots means that not all of the digits you entered are in the passcode
- 0 dots means that none of the digits you entered are in the passcode

After the 12th guess, the game is over, and you win or lose. You can win
earlier than the 12th guess if you deduce the passcode early.

### Controls

Use the following keys to play the game:

| Keyboard Key(s) | Chip 8 Key(s) |  Action                                                           |
|-----------------|---------------|-------------------------------------------------------------------|
| F               | E             | Submit current passcode if valid ("OK" above the passcode)        |
| 1 , 2           | 1 , 2         | Increment/decrement 1st number                                    |
| Q , E           | 4 , 5         | Increment/decrement 2nd number                                    |
| A , S           | 7 , 8         | Increment/decrement 3rd number                                    |
| Z , X           | A , 0         | Increment/decrement 4th number                                    |
