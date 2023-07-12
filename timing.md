# removal and recovery time 


the Removal Time, Trem, refers to the minimum time, after the active clock edge, that the reset must be stable before being de-asserted. The reset Removal Check ensures that the de-asserted reset signal is not captured by the same clock edge that launches the reset.

![Uploading removal_recovery.png…]()

Figure . Recovery and Removal Check Timing Diagram (https://www.intel.com/content/www/us/en/docs/programmable/683539/20-4/recovery-and-removal-checks.html)

Reset Recovery Time, Trec, is the minimum time between the de-assertion of a reset and the clock signal being high again. The reset Recovery Check ensures that the reset signal is stable for a minimum time after de-assertion, before the next active clock edge.

总结，对于reset de-assert的clock沿， 
1. to 左边这个沿, reset要保持一段最短时间 T_removal再de-assert
2. to 右边这个沿, reset要在沿之前de-assert并保持稳定一段最短时间T_recovery
