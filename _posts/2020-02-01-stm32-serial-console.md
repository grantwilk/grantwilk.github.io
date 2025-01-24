---
title: STM32 Serial Console
description: A serial console for STM32 MCUs with a set of basic commands for troubleshooting.
date: 2020-02-01 00:00:00 -0600
image:
  path: /assets/img/posts/2020-02-01-stm32-serial-console/stm32-serial-console.jpg
---

Although ST offers an impressive set of bare-metal debugging tools for their microcontrollers, they are not fit for running diagnostics or being managed in the field. There needs to be a more user-friendly high-level debugging tool.

### The Plan

Use C to implement a ring-buffered UART and an interrupt driven console application for the STM32 microcontroller.

The UART driver should accomplish the following goals:

1. Effectively transmit data via the UART protocol
2. Utilize a ring buffer to buffer incoming and outgoing packets
3. Allow programmers to set a custom Baud rate
4. Integrate seamlessly with the `printf()` and `scanf()` functions

Likewise, the console application should accomplish the following goals:

1. Accept a command and multiple arguments from the UART's input buffer
2. Parse the command and extract all arguments
3. Run the proper functionality based on the value of the command
4. Catch invalid commands/arguments and print useful information to the UART's output buffer to help the user determine what they did wrong

### The Result

The basic implementation of my console application allowed users to read from, write to, and dump memory from the microcontroller via my ring-buffered UART driver. It accepts and successfully parses commands from the user and responds accordingly. Additionally, if the command or arguments are invalid, the system will print out a basic error dialog suggesting what the user may have done incorrectly.

In addition to the UART driver and console application, I also wound up implementing a set of functions with functionality similar to Java's `Scanner` class for parsing data from the user's input. Out of everything in this project, this wound up being the most difficult task by far. To say the least, I spent a little more time working with C-style strings than I ever expected to ... but boy, do I have a confident understanding of them now!

### The Future

I don't plan on returning to this project in the future, but I do plan on re-using and re-purposing the code in future embedded projects. I can add custom commands and functionality for each project, so my embedded devices can be easily diagnosed or otherwise managed in the field.

The potential applications are unlimited!