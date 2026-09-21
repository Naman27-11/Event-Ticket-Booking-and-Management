# High-Frequency Wireless Spectrum Grid & Bandwidth Manager

## Overview of the Project
The **High-Frequency Wireless Spectrum Grid & Bandwidth Manager** is an Electronics & Communication Engineering (ECE) console-based transaction application designed to handle optimal radio frequency (RF) distribution, sub-carrier channel tracking, and transmission session provisions. 

To bridge software with physical ECE environments without external hardware dependencies, the engine integrates a **real-time hardware telemetry link**. It directly samples the host system's hardware execution layer (microsecond processing clock jitter and garbage collection heap sizes) during usage routines. These dynamic computational metrics are mathematically mapped into real-time RF data points—specifically **Signal-to-Noise Ratio (SNR)** and **Channel Congestion** percentages. Built with defensive error trapping, the system maintains strict thread safety and prevents runtime processing failures.

## Features
* **RF Infrastructure Registry (Admin):** Allows network managers to initialize wireless nodes or satellite arrays with specific total channel capacities and licensing fees.
* **Dynamic Hardware Telemetry Integration:** Native system sampling loops that query CPU time-slice jitter and memory load arrays, converting them into live **SNR (dB)** and **Congestion (%)** matrix feeds.
* **Bandwidth Provisioning Module:** An interface enabling communications subsystems or field engineers to instantly check real-time channel balances and secure frequency slices.
* **Session Matrix Authorization Key:** Automated compilation of secure, unique 8-character uppercase hexadecimal token markers using UUIDv4 string segmentation.
* **Bidirectional Restoration Engine:** Validates transmission keys, tears down outdated session records, and returns leased frequency spectrum slices instantly to the open base-station grid pool.

## Technologies/Tools Used
* **Programming Language:** Python 3.x
* **Core Standard Modules:** `uuid` (token generation), `time` (nanosecond clock profiling), `random` (micro-calculation loops), `gc` (runtime heap assessment)
* **Development Environment:** Any standard terminal text environment (e.g., VS Code, PyCharm, Terminal)
* **Version Control:** Git & GitHub

## Steps to Install & Run the Project

### Prerequisites
Ensure that **Python 3.x** is installed on your local workstation machine. You can verify your environment configuration by typing:
python --version

### Installation
1. Clone this repository to your local drive directory:
   git clone https://github.com
2. Change directory into the project folder workspace:
   cd spectrum-grid-manager

### Running the Application
Launch the terminal controller application layout using the default Python execution statement:
python main.py

## Instructions for Testing
To evaluate the integrity rules and real-time execution parameters of the spectrum manager, input the following terminal commands:

1. **Test Case 1 (Base-Station Deployment):** Select option `1`. Create a new wireless array transceiver with ID `5G-TEST`, Capacity `30` sub-carrier slots, and Rate `25.0`. Confirm successful indexing.
2. **Test Case 2 (Live Telemetry Audit):** Select option `2`. Inspect the dynamic readout table columns. Verify that the **Live SNR (dB)** and **Live Congestion (%)** columns display auto-calculated numeric data that changes dynamically based on your local machine's processing state.
3. **Test Case 3 (Bandwidth Allocation):** Proceed within option `2`. Input target Node ID `5G-TEST`, pass your engineer handle name, and specify a slice requirement of `5` channels. Verify that the system provides the accurate dollar balance assessment and prints an 8-character session token.
4. **Test Case 4 (Grid Capacity Validation):** Re-enter option `2`. Try to provision an impossible slice quantity of `40` channels for node `5G-TEST`. The transaction should be safely blocked with a clear warning explaining that inventory bounds have been breached.
5. **Test Case 5 (Session De-provisioning):** Select option `3`. Input the exact 8-character auth token created during Test Case 3. Confirm that the application removes the connection index logs and returns the 5 channel slots to the open transceiver grid.

## Screenshots
### Real-Time Infrastructure Grid Readout Matrix
```text
==================================================================
HIGH-FREQUENCY SPECTRUM GRID MANAGER [REAL-TIME HARDWARE DATA LINK]
==================================================================

--- SPECTRUM DISTRIBUTION PORTAL ---
1. Admin: Register Wireless Base-Station Array
2. System: View Live Telemetry Grid & Provision Bandwidth
3. Operations: Terminate Session & Release Channels
4. Shutdown Telemetry Controller
Select operation path (1-4): 2

[ACTIVE RF BASE-STATION ARCHITECTURE GRID - SYSTEM METRIC FEEDS]
Node ID    | Transceiver Description          | Free Ch  | Live SNR   | Live Congestion
-------------------------------------------------------------------------------------
5G-MWM01   | Metro Millimeter-Wave Base Cell  | 100      | 32.5 dB    | 4.12 %    
SAT-LEO3   | LEO Ku-Band Transponder Array    | 40       | 28.15 dB   | 1.84 %    
```
