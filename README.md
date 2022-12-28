# OpenHT
OpenHT - an open-source, SDR handheld transceiver

# Project Plan - Proof of Concept

## Aim of the PoC

Open risks (things we want to buy down quicky): 

* FPGA -> MCU link bandwidth (determine protocol requirements)
* FPGA resource size (determine size requirements)
* RF characterisitics of the AT86RF215 (check for harmonics, real power output, sensitivity, image rejection)
* Overall power consumption
* Zephyr complexity / RTOS choice
* LVGL

## Tests

### RF usablility tests

#### CW test
* transmit a CW signal using the Atmel AT86RF215; vary the power output (by varying the power we get actual AM)
* Should demonstrate signal chain from STM32 -> FPGA -> RF
   
#### FM test
* receive an FM signal and successfully demodulate it
* transmit an FM signal

#### SSB test

* transmit an SSB signal (the last thing to test)

### Platform tests

#### Zephyr bringup
* Should demonstrate use of Zephyr on STM32 Discovery board
* Demonstrate use of SPI and I2S peripherials

#### LVGL test
* Demonstrate use of LVGL on the STM32 Discovery board
* Demonstrate LVGL running on Zephyr

## Hardware required for the PoC
* LIFCL-40-EVM FPGA eval board
* AT86RF215 RF eval board + an SMA antenna
* a breakout board for RF-FPGA interconnection (with SATA cables)
* STM32F469I-DISCO board (for the display and mic/spk - an interface)
* a small speaker
* a bunch of interconnection wires

## Software used
* Zephyr
* Lattice Radiant (https://www.latticesemi.com/latticeradiant)

## Sub Repos
firmware --> https://github.com/M17-Project/OpenHT-firmware 
