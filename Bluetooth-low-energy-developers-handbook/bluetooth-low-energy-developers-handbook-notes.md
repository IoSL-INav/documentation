# Bluetooth Low Energy notes

## Source
All following quotations are taken from the book "Bluetooth Low Energy - The Developer's Handbook" by Robin Heydon, published with Prentice Hall in 2013. Also not quoted points can be understood as a paraphrasation of read contents of this book.

## What is Bluetooth Low Energy

### Chapter 1
* "Although it uses the Bluetooth brand and borrows a lot of technology from its parent, Bluetooth low energy should be considered a different technology, [...].", p. 3
* Bluetooth transmission speeds across its versions (table 1-1, p. 4):
  * v1.1:   1 MBps
  * v2.0:   3 MBps
  * v3.0:  54 MBps
  * v4.0: 0.3 MBps (Bluetooth low energy)
* Bluetooth low energy does not try to be yet another bandwidth upgrade for Bluetooth but rather a step towards extremly low power consumption as well as being very cheap. This latter directive makes it possible for Bluetooth low energy to be deployed in high volumes.
In order to achieve this, Bluetooth low energy makes use of following 3 design points:
  * ISM band: 2.4 GHz band, over used and bad characteristics as heavily absorbed by water (human body), but no license fees => less costly => "Therefore, choosing to use the ISM band lowers the cost" (p. 5)
  * IP license: basically, the Bluetooth Special Interest Group is claimed to be cheaper than other SIGs. Licenses are given under a FRAND policy which "stands for Fair, Reasonable, and Non-Discriminatory" (p. 5).
  * Low Power: Aiming at low power consumption overall reduces the costs of accompanying services and material costs.
* "[...] because single mode Bluetooth low energy does not support audio for headsets and stereo music or high data rates for file transfers." (p. 6)
* "When the low energy work started, the goal was to create the lowest-power short-range wireless technology possible." (p. 7)
* Initial design goals (p. 7):
  * Worldwide operation => 2.45 GHz band
  * Low cost
  * Robust
  * Short range
  * Low power
* Bluetooth low energy uses adaptive frequency hopping => detects sources of interference, helps to avoid them in the future and quickly recovers from dropped packages. "It is this robustness that is absolutely key to the success of any wireless technology in the most congested radio spectrum available." (p. 8)
* "Short range means that Bluetooth low energy should be a *person area network*" (p. 8)