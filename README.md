# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL: an unsigned counter without overflow protection.  The `counter.vhdl` file contains a simple 4-bit counter. When the counter reaches its maximum value ("1111"), incrementing it results in overflow.  The solution (`bugSolution.vhdl`) demonstrates how to correctly handle this situation.

## Bug

The provided VHDL code implements a counter that increments on every rising clock edge.  However, it doesn't handle the case where the counter reaches its maximum value. Incrementing beyond the maximum value results in an unexpected wrap-around to 0, leading to incorrect behavior in some applications. This is a classic unsigned integer overflow.

## Solution

The solution involves adding a check to detect when the counter reaches its maximum value and handling it appropriately. This might involve stopping the count, resetting it, or triggering an overflow flag.
