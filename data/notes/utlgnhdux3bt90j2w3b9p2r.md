
> LTC7800EUDC Demo Circuit 2726A


# Documents

- ![DC2736A Demo Manual](/assets/DC2736A.DemoManual.pdf) ([download](https://www.analog.com/media/en/technical-documentation/user-guides/dc2736af.pdf))
- ![DC2736A Schematics](/assets/DC2736A.Schematics.pdf) ([download](https://www.analog.com/media/en/technical-documentation/eval-board-schematic/DC2736A-2-SCH.PDF))

# Description

- High Frequency Synchronous Buck Converter with GaN Transistors

![](/assets/images/dc2736a.pic.png){max-width: 600px, display: block, margin: 0 auto}

# Data Sheet DC2726A

![](/assets/images/dc2736a.PerformanceSummary.png){max-width: 600px, display: block, margin: 0 auto}

- programmable fixed frequency from 320kHz up to 2.25MHz

- 3 modes
    - forced continuous operation
    - pulse-skipping operation
    - Burst Mode® operation

- **Limitations**
    - Input
        - DC 30V-55V
        - LT 60V max
    - Output
        - DC 12V with 20A

- LTC has two integrated 5V gate drivers with 20ns dead time

- The $EXTV_{CC}$ pin permits the LTC7800 to be powered from the output of
the switching regulator or other available source


![](/assets/images/dc2736a.CardMapping.png){max-width: 600px, display: block, margin: 0 auto}

![](/assets/images/dc2736a.schematic.png){max-width: 800px, display: block, margin: 0 auto}

- INTVCC3 ???

# Quick Start Procedure

Demonstration circuit 2736A is easy to set up to evaluate the performance of the LTC7800. Refer to Figure 1 for the proper measurement equipment setup and follow the procedure below. 

1.   With board not connected, adjust the input power supply to 48V, then turn off the input power supply. Make sure the input power supply is capable of 10A at 30V.

2.   With power off, connect the input power supply to $V_{IN}$ and $GND$ terminal of the board.

3.   Connect the output load between $V_{OUT}$ and $GND$ (Initial load: no load). Refer to Figure 1.

4.   Connect the DVMs to the input and output.

5.   Check the default jumper/switch position: JP7: ON; JP13: CCM.

6.   Turn on the input power supply.
    
    NOTE: The input voltage range for the board is 30V to 55V.

7.   Check for the proper output voltage from $V_{OUT}$ to $GND$. The output voltage should be between 11.76V to 12.24V.

8.   Once the proper output voltage is established, adjust the loads within the operating range (0A to 20A) and observe the output voltage regulation, ripple voltage and other parameters.

9.   After completing all tests, adjust the load to 0A, turn
off the input power supply.

Notes: 
1.   When measuring the output or input voltage ripple, do not use the long ground lead on the oscilloscope probe. See Figure 2 for the proper scope probe technique. Short, stiff leads need to be soldered to the (+) and (–) terminals of an output capacitor. The probe’s ground ring needs to touch the (–) lead and the probe tip needs to touch the (+) lead.
2.   Please set the electronic load in CR (constant resistance) mode for the evaluation of the board. The default setup of the 2736A board is to have $EXTV_{CC}$ pin connected to $V_{OUT}$. Some electronic load outputs negative voltage when doing output overcurrent test of the
board, which exceeds the absolute maximum rating
–0.3V on $EXTV_{CC}$ pin of LTC7800.

External $EXTV_{CC}$ Option 

By default, the $EXTV_{CC}$ pin of LTC7800 on DC2736A board is connected to the output of the converter with R69 (0Ω) for good efficiency and good thermal performance. Please follow the below procedure if an external power supply is used to bias the LTC7800 $EXTV_{CC}$ pin (Do not float this pin). 

1.   Remove R69 on the board. 

2.   Apply a DC voltage (recommend 5.5V – 13V) on $EXTV_{CC}$ and $GND$ turret after the input voltage is established. Make sure $EXTV_{CC} < V_{IN}$.

3.   Turn off the DC bias on the $EXTV_{CC}$ before powering
off the input power supply.

# Measuring Output Voltage

## Method

![](/assets/images/dc2736a.MeasuringOutputVoltage.png){max-width: 300px, display: block, margin: 0 auto}

## Efficiency vs Load Current

![](/assets/images/dc2736a.measure.EfficiencyVsLoad.Vout12vFsw500hz.png){max-width: 300px, display: block, margin: 0 auto}