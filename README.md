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

# Design specifications:
PARAMETERS with VALUES
1)Technology-28nm
2)Power supply +/_400mv
3)Output swing "-400mv to +400mv"
4)Open loop gain       40dB
# Diagrams and Waveforms of Two Stage Op-Amp

# Reference Circuit:
![Screenshot 2022-03-01 130348](https://user-images.githubusercontent.com/100671397/156124970-3b0d781c-a16c-45cb-b5d2-4da8e537345a.png)

# Schematic Diagram of Two Stage of Operational amplifier
![Screenshot (149)](https://user-images.githubusercontent.com/100671397/156124432-b346a13c-d179-4d06-926a-859c3b2a4390.png)

# Transient Response of Two Stage Op-Amp
![Screenshot (144)](https://user-images.githubusercontent.com/100671397/156125411-2da8ffc1-f417-4f82-bea2-f989e75e4aac.png)

# Ac analysis with gain and gain bandwidth
![Screenshot (145)](https://user-images.githubusercontent.com/100671397/156125899-7e5b5b0a-fcca-417e-a82f-2161c3343778.png)


# Netlist of Op-Amp
<br /> *  Generated for: PrimeSim
*  Design library name: cp.opamp
*  Design cell name: cp.op
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Tue Mar  1 07:41:39 2022

.global gnd!
********************************************************************************
* Library          : cp.opamp
* Cell             : cp.op
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
<br /> xm26 vout net114 net75 net75 p105 w=10.5u l=30n nf=5 m=2
<br /> xm1 net114 net9 net75 net75 p105 w=9.5u l=0.03u nf=4 m=2
<br /> xm0 net75 net9 net9 net75 p105 w=8u l=30n nf=4 m=2
<br /> xm6 vout net110 gnd! gnd! n105 w=10.5u l=0.03u nf=3 m=2
<br /> xm5 gnd! net110 net110 gnd! n105 w=4u l=0.03u nf=4 m=2
<br /> xm4 net111 net110 gnd! gnd! n105 w=6u l=0.03u nf=4 m=2
<br /> xm3 net111 b net114 gnd! n105 w=10.101u l=0.03u nf=3 m=2
<br /> xm2 net9 a net111 gnd! n105 w=10.101u l=0.03u nf=3 m=2
<br /> v8 net75 gnd! dc=1
<br /> i14 net75 net110 dc=30u
<br /> c24 net114 vout c=10p
<br /> c25 vout gnd! c=10p
<br /> v22 a gnd! dc=50m ac=1 sin ( 0 10m 1k 0 0 0 )
<br /> v37 gnd! b dc=50m ac=1 sin ( 0 5m 1k 0 0 0 )

<br /> .tran '0.001*(50m-0)' '50m' name=tran
<br /> .ac dec '10' '0' '1meg' name=ac
<br /> .dcOP

<br /> .option primesim_remove_probe_prefix = 0
<br /> .probe v(*) i(*) level=1
<br /> .probe tran v(a) v(b) v(vout)

<br /> .temp 25

<br /> .option primesim_output=wdf

<br /> .option parhier = LOCAL

<br /> .end





