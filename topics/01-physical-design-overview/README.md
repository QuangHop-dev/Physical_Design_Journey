# Topic 01 — Physical Design Overview

## Agenda

| Order | Content | Description | Objectives |
|---|---|---|---|
| 1 | [Digital Background and CMOS process](#1-digital-background-and-cmos-process) | • Overview of knowledge for Digital Design.<br>• Physical Structure and Fabrication Overview | • Grasp fundamental digital design concepts.<br>• Understand the IC fabrication flow and CMOS structures.
| 2 | Input of PnR flow | Netlist, Constraint (SDC), Physical Library File (.lib), UPF, DEF | Identify the input, output, optimization goal, and feedback loop of each stage.
| 3 | Digital Design and PnR flow | • Floorplan (Initializaion) <br> • Placement (PreCTS) <br> • Clock Tree Synthesis (PostCTS) <br> • Routing <br> • Timing Closure <br> • Physical Verification and Signoff | • Place every implementation stage in the RTL-to-GDS flow <br> • Distinguish a generated GDS from a signoff-qualified layout
|
 
### 1. Digital Background and CMOS process


| | |
|:---|:---|
| **Digital Circuits** <br> ▪ Combinational Logic: AND, OR, INV ... <br> ▪ Sequential Logic: Flip-Flop, Latches ... <br><br> **Timing Concepts** <br> ▪ Clock drives sequential elements <br> ▪ Setup / Hold time define valid data window <br> ▪ Slack = Required time - Arrival time | **Design Abstraction** <br> ▪ RTL -> Behavioral description (Verilog/VHDL) <br> ▪ Gate-level Netlist -> Logic mapped to standard cells <br> ▪ Physical Layout -> Placement & Routing on silicon <br><br> **Standard Cell Library** <br> ▪ Building blocks: INV, NAND, NOR, DFF ... <br> ▪ Characterized for timing, power, area <br> ▪ Used during synthesis & PnR |

**CMOS Inverter — Physical Structure and Layout**

<p align="center">
  <img src="../../assets/topic-01/cmos_inverter_physical_shape.png"
       alt="CMOS inverter physical structure and layout"
       width="850">
</p>

<p align="center">
  <img src="../../assets/topic-01/cmos_inverter_layout.png"
       alt="CMOS inverter physical structure and layout"
       width="850">
</p>

A CMOS inverter consists of an **nMOS transistor** formed in the p-substrate and a **pMOS transistor** formed inside an n-well.

- The gates of both transistors are connected together to form the input **A**.
- Their drains are connected together to form the output **Y**.
- The nMOS source is connected to **GND**, while the pMOS source is connected to **VDD**.
- **Substrate tap** and **well tap** provide proper body connections to GND and VDD.
- The physical layout represents these devices using diffusion, polysilicon, contacts, wells, and metal interconnect layers.

### CMOS Fabrication Overview
<p align="center">
  <img src="../../assets/topic-01/cmos_process.png"
       alt="CMOS inverter physical structure and layout"
       width="850">
</p>











