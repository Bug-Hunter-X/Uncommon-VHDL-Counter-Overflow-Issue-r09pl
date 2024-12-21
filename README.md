# Uncommon VHDL Counter Overflow Issue

This repository demonstrates a subtle bug in a VHDL counter implementation.  The counter is designed to count from 0 to 15 and then reset. However, there is a potential issue related to how the counter handles the transition from 15 back to 0.  The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description

The primary issue lies in the way the counter handles the rollover from 15 to 0.  While functionally it appears correct, there might be unintended behavior in some synthesis tools or when dealing with specific timing scenarios.  The solution presented is more robust and prevents potential issues.

## Solution

The solution uses a more robust way of handling the counter reset, ensuring a cleaner transition and potentially better synthesizability. Refer to `fixed_counter.vhdl` for details.