---
title: Embedded Calculator
description: A simple calculator that allows users to add, subtract, multiply, and divide numbers.
date: 2020-02-01 00:00:00 -0600
image:
  path: /assets/img/posts/2020-02-01-embedded-calculator/embedded-calculator.jpg
tags: [hardware, firmware]
---

### Problem Statement

Create a simple 2-operand embedded calculator that allows users to add, subtract, multiply, or divide any two 32-bit integers by utilizing the external switch-matrix keypad as an input device and the external LCD module as an output device.

### Implementation

To begin, I decided I wanted to replicate the normal use-case of a simple household calculator. I also wanted to implement some additional features not required by the problem statement such as overflow/underflow protection, divide-by-zero protection, a clear button, and (my favorite extra feature) calculation chaining.

Before I could begin writing the calculator application, I had to develop drivers to interface with the LCD and keypad. I developed these in C using the LCD's asynchronous parallel communication interface and an interrupt-driven scanning routine with the keypad. The completed drivers are included in the project's GitHub repository.

With the drivers constructed, I began implementing my calculator application. As the user enters information on the keypad, the calculator constructs a C-style string (the "op string") in the form [operand1][operator][operand2]['\0'].

When the user presses the equals key, the system parses the op string and runs operands through the appropriate operation. If the result of the calculation involves dividing by zero, overflows, or underflows, it will default to zero. Otherwise, the result will be calculated, printed to the LCD, and automatically re-inserted into the op string as the first operand for the next calculation.

### Demo Video

{% include embed/youtube.html id='c5m5CCOlb9k' %}

### Future Improvements

As with all of my projects, there are a number of improvements that could be made. I've listed the most prominent ones below.

- Use 64-bit integers for calculations instead of 32-bit integers
- Display error messages for overflow/underflow/divide-by-zero errors instead of defaulting to 0
- Enable the microcontroller's FPU and use floating point arithmetic instead of integer arithmetic
- Allow the user to enter numbers up to 14 digits instead of limiting them at 9 digits