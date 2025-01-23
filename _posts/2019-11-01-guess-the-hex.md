---
title: "Guess the Hex!"
description: A fun Bop-It type game where you translate binary nibbles to hex!
date: 2019-11-01 00:00:00 +0600
image:
  path: /assets/img/posts/2019-11-01-guess-the-hex/guess-the-hex.jpg
---

### The Problem

The ability to convert binary numbers to hexadecimal is *indispensable* for computer engineers. Unfortunately, this skill takes a long time to develop and requires hours of practice to perfect. There needs to be a faster and more entertaining way!

### The Plan

Implement a fast-paced binary to hexadecimal conversion game that starts slow and gets faster over time. Use ARM Assembly, an STM32 microcontroller, and embedded systems software development techniques to implement the application.

The "Guess the Hex!" game should accomplish the following goals:

1. Display a startup screen on the LCD and wait for the user to press a key
2. Provide a countdown before the round starts
3. Display a binary number on the LCD and await keypad input
4. After every 10 conversions, notify the user they're on a streak and increase the pace of the game
5. End the round if the user makes an improper conversion or takes too long to respond
6. Keep track of the users score, fastest response time, and average response time and display them when the round is over
7. Provide audio feedback for prompts and button presses
8. Make some cute jingles that play at different phases of the game (e.g. startup, game start, speeding up)

### The Result

As nerdy as it might be, Guess the Hex wound up being a super intense and very competitive game. During my lab, many fellow students wound up challenging each other to competitions, attempting to set the new high score.

I wound up setting the all-time high score of 77 correct conversions before running out of time. This record has yet to be beaten.

### The Future

Given its popularity in my class and its entertaining nature, I'm pretty satisfied with the final state of Guess the Hex. This makes it hard to pick out potential improvements, but I've still listed a few below.

- Provide dynamically formatted feedback about response times instead of defaulting to milliseconds for everything
- Create some sort of interrupt driven background music that runs at the tempo of the game
- Automatically keep track of the high score on the system