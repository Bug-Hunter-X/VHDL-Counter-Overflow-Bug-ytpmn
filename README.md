# VHDL Counter Overflow Bug

This repository demonstrates a common, yet subtle bug in VHDL code: an integer counter that lacks overflow protection.  The `buggy_counter.vhdl` file contains the buggy code. The `fixed_counter.vhdl` file provides a corrected version.

## Bug Description

The original code initializes a counter.  When the counter reaches its maximum value (15), incrementing it would cause an overflow.  This could lead to unexpected behavior, including the counter wrapping around to 0 or producing unpredictable results.  In some synthesis tools this could lead to unintended hardware implementation.

## Solution

The solution involves adding an overflow check within the counter's process.  If the counter reaches its maximum value, it should remain there, preventing further increments until a reset.

## How to Run

This code is intended for simulation or synthesis with a VHDL simulator or synthesis tool. 