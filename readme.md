# 🖥️ RISC-V Reference SoC Tapeout Program VSD

<div align="center">

![RISC-V](https://img.shields.io/badge/RISC--V-SoC%20Tapeout-blue?style=for-the-badge&logo=riscv)
![VSD](https://img.shields.io/badge/VSD-Program-orange?style=for-the-badge)
![Participants](https://img.shields.io/badge/Participants-3500+-success?style=for-the-badge)
![India](https://img.shields.io/badge/Made%20in-India-saffron?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjgiIGZpbGw9IiNGRjk5MzMiLz4KPHJlY3QgeT0iOCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjgiIGZpbGw9IiNGRkZGRkYiLz4KPHJlY3QgeT0iMTYiIHdpZHRoPSIyNCIgaGVpZ2h0PSI4IiBmaWxsPSIjMTM4ODA4Ii8+Cjwvc3ZnPgo=)

</div>

Welcome to my journey through the **SoC Tapeout Program VSD**!

This repository documents my **week-by-week progress** with tasks inside each week.

<div align="center">

> *"In this program, we learn to design a System-on-Chip (SoC) from basic RTL to GDSII using open-source tools. Part of India's largest collaborative RISC-V tapeout initiative, empowering 3500+ participants to build silicon and advance the nation's semiconductor ecosystem."*

</div>

<div align="center">

```
📝 RTL Design → 🔄 Synthesis → 🏗️ Physical Design → 🎯 Tapeout Ready
```

</div>

<details>
	<summary>Week 0 - Setup and Tools Installation </summary>
	
# Task 1
## RTL to GDSII SoC Design Flow

This covers the complete journey of designing a **System-on-Chip (SoC)**, starting from high-level specifications and ending at a verified GDSII layout.

---

## 🔹 Design Flow Steps

### 1. **Chip Modelling (O1)**

* Begin with **specifications** using a **C model**.
* Create a **C testbench** to validate functionality at this level.

---

### 2. **RTL Design (O2)**

* Write the **soft copy of hardware** using **RTL (Verilog)**.
* Model different blocks:
  * **Processor**
  * **Peripherals / IPs**
* Verify functionality through RTL testbenching.

---

### 3. **Synthesis & Netlist Generation**

* Convert RTL into a **Gate-Level Netlist**.
* Include supporting elements:

  * **Macros (synthesized RTL)**
  * **Analog IPs (functional RTL)**
* Netlist represents the circuit structure in terms of logic gates.

---

### 4. **SoC Integration (O3)**

* Integrate **Processor, Macros, Analog IPs, GPIOs, and Peripherals** into a single SoC.
* Validate correctness of the overall system.

---

### 5. **Physical Design (RTL2GDS)**

* Perform the following steps:

  * **Floorplanning**
  * **Placement**
  * **Clock Tree Synthesis (CTS)**
  * **Routing**
* Place **hardened macros and analog IP libraries** in layout.
* Generate the **GDSII file** (final chip layout).

---

### 6. **Verification & Signoff**

* Run **DRC (Design Rule Check)** to ensure layout follows manufacturing rules.
* Run **LVS (Layout vs. Schematic)** to confirm layout matches logical design.
* A clean DRC/LVS means the design is ready for fabrication (tape-out).

<img width="575" alt="yosys" src="week 0/assets/Task1_RTLtoGDS_Flow.png">

---

## ✅ Final Validation

The SoC design is declared successful when:

**O1 = O2 = O3 = O4**

* **O1** → C Model (Specs)
* **O2** → RTL Design
* **O3** → SoC Integration
* **O4** → Final SoC with Peripherals

This equivalence ensures the chip behaves **consistently** across specification, RTL, integration, and physical implementation.

<img width="575" alt="yosys" src="week 0/assets/Task1goal.png">

# Task 2

## Yosys
```
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys 
$ sudo apt install make (If make is not installed please install it) 
$ sudo apt-get install build-essential clang bison flex \
    libreadline-dev gawk tcl-dev libffi-dev git \
    graphviz xdot pkg-config python3 libboost-system-dev \
    libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make 
$ sudo make install
```
<img width="575" alt="yosys" src="week 0/assets/yosys.png">

## Iverilog
```
$ sudo apt-get install iverilog
```
<img width="702" alt="iverilog" src="week 0/assets/iverilog.png">

## GTKWave
```
$ sudo apt update
$ sudo apt install gtkwave
```
<img width="1008" alt="gtkwave" src="week 0/assets/gtkwave.png">

### 🌟 Key Learnings from Week 0
- Installed and verified **open-source EDA tools** successfully.  
- Learned about **basic environment setup** for RTL design and synthesis.  
- Prepared the system for upcoming **RTL → GDSII flow experiments**.
</details>

</div>

---

## 🙏 **Acknowledgment**
I am thankful to [**Kunal Ghosh**](https://github.com/kunalg123) and Team **[VLSI System Design (VSD)](https://vsdiat.vlsisystemdesign.com/)** for the opportunity to participate in the ongoing **RISC-V SoC Tapeout Program**.  

I also acknowledge the support of **RISC-V International**, **India Semiconductor Mission (ISM)**, **VLSI Society of India (VSI)**, and [**Efabless**](https://github.com/efabless) for making this initiative possible.  
<div align="center">

