---
title: ARM v4 Microarchitecture
description: An FPGA implementation of the ARM v4 ISA using VHDL.
date: 2019-05-01 00:00:00 -0600
image:
  path: /assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-execute.jpg
tags: [hardware, fpga]
---

### The Problem

Modern computing tasks require a massive amount of computation power packed into a small device. Implement a single-cycle microarchitecture based around the ARMv4 ISA that can be successfully emulated on an Intel™ MAX® 10 FPGA.

### The Plan

Use VHDL to implement all base components including the register file, the ALU, the barrel shifter, and the instruction ROM. Then, use Quartus Prime's schematic editor to implement the processors stages and system architecture.

The microprocessor should accomplish the following goals:

- Execute one instruction per clock-period (single-cycle)
- Successfully execute instructions of the following types:
  - Data Processing (ADD, SUB, MOV, LSL, ROR, etc.)
  - Adv. Data Processing (MUL, DIV, etc.)
  - Memory Access (LDR, STR, etc.)
  - Conditional/Unconditional Branch (B, BEQ, BNE, etc.)
- Successfully execute a simple counting program in simulation
- Successfully execute a simple calculator program in simulation
- Successfully execute a simple calculator program when emulated on an Intel™ MAX® 10 FPGA using memory mapped switches, 7-seg displays, and LEDs as a user interface

![](/assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-uarch.jpg)
_The top-level microarchitecture of my ARM v4 CPU._

### The Result

After spending months of my spring term implementing the stages, components, and logic of the microarchitecture, I finally ran my first successful simulation in early May. In later weeks, I would revisit the project, implement more features, and develop a simple system-level architecture for testing.

By the end, the system was running on an FPGA and was fully capable of running a simple calculator program that I wrote and assembled in ARM Assembly.

I am immensely proud of this project for a few reasons.

1. I just built my own microprocessor (seriously, how cool is that?!)
2. I was able to implement my designs from a industry-standard ISA
3. I finally understood how a computer works from the ground up -- a question that has perplexed me since I was 7 or 8 years old

I really hope I can do more projects like this in the future.

![](/assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-fetch.jpg)
_The FETCH stage._

![](/assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-decode.jpg)
_The DECODE stage._

![](/assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-execute.jpg)
_The EXECUTE stage._

![](/assets/img/posts/2019-05-01-arm-v4-microarchitecture/arm-v4-system.jpg)
_The system/board level integration._