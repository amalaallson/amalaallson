<div align="center">

<img src="./assets/hero.svg" width="100%" alt="AMALA ALLSON - Building intelligence at the hardware level. Embedded systems laboratory boot screen." />

<br/>

**Amala Allson N**
Electronics and Communication Engineering Student · Embedded Systems Developer · Hardware & Firmware Engineer

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-amalaallson-0D1624?style=flat-square&logo=github&logoColor=00E5FF)](https://github.com/amalaallson)
[![Hardware](https://img.shields.io/badge/JUMP_TO-HARDWARE-0D1624?style=flat-square&logoColor=00E5FF)](#hardware)
[![Projects](https://img.shields.io/badge/JUMP_TO-PROJECTS-0D1624?style=flat-square)](#projects)
[![Skills](https://img.shields.io/badge/JUMP_TO-SKILLS-0D1624?style=flat-square)](#skills)

</div>

<!-- Add LinkedIn / email badges here once you want them public:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-profile-0D1624?style=flat-square&logo=linkedin&logoColor=00E5FF)](https://www.linkedin.com/in/YOUR-HANDLE)
[![Email](https://img.shields.io/badge/Email-contact-0D1624?style=flat-square&logo=gmail&logoColor=00E5FF)](mailto:YOUR-EMAIL)
-->

Electronics and Communication Engineering student passionate about embedded systems, low-level firmware, hardware integration and intelligent electronic systems. My direction: **embedded systems, hardware–firmware development and semiconductor engineering.**

<table>
<tr>
<td><b>FOCUS</b></td>
<td>Bare-metal programming · Microcontroller architecture · Hardware–firmware integration · Sensor interfacing</td>
</tr>
<tr>
<td><b>DOMAINS</b></td>
<td>IoT & edge computing · Embedded AI · Digital electronics · Communication protocols · Real-time monitoring</td>
</tr>
<tr>
<td><b>PLATFORMS</b></td>
<td>STM32 · ESP32 · PSoC 4</td>
</tr>
</table>

<img src="./assets/divider.svg" width="100%" alt="" />

<a id="hardware"></a>

## HARDWARE ECOSYSTEM // SYSTEM ARCHITECTURE

<img src="./assets/hardware-architecture.svg" width="100%" alt="Generic microcontroller interface map: GPIO, PWM, ADC/DAC, I2C, I2S, 1-wire and UART connected to an MCU, with STM32 Blue Pill, ESP32 DevKit V1, PSoC 4100S Plus and ESP32-CAM as target platforms." />

<sub>Generic interface map. Pin numbers and wiring are shown only where a project documents them, so none are shown here.</sub>

<details>
<summary><b>Text-based view (mobile friendly)</b></summary>

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00E5FF','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart LR
  MCU(["MCU<br/>GPIO · Timers · IRQ<br/>ADC · DAC · PWM"])
  MCU -- I2C --> S1["MPU6050<br/>SSD1306 OLED"]
  MCU -- I2S --> S2["INMP441 mic<br/>(ESP32 project)"]
  MCU -- "1-wire" --> S3["DHT11"]
  MCU -- UART --> S4["Serial monitor"]
  MCU -- GPIO --> O1["LED · Buzzer<br/>Push button"]
  MCU -- PWM --> O2["Output control"]
  MCU -- ADC --> O3["Analog input"]
```

</details>

| Platform | Device | Role in my work |
|:--|:--|:--|
| **STM32 Blue Pill** | STM32F103C6T6A | Bare-metal / CubeIDE firmware |
| **ESP32 DevKit V1** | ESP32 | Sensor + signal-acquisition projects |
| **PSoC 4100S Plus** | Cortex-M0+ | Peripheral and interrupt exercises |
| **ESP32-CAM** | ESP32 + camera | Exploration, planned integration |

<img src="./assets/divider.svg" width="100%" alt="" />

<a id="projects"></a>

## FEATURED PROJECTS

> **Repository status.** The embedded projects below are not yet published as public repositories on this account, so none are linked. Each card is marked **REPO PENDING**. Links are added as projects are published.

### A · PneuSense — Intelligent Pneumatic System Monitoring

![status](https://img.shields.io/badge/STATUS-REPO_PENDING-8B5CF6?style=flat-square&labelColor=0D1624)
![platform](https://img.shields.io/badge/ESP32_DevKit_V1-0D1624?style=flat-square&logo=espressif&logoColor=00E5FF)

| | |
|:--|:--|
| **Problem** | Monitor a pneumatic system through acoustic signal acquisition and raise local alerts. |
| **Hardware** | ESP32 DevKit V1 · INMP441 microphone · SSD1306 OLED · LED · buzzer |
| **Stack** | Embedded firmware · signal acquisition · monitoring interface |
| **Wiring** | Pin map not yet documented publicly |
| **Repository** | Pending |
| **Demo** | Pending |

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00E5FF','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart LR
  MIC["INMP441<br/>microphone"] -- I2S --> ESP["ESP32<br/>DevKit V1"]
  ESP --> SIG["Signal<br/>processing"]
  SIG --> LED["LED"]
  SIG --> BUZ["Buzzer"]
  SIG --> OLED["SSD1306<br/>OLED"]
  SIG --> MON["Monitoring<br/>interface"]
```

<sub>Functional signal flow. Not a wiring diagram.</sub>

### B · Secure QR Medicine Authentication

![status](https://img.shields.io/badge/STATUS-REPO_PENDING-8B5CF6?style=flat-square&labelColor=0D1624)
![python](https://img.shields.io/badge/Python-0D1624?style=flat-square&logo=python&logoColor=00D68F)
![mysql](https://img.shields.io/badge/MySQL-0D1624?style=flat-square&logo=mysql&logoColor=00D68F)

| | |
|:--|:--|
| **Problem** | Verify medicine authenticity by scanning a QR code or barcode and checking it against a database. |
| **Hardware** | Scanning input only where implemented (not documented publicly) |
| **Stack** | Python processing · MySQL · dashboard |
| **Contribution split** | Software and data-processing project; embedded hardware is not claimed |
| **Repository** | Pending |

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00D68F','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart LR
  SCAN["QR / barcode<br/>scan"] --> PY["Python<br/>processing"] --> DB[("MySQL")] --> DASH["Dashboard"]
```

### C · AXI Semiconductor X-ray Defect Inspection

![status](https://img.shields.io/badge/STATUS-REPO_PENDING-8B5CF6?style=flat-square&labelColor=0D1624)
![pytorch](https://img.shields.io/badge/PyTorch-0D1624?style=flat-square&logo=pytorch&logoColor=8B5CF6)
![opencv](https://img.shields.io/badge/OpenCV-0D1624?style=flat-square&logo=opencv&logoColor=8B5CF6)

| | |
|:--|:--|
| **Problem** | Detect defects in semiconductor X-ray inspection images. |
| **Stack** | Python · PyTorch · YOLOv8 · OpenCV |
| **AI / software** | Image preprocessing, model training and defect detection |
| **Embedded hardware** | None claimed. This is a computer-vision project. |
| **Repository** | Pending |

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#8B5CF6','lineColor':'#00E5FF','fontFamily':'monospace'}}}%%
flowchart LR
  IMG["X-ray<br/>images"] --> CV["OpenCV<br/>preprocessing"] --> YOLO["YOLOv8<br/>(PyTorch)"] --> OUT["Defect<br/>detections"]
```

### D · STM32 Bare-Metal Development

![status](https://img.shields.io/badge/STATUS-REPO_PENDING-8B5CF6?style=flat-square&labelColor=0D1624)
![stm32](https://img.shields.io/badge/STM32F103C6T6A-0D1624?style=flat-square&logo=stmicroelectronics&logoColor=00D68F)

| | |
|:--|:--|
| **Problem** | Learn the STM32 peripheral stack at register level and control outputs from analog input. |
| **Hardware** | STM32 Blue Pill (STM32F103C6T6A) · LED |
| **Stack** | Embedded C · STM32CubeIDE |
| **Topics** | GPIO · ADC · LED intensity control |
| **Wiring** | Pin map not yet documented publicly |
| **Repository** | Pending |

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00E5FF','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart LR
  AIN["Analog<br/>input"] -- ADC --> FW["STM32F103C6T6A<br/>firmware"] -- "intensity control" --> LED["LED"]
```

<sub>Functional flow. Not a wiring diagram.</sub>

### E · PSoC 4100S Plus Development

![status](https://img.shields.io/badge/STATUS-REPO_PENDING-8B5CF6?style=flat-square&labelColor=0D1624)
![psoc](https://img.shields.io/badge/PSoC_Creator_4.4-0D1624?style=flat-square&logoColor=00D68F)

| | |
|:--|:--|
| **Problem** | Practice peripheral configuration and interrupt-driven input on a PSoC 4. |
| **Hardware** | PSoC 4100S Plus · push button |
| **Stack** | Embedded C · PSoC Creator 4.4 |
| **Topics** | GPIO · timers · PWM · ADC · UART · I2C · interrupt handling |
| **Application** | Push-button counter with reset |
| **Repository** | Pending |

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00E5FF','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart LR
  BTN["Push<br/>button"] -- "GPIO IRQ" --> ISR["Interrupt<br/>handler"] --> CNT["Counter<br/>+ reset"]
```

<img src="./assets/divider.svg" width="100%" alt="" />

## PUBLIC REPOSITORIES

Software and web work currently public on this account.

| Repository | Language | Note |
|:--|:--|:--|
| [Portfolio](https://github.com/amalaallson/Portfolio) | TypeScript | Web portfolio |
| [vitalsync](https://github.com/amalaallson/vitalsync) | TypeScript | Web application |
| [Monastery360](https://github.com/amalaallson/Monastery360) | n/a | Fork of [Bavithran100/Monastery360](https://github.com/Bavithran100/Monastery360) |
| [lmsapp](https://github.com/amalaallson/lmsapp) | n/a | Software project |
| [Allson](https://github.com/amalaallson/Allson) | n/a | Scratch repository |
| [allson77](https://github.com/amalaallson/allson77) | n/a | Scratch repository |

<img src="./assets/divider.svg" width="100%" alt="" />

<a id="skills"></a>

## TECHNICAL SKILLS

<table>
<tr>
<td width="160"><b>PROGRAMMING</b></td>
<td>
<img src="https://img.shields.io/badge/Embedded_C-0D1624?style=flat-square&logo=c&logoColor=00E5FF" alt="Embedded C"/>
<img src="https://img.shields.io/badge/C-0D1624?style=flat-square&logo=c&logoColor=00E5FF" alt="C"/>
<img src="https://img.shields.io/badge/Python-0D1624?style=flat-square&logo=python&logoColor=00E5FF" alt="Python"/>
<img src="https://img.shields.io/badge/C++-0D1624?style=flat-square&logo=cplusplus&logoColor=00E5FF" alt="C++"/>
<img src="https://img.shields.io/badge/Java-0D1624?style=flat-square&logoColor=00E5FF" alt="Java"/>
</td>
</tr>
<tr>
<td><b>MICROCONTROLLERS</b></td>
<td>
<img src="https://img.shields.io/badge/STM32-0D1624?style=flat-square&logo=stmicroelectronics&logoColor=00D68F" alt="STM32"/>
<img src="https://img.shields.io/badge/ESP32-0D1624?style=flat-square&logo=espressif&logoColor=00D68F" alt="ESP32"/>
<img src="https://img.shields.io/badge/PSoC_4-0D1624?style=flat-square&logoColor=00D68F" alt="PSoC 4"/>
</td>
</tr>
<tr>
<td><b>HARDWARE</b></td>
<td>
<img src="https://img.shields.io/badge/Sensor_Interfacing-0D1624?style=flat-square" alt="Sensor interfacing"/>
<img src="https://img.shields.io/badge/GPIO-0D1624?style=flat-square" alt="GPIO"/>
<img src="https://img.shields.io/badge/ADC_/_DAC-0D1624?style=flat-square" alt="ADC and DAC"/>
<img src="https://img.shields.io/badge/PWM-0D1624?style=flat-square" alt="PWM"/>
<img src="https://img.shields.io/badge/Timers-0D1624?style=flat-square" alt="Timers"/>
<img src="https://img.shields.io/badge/Interrupts-0D1624?style=flat-square" alt="Interrupts"/>
<img src="https://img.shields.io/badge/Circuit_Prototyping-0D1624?style=flat-square" alt="Circuit prototyping"/>
</td>
</tr>
<tr>
<td><b>COMMUNICATION</b></td>
<td>
<img src="https://img.shields.io/badge/UART-0D1624?style=flat-square" alt="UART"/>
<img src="https://img.shields.io/badge/I2C-0D1624?style=flat-square" alt="I2C"/>
</td>
</tr>
<tr>
<td><b>TOOLS</b></td>
<td>
<img src="https://img.shields.io/badge/STM32CubeIDE-0D1624?style=flat-square&logo=stmicroelectronics&logoColor=00E5FF" alt="STM32CubeIDE"/>
<img src="https://img.shields.io/badge/PSoC_Creator_4.4-0D1624?style=flat-square" alt="PSoC Creator 4.4"/>
<img src="https://img.shields.io/badge/VS_Code-0D1624?style=flat-square" alt="VS Code"/>
<img src="https://img.shields.io/badge/Git-0D1624?style=flat-square&logo=git&logoColor=00E5FF" alt="Git"/>
<img src="https://img.shields.io/badge/GitHub-0D1624?style=flat-square&logo=github&logoColor=00E5FF" alt="GitHub"/>
</td>
</tr>
<tr>
<td><b>AI & VISION</b></td>
<td>
<img src="https://img.shields.io/badge/PyTorch-0D1624?style=flat-square&logo=pytorch&logoColor=8B5CF6" alt="PyTorch"/>
<img src="https://img.shields.io/badge/YOLOv8-0D1624?style=flat-square&logoColor=8B5CF6" alt="YOLOv8"/>
<img src="https://img.shields.io/badge/OpenCV-0D1624?style=flat-square&logo=opencv&logoColor=8B5CF6" alt="OpenCV"/>
</td>
</tr>
</table>

<img src="./assets/divider.svg" width="100%" alt="" />

## HOW I BUILD SYSTEMS

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#0D1624','primaryTextColor':'#E6EDF3','primaryBorderColor':'#00E5FF','lineColor':'#8B5CF6','fontFamily':'monospace'}}}%%
flowchart TB
  A["01 · PROBLEM IDENTIFICATION"] --> B["02 · HARDWARE SELECTION"]
  B --> C["03 · CIRCUIT DESIGN"]
  C --> D["04 · FIRMWARE DEVELOPMENT"]
  D --> E["05 · SENSOR INTEGRATION"]
  E --> F["06 · TESTING & DEBUGGING"]
  F --> G["07 · SYSTEM VALIDATION"]
  F -. "fix and re-flash" .-> D
  style A stroke:#00E5FF
  style B stroke:#00E5FF
  style C stroke:#8B5CF6
  style D stroke:#8B5CF6
  style E stroke:#8B5CF6
  style F stroke:#00D68F
  style G stroke:#00D68F
```

<img src="./assets/divider.svg" width="100%" alt="" />

## GITHUB TELEMETRY

<div align="center">

<img src="https://ghchart.rshah.org/00E5FF/amalaallson" width="100%" alt="GitHub contribution graph for amalaallson" />

<table>
<tr>
<td align="center"><img src="https://github-readme-stats.vercel.app/api?username=amalaallson&hide_border=true&bg_color=080D16&title_color=00E5FF&icon_color=8B5CF6&text_color=94A3B8" alt="GitHub stats" /></td>
<td align="center"><img src="https://github-readme-stats.vercel.app/api/top-langs/?username=amalaallson&layout=compact&hide_border=true&bg_color=080D16&title_color=00E5FF&text_color=94A3B8" alt="Most used languages" /></td>
</tr>
<tr>
<td colspan="2" align="center"><img src="https://streak-stats.demolab.com/?user=amalaallson&hide_border=true&background=080D16&ring=00E5FF&fire=8B5CF6&currStreakLabel=00D68F&currStreakNum=E6EDF3&sideNums=E6EDF3&sideLabels=94A3B8&dates=94A3B8" alt="Contribution streak" /></td>
</tr>
</table>

</div>

<img src="./assets/divider.svg" width="100%" alt="" />

## CURRENT FOCUS // ROADMAP

<!-- Change [ ] to [x] only when a topic is genuinely complete. -->

- [ ] Advanced Embedded C
- [ ] STM32 bare-metal development
- [ ] Hardware–firmware integration
- [ ] RTOS fundamentals
- [ ] Embedded Linux
- [ ] Semiconductor and VLSI fundamentals
- [ ] Embedded AI

<img src="./assets/divider.svg" width="100%" alt="" />

<div align="center">

**DESIGNING. CONNECTING. DEBUGGING. BUILDING.**

[![GitHub](https://img.shields.io/badge/GitHub-amalaallson-0D1624?style=flat-square&logo=github&logoColor=00E5FF)](https://github.com/amalaallson)

</div>
