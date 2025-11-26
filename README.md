<h1 align="center">Hello World 👋, I'm Daniel Narbón</h1>
<h3 align="center">A passionate electronics engineer from Barcelona, Spain</h3>

I have experience working at University of Barcelona as a researcher where, among many other things, I contributed to [this paper](https://doi.org/10.1038/s41528-024-00374-4) on flexible electronics.

---

## Project 1 – Sensorless BLDC ESC (3-phase motor controller)

Custom 10–12 V ESC for a 3-phase BLDC motor, with trapezoidal commutation, BEMF zero-cross detection and a fully custom power PCB (MOSFET half-bridges + IR gate drivers + MSP432 interface).

### PCB design

<p align="center">
  <img width="947" height="885" alt="BLDC_ESC_PCB_no_copper_pours" src="https://github.com/user-attachments/assets/5a45e7cd-4caf-4d5f-a25b-7334eb9a42b7" />
  <br/>
  <sub>BLDC ESC – early PCB layout without copper pours (routing of 3-phase power stage).</sub>
</p>

<p align="center">
  <img width="939" height="832" alt="BLDC_ESC_PCB_with_copper_pours" src="https://github.com/user-attachments/assets/81cb04b5-ab3a-4611-ae83-d75f3cfae7a4" />
  <br/>
  <sub>BLDC ESC – final PCB layout with copper pours and power planes.</sub>
</p>

<p align="center">
  <img width="1108" height="816" alt="BLDC_ESC_schematic" src="https://github.com/user-attachments/assets/06dfbe08-ae32-4d78-b66b-c573f30089b8" />
  <br/>
  <sub>Complete ESC schematic: MSP432, 3 half-bridges, gate drivers, BEMF network and protection.</sub>
</p>

<p align="center">
  <img width="1018" height="858" alt="BLDC_ESC_render" src="https://github.com/user-attachments/assets/560e43db-410b-4f67-836b-2d16c32860f4" />
  <br/>
  <sub>3D render of the assembled ESC PCB.</sub>
</p>

### Power stage and 3-phase behaviour (SPICE)

<p align="center">
  <img width="1236" height="760" alt="BLDC_triphase_SPICE_commutation" src="https://github.com/user-attachments/assets/e7f65e2b-bf57-4eeb-9ee5-18740e3c51dc" />
  <br/>
  <sub>SPICE simulation of 3-phase commutation and phase voltages.</sub>
</p>

<p align="center">
  <img width="777" height="689" alt="BLDC_triphase_SPICE_timing" src="https://github.com/user-attachments/assets/dfb3f54d-58ed-4c45-9674-a316a468eb06" />
  <br/>
  <sub>Timing of the six-step commutation sequence for the BLDC.</sub>
</p>

### BEMF sensing and control

<p align="center">
  <img width="1168" height="579" alt="BLDC_triphase_control_and_BEMF" src="https://github.com/user-attachments/assets/cdc76103-094b-4166-afab-504231602f81" />
  <br/>
  <sub>Triphase control and BEMF sensing setup for sensorless operation.</sub>
</p>

<p align="center">
  <img width="738" height="138" alt="BLDC_BEMF_one_phase" src="https://github.com/user-attachments/assets/42c075ea-1321-4d26-9c11-3cfd9498f027" />
  <br/>
  <sub>Back-EMF zero-cross detection on a single phase.</sub>
</p>

<p align="center">
  <img width="1338" height="565" alt="BLDC_BEMF_two_phases" src="https://github.com/user-attachments/assets/7a81763f-3a2b-4565-8933-c5206e103280" />
  <br/>
  <sub>BEMF zero-cross detection on two phases, 120° phase-shifted.</sub>
</p>

---

## Project 2 – Self-balancing beam with dual BLDC + RTOS control

Mechatronic system that keeps a beam level using two BLDC motors, an IMU (sensor fusion with complementary filter) and a PID loop running on a Tiva-C Launchpad under FreeRTOS. Custom PCBs handle motor ESCs, power and sensor interfacing.

### Mechanical design and 3D model

<p align="center">
  <img width="1201" height="616" alt="balancing_beam_3D_model" src="https://github.com/user-attachments/assets/520bf382-27c6-4b7b-a886-41c27542f44a" />
  <br/>
  <sub>3D render of the self-balancing beam with dual BLDC actuation.</sub>
</p>

### Control and sensor fusion

<p align="center">
  <img width="414" height="270" alt="balancing_beam_sensor_fusion_plot" src="https://github.com/user-attachments/assets/86158886-1499-40fd-814f-d9411095398a" />
  <br/>
  <sub>Sensor fusion: accelerometer + gyroscope combined via complementary filter for angle estimation.</sub>
</p>

<p align="center">
  <img width="1365" height="503" alt="balancing_beam_FreeRTOS_architecture" src="https://github.com/user-attachments/assets/1742c542-3495-4d53-be28-c965c5f1eb96" />
  <br/>
  <sub>FreeRTOS architecture: IMU sampling, angle estimation, PID control and motor command tasks.</sub>
</p>

### Custom PCBs (controller + sensor board)

<p align="center">
  <img width="620" height="598" alt="balancing_beam_main_pcb_assembled_overlay" src="https://github.com/user-attachments/assets/625918a6-6c2e-415e-9d22-1b8ad7f93fdd" />
  <br/>
  <sub>Main controller PCB (assembled) with silkscreen/overlay highlighting key blocks.</sub>
</p>

<p align="center">
  <img width="660" height="597" alt="balancing_beam_main_pcb_kicad" src="https://github.com/user-attachments/assets/ccacbabb-4af1-4fe2-af70-d39bdeb8b68d" />
  <br/>
  <sub>Main controller PCB layout in KiCad (power, IMU, motor interfaces).</sub>
</p>

<p align="center">
  <img width="463" height="523" alt="balancing_beam_sensor_pcb_assembled_overlay" src="https://github.com/user-attachments/assets/59820dd1-77ea-420f-a7e6-0b56e28f2b9b" />
  <br/>
  <sub>Dedicated IMU/sensor PCB (assembled) with overlay.</sub>
</p>

### Final prototype

<p align="center">
  <img width="2316" height="1737" alt="balancing_beam_final_setup" src="https://github.com/user-attachments/assets/dbf61fb2-ad45-42b8-bcf8-87f09ea831e9" />
  <br/>
  <sub>Final self-balancing beam prototype with BLDCs, electronics and wiring.</sub>
</p>
