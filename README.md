# Automatic Night Light Circuit - ENEE2360 Project



## 🌙 Project Overview
An analog electronics design that automatically activates an LED when ambient light falls below a configurable threshold. Implemented both practically on breadboard and simulated in PSpice, this project demonstrates light sensing using an LDR with comparator-based switching.

## 📋 Key Specifications
- **Input Voltage**: 9V DC
- **Light Sensor**: Light Dependent Resistor (LDR)
- **Comparator**: μA741 Op-amp
- **Switching Element**: NPN Transistor (2N3904)
- **Threshold Adjustment**: 100kΩ potentiometer
- **Load**: LED with current-limiting resistor

## 🛠️ Circuit Components
| Component | Role |
|-----------|------|
| LDR | Light sensing (10kΩ @ lux → 400kΩ dark) |
| μA741 Op-amp | Voltage comparator |
| 2N3904 Transistor | LED switch |
| 100kΩ Potentiometer | Threshold adjustment |
| 1.7kΩ Feedback Resistor | Hysteresis control |
| 5x Protection Diodes | Signal conditioning |

## 📊 Performance Characteristics
**Node Voltages (Measured):**
| Condition | VA | VB | VC | VD | VE |
|-----------|----|----|----|----|----|
| Dark (LED ON) | 1.3V | 1.5V | 6.34V | 2.75V | 2.1V |
| Light (LED OFF) | 1.6V | 4.0V | 0.0V | 0.58V | 9.2V |

**Threshold Analysis:**
- Upper Threshold (Simulated): 3.58V
- Lower Threshold (Simulated): 1.24V
- Calculated Error < 1.5% vs measurements

## 🔬 Project Phases
1. **Practical Implementation**
   - Breadboard construction
   - Potentiometer calibration
   - Voltage measurements under light/dark conditions

2. **PSpice Simulation**
   - LDR modeling (10kΩ-600kΩ range)
   - VPWL source replacement analysis
   - Transient response plotting

3. **Theoretical Verification**
   - Hand calculations of threshold voltages
   - Hysteresis window analysis
   - Error comparison between simulation and calculation

