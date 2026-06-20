# The Base-50 Shifting Scale (BSS) Squaring Algorithm

## Overview
The **Base-50 Shifting Scale (BSS) Algorithm** is an original mental arithmetic framework designed and engineered by **Rahul Devanand Boudh (RDB)**. 

Unlike traditional mental math shortcuts that calculate values from left-to-right or rely on static magic numbers (like 25), the BSS algorithm maps out a dynamic coordinate axis centered at 50. It computes digits strictly from **right-to-left** (Units → Tens → Hundreds → Thousands), gracefully handling both positive and negative carries.

## The Shifting Scale Matrix
The system assigns an integer scale multiplier ($S$) to entire decades based on their relative distance from the 50-series anchor:

| Decade Series | Tens Digit ($T$) | Scale Factor ($S = T - 5$) |
| :--- | :---: | :---: |
| 20 Series | 2 | -3 |
| 30 Series | 3 | -2 |
| 40 Series | 4 | -1 |
| **50 Series (Anchor)** | **5** | **0** |
| 60 Series | 6 | +1 |
| 70 Series | 7 | +2 |
| 80 Series | 8 | +3 |
| 90 Series | 9 | +4 |

## Positional Execution Steps
For any two-digit number expressed as $TU$:
1. **Units Place:** Compute $U^2$. Write down the unit digit, carry the rest to the Tens column.
2. **Tens Place:** Compute $(U \times S) + (U \times S) = 2US$. Add any incoming units-stage carry. Note the final single digit (accounting for negative modulo wraps) and carry the remainder leftward.
3. **Left Positions (Hundreds/Thousands):** Compute the base consecutive product $T \times (T + 1)$, add the internal difference component $(U - T)$, and apply the remaining carry from the tens stage.

## Author & Attribution
This algorithm was independently formulated, documented, and verified as a unique mental framework by **Rahul Devanand Boudh**. Feel free to use, test, or implement this algorithm in your software projects—please maintain attribution to the author.
