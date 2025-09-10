# My First PCB - Microcontroller and USB Interface Board

## 📋 Project Overview

This repository contains the design files for my first printed circuit board (PCB) - a microcontroller and USB interface system built around the STM32F103C8T6 ARM Cortex-M3 processor. This project represents a significant milestone in my electronics engineering journey, demonstrating practical application of hardware design principles.

## 🔧 Hardware Specifications

### Core Components
- **Microcontroller**: STM32F103C8T6 (ARM Cortex-M3, 72MHz, 64KB Flash, 20KB RAM)
- **Power Management**: AMS1117-3.3V Linear Voltage Regulator
- **Connectivity**: USB-C Connector for data and power
- **Clock Source**: 16MHz Crystal Oscillator
- **Voltage Rails**: 5V and 3.3V power distribution

### Key Features
- ✅ Complete GPIO breakout for all microcontroller pins
- ✅ USB-C interface with proper differential pair routing
- ✅ Comprehensive power decoupling network
- ✅ External crystal oscillator for precise timing
- ✅ Power LED indicators
- ✅ Reset button for system control

## 📁 Repository Structure

```
├── Hardware/
│   ├── Schematics/
│   │   └── pcb-schematic.pdf
│   ├── PCB_Layout/
│   │   └── pcb-layout.pdf
│   ├── Gerber_Files/
│   │   └── manufacturing_files/
│   └── BOM/
│       └── bill_of_materials.xlsx
├── Documentation/
│   ├── Design_Notes.md
│   └── Pin_Mapping.md
├── Images/
│   ├── pcb_3d_render.png
│   └── schematic_overview.png
└── README.md
```

## 🛠️ Design Tools

- **EDA Software**: KiCad 7.x
- **Schematic Capture**: KiCad Eeschema
- **PCB Layout**: KiCad Pcbnew
- **3D Visualization**: KiCad 3D Viewer

## ⚡ Power Architecture

### Power Supply Design
- **Input**: 5V via USB-C or external power jack
- **Regulation**: AMS1117-3.3V for stable 3.3V rail
- **Decoupling**: Multiple capacitor values (1µF, 100nF, 10nF) for clean power delivery
- **Protection**: Reverse polarity protection and overcurrent limiting

### Power Consumption
- **Active Mode**: ~20mA (estimated)
- **Sleep Mode**: <1mA (microcontroller dependent)

## 🔌 Pinout and Connectivity

### USB-C Interface
- **Power**: VBUS, GND
- **Data**: D+, D- (USB 2.0 Full Speed)
- **Configuration**: CC1, CC2 for USB-C compliance

### GPIO Breakout
- All STM32F103C8T6 pins accessible via 0.1" headers
- Standard pin numbering and labeling
- Compatible with breadboard prototyping

## 📐 PCB Specifications

- **Board Size**: 50mm x 30mm (approximate)
- **Layer Count**: 2-layer PCB
- **Thickness**: 1.6mm standard
- **Copper Weight**: 1oz
- **Via Size**: 0.2mm drill, 0.45mm pad
- **Minimum Trace Width**: 0.15mm
- **Minimum Spacing**: 0.15mm

## 🔧 Manufacturing Notes

### PCB Fabrication
- Standard FR4 substrate
- HASL (Hot Air Solder Leveling) finish
- Green solder mask with white silkscreen
- Design Rule Check (DRC) compliant

### Assembly Considerations
- SMD components: 0805 and SOIC packages
- Through-hole components for headers and connectors
- Hand soldering friendly component selection

## 📊 Bill of Materials (BOM)

| Designator | Component | Package | Quantity | Notes |
|------------|-----------|---------|----------|-------|
| U1 | STM32F103C8T6 | LQFP-48 | 1 | Main microcontroller |
| U2 | AMS1117-3.3 | SOT-223 | 1 | Voltage regulator |
| J1 | USB-C Connector | USB-C | 1 | Power and data |
| Y1 | 16MHz Crystal | HC-49S | 1 | Clock source |
| C1-C10 | Various Capacitors | 0805 | 10 | Decoupling and filtering |
| R1-R5 | Various Resistors | 0805 | 5 | Pull-ups and current limiting |

*Complete BOM available in `/Hardware/BOM/` directory*

## 🚀 Getting Started

### Prerequisites
- KiCad 7.x or later
- Basic understanding of PCB design principles
- PCB manufacturing service account (JLCPCB, PCBWay, etc.)

### Viewing the Design
1. Clone this repository
2. Open the `.kicad_pro` file in KiCad
3. View schematics in Eeschema
4. Examine PCB layout in Pcbnew

### Manufacturing
1. Generate Gerber files from Pcbnew
2. Create drill files
3. Export pick and place files (if needed)
4. Upload to your preferred PCB manufacturer

## 📈 Future Improvements

- [ ] Add USB bootloader capability
- [ ] Implement USB device classes (CDC, HID)
- [ ] Add onboard sensors (temperature, accelerometer)
- [ ] Improve power efficiency with switching regulator
- [ ] Add wireless connectivity (ESP32 integration)
- [ ] Implement proper EMI/EMC design practices

## 🤝 Contributing

This is a learning project, but suggestions and improvements are welcome! Please feel free to:
- Open issues for design discussions
- Submit pull requests for documentation improvements
- Share your own implementations and modifications

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**[Your Name]**
- B.Tech ECE Final Year Student
- Electronics and Hardware Design Enthusiast
- GitHub: [@Naurasshaji][(https://github.com/NaurasShaji)]
- LinkedIn: [Nauras Shaji][((https://www.linkedin.com/in/nauras-shaji-/)]

## 🙏 Acknowledgments

- STMicroelectronics for comprehensive documentation
- KiCad development team for the excellent EDA tools
- Electronics engineering community for inspiration and guidance
- My professors and mentors for their support

***

⭐ **If you find this project helpful, please consider giving it a star!** ⭐

**Project Status**: ✅ Design Complete | 🔄 Testing Phase | 📋 Documentation In Progress

*Last Updated: September 10, 2025*
