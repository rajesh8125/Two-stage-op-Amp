# Two-stage-op-Amp

# Abstract:
An Operational amplifier is consider to 
be the most imperative electronic device. The 
procedure in this paper is to design a two stage 
CMOS operational amplifier and analyze the effect 
of various parameters on the characteristics of Op-amp design. This work presents a design and 
implementation of two stage CMOS operational 
amplifier which operates at ±400mv supply voltage 
and Simulation process is carried out by using an 
EDA tool Synopsys with 28nm technology. The 
obtained gain is 84dB. with phase margin of 560
and the power dissipation is of 38.02μW.

# Circuit details:
Op-amps are the most commonly used devices in 
electronic circuits. The differential amplifier has two 
different voltage inputs vin+ and vin- which 
amplifies the differences between two input 
voltages. Since the gain obtained from the first stage 
is not sufficient, it uses common source amplifier at 
second stage. Thus, the output of this differential 
amplifier continues to enter the common source 
amplifier where further more gain is increased. In 
order to obtain low gain at high frequencies and 
maintain the device’ stability, it includes 
compensation circuit whenever the device is in 
negative feedback condition.

Design specifications:
PARAMETERS           VALUES
Technology             28nm
Power supply          +/_400mv
Output swing        -400mv to +400mv
Open loop gain       >80dB
Phase margin           600
Power dissipation     <40uW
