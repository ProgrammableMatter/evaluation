Measurements
============

Clock Skew Synchronization
--------------------------

| Result | Setup | Description | 
|--------|-------|-------------|
| <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-20sec-0.png" width=100 /> <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-20sec-1.png" width=100 /> <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-20sec-2.png" width=100 /> <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-20sec-3.png" width=100 /> <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-20sec-4.png" width=100 /> | soft1, cap1, osc2, net1, mcu1, func[1-4]-1, proAn[1-4]-1 | fifo 4, mean | 
| <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order2-20sec-0.png" width=100 /> | soft1, cap1, osc2, net2, mcu1, func[1-4]-1, proAn[1-4]-1 | fifo 4, mean |

| <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c0-order1-5sec-0.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c0-order1-5sec-1.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c0-order1-5sec-2.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c0-order1-5sec-3.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c0-order1-5sec-4.png" width=100 /> | soft1 cap0, osc1 net1, mcu1, func[1-4]-1, proAn[1-4]-1 | fifo 4, mean |
| <img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-5sec-0.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-5sec-1.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-5sec-2.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-5sec-3.png" width=100 />
<img src="./results/clock-skew-synchronization/sync-clock-skew-fifo4-mean-pitch16-c560-each2nd-particle-order1-5sec-4.png" width=100 /> | | soft1 cap0, osc2 net1, mcu1, func[1-4]-1, proAn[1-4]-1 | fifo 4, mean | 


Setup Configurations
====================

Particle Speed (internal RC osc.)
---------------------------------

| Particle ID | Approx. Frequency [MHz]|
|-------------|--------------------|
| 1  | 8.178 |
| 2  | 8.180 |
| 3  | 8.191 |
| 4  | 8.211 |
| 5  | 8.241 |
| 6  | 8.254 |
| 7  | 8.279 |
| 8  | 8.284 |
| 9  | 8.386 |
| 10 | 8.303 |
| 11 | 8.355 |
| 12 | 8.382 |

* Measurements taken with particles having room temperature.
* Measured after powered 30sec. 
* Averaged 5sec (~7000 samples).
* Measurements could be reproduced in a 2nd run.
* Frequency is voltage dependent; values are understood to be "relative".
* Vcc approx. 5v, see power supply of setup mcu1.

Order Setup in Measurements
---------------------------

Setup ID | Network Dimension | Order P.ID | Address | Details |
|--------|-------------------|-------|--------------|---------|
| net1   | (12x1) | {6, 3, 9, 1, 7, 4, 11, 2, 10, 5, 12} | {(1,1), (2,1), (3,1), (4,1), (5,1), (6,1), (7,1), (8,1), (9,1), (10,1), (11,1), (12,1)} | order having good discrepancy in between subsequent particles's frequency |
| net2   | (12x1) | {6, 2, 10, 1, 8, 4, 12, 3, 9, 7, 11, 6, 5} | {(1,1), (2,1), (3,1), (4,1), (5,1), (6,1), (7,1), (8,1), (9,1), (10,1), (11,1), (12,1)} | same as 1 but less discrepancy |


Oscilloscope Measurement Notes
------------------------------

| Setup ID | Capture Duration [s] | [MSa/s] | Pre-Trigger [s] |  Details |
|----------|----------------------|---------|-----------------|----------|
| osc1        | 2.8 - 7.8            | 5       | 5              | cap1   |
| osc2        | 2 - 22               | 5       | 10.7           | cap1   |              

| Function Config ID | Function Name | Action | Input Data | Color |
|--------------------|---------------|--------|------------|-------|
| func1-1            | f1            | trend  | Analogue 1 | beige |
| func2-1            | f2            | trend  | Analogue 2 | green |
| func3-1            | f3            | trend  | Analogue 3 | blue  |
| func4-1            | f4            | trend  | Analogue 4 | purple | 

| Connection ID | Probe | Input Data | Notes |
|---------------|-------|------------|-------|
| proAn1-1 | Analogue 1 | Internal Time Tracking ISR: Particle 1  | |
| proAn2-1 | Analogue 2 | Internal Time Tracking ISR: Particle 4  | |
| proAn3-1 | Analogue 3 | Internal Time Tracking ISR: Particle 7  | |
| proAn4-1 | Analogue 4 | Internal Time Tracking ISR: Particle 12 | |

Capacitor Configurations
------------------------

| Setup ID | Caps [µF] | Configuration |
|----------|-----------|---------------|
| cap0     | -         | no additional caps |
| cap1     | 560       | each 2nd particle  |

Software Configuration
----------------------

| Setup ID | Averaging Method | outlier rejection | FiFo Size [Elements] | Pitch |
|----------|------------------|-------------------|----------------------|-------| 
| soft1    | mean             | -                 | 4                    | 16    |


Mircocontroller Configuration
-----------------------------

| Configuration ID | Details | Fuses | Power Supply |
|------------------|---------|-------|--------------|
| mcu1             | internal RC 8MHz, clk out | ```FUSES = { .low =  (FUSE_SUT_CKSEL0 & FUSE_SUT_CKSEL2 & FUSE_SUT_CKSEL3 & FUSE_SUT_CKSEL4 & FUSE_CKOUT), .high = HFUSE_DEFAULT, .extended = EFUSE_DEFAULT,};``` | Anker, USB, max. 5V/3A |
