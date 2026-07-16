
For your KiCad schematics, the control board for the catheter pump must run specific safety logic loops to maintain absolute structural stability during fluid movement. Your repository files can define this hardware mapping layout:

Component Pin Allocation Grid

| Sensor Sub-System | Hardware Interface Type | Microcontroller Pin Designation | Fail-Safe Interruption Logic |
| **Piezo-Resistive Pressure Transducer** | SPI Bus (Differential) | `SPI_SCK` / `SPI_MISO` / `PIN_A0` | Shuts down the pump motor instantly if line pressure exceeds **15 psi** due to lipid thickening. |
| **Ultrasonic Bubble Detector** | Digital Input (Interrupt) | `GPIO_INT_EXT1` | Triggers a hard safety stop if an air or gas gap breaks the ultrasonic sound path across the line. |
| **Optical Flow Sensor** | PWM / Pulse Counter | `TIM_CH1_PIN` | Monitors for low-flow anomalies or sudden downstream blocks. |

* * * * *
