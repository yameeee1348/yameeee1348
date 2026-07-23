<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=250&section=header&text=Jeong%20Won&fontSize=70&desc=Hardware%20Engineer&descAlignY=70&fontAlignY=35" alt="header" />
</div>

# 정원 (Jeong Won)
전자공학과를 졸업하고 SoC 설계, 검증 직무를 준비 중이다.
디지털 회로 설계, Verilog/SystemVerilog, FPGA 기반 시스템 구현 및 UVM 검증 환경 구축에 주력한다.

## Tech Stack
<div align="left">
  <img src="https://img.shields.io/badge/Verilog-005C8A?style=for-the-badge" alt="Verilog">
  <img src="https://img.shields.io/badge/SystemVerilog-005C8A?style=for-the-badge" alt="SystemVerilog">
  <img src="https://img.shields.io/badge/UVM-E0234E?style=for-the-badge" alt="UVM">
  <br>
  <img src="https://img.shields.io/badge/RISC--V-F2E500?style=for-the-badge&logoColor=black" alt="RISC-V">
  <img src="https://img.shields.io/badge/AMBA%20(APB/AXI)-4B0082?style=for-the-badge" alt="AMBA">
  <img src="https://img.shields.io/badge/UART/I2C/SPI-4B0082?style=for-the-badge" alt="Protocols">
  <br>
  <img src="https://img.shields.io/badge/FPGA-009688?style=for-the-badge" alt="FPGA">
  <img src="https://img.shields.io/badge/SoC%20Design-FF9800?style=for-the-badge" alt="SoC">
  <img src="https://img.shields.io/badge/AI%20Hardware-607D8B?style=for-the-badge" alt="AI Hardware">
</div>

## Core Projects
포트폴리오 기술서 기준으로 대표 프로젝트를 요약했다.  
프로필 README에서는 전체 흐름을 빠르게 보여주고, 세부 RTL/UVM 코드는 관련 레포지토리에서 확인할 수 있도록 구성했다.

### 1. M.A.T.S. - 기동형 자율 조준 및 타겟 시스템
<div align="center">

</div>

- **Summary**: OV7670 카메라 영상에서 드론을 실시간 검출하고, 좌표와 크기를 기반으로 Bounding Box와 경고 문구를 VGA 화면에 표시하는 FPGA 기반 영상 처리 시스템이다.
- **My Role**: UI_Generator 설계, Ready-Valid 기반 스트리밍 구조 구현, Bounding Box clipping 및 text rendering 로직 구현, CAM_Set UVM 검증 환경 구축
- **Keywords**: `SystemVerilog` `UVM` `OV7670` `VGA` `FIFO` `FSM` `FPGA`
- **More**: [M.A.T.S.](https://github.com/kccistcs1st/M.A.T.S.) / [CAM UVM](https://github.com/yameeee1348/Ondevice_UVM/tree/main/0716_CAM_UVM)

### 2. AXI4-Lite SPI/I2C Peripheral IP
<div align="center">

</div>

- **Summary**: AXI4-Lite BUS로 제어 가능한 SPI/I2C Peripheral IP를 설계하고, memory-mapped register 기반으로 통신 동작을 제어할 수 있도록 구현했다.
- **My Role**: AXI4-Lite slave register 구조 설계, SPI CPOL/CPHA mode FSM 구현, I2C START-ADDR-DATA-ACK-STOP timing 구현, UVM 기반 protocol 검증
- **Keywords**: `AXI4-Lite` `SPI` `I2C` `UVM` `VCS` `Verdi` `FPGA`
- **More**: [AXI_SPI](https://github.com/yameeee1348/Ondevice_RTL/tree/main/AXI_SPI) / [AXI_I2C](https://github.com/yameeee1348/Ondevice_RTL/tree/main/AXI_I2C)

### 3. Multi-cycle RV32I MCU
<div align="center">

</div>

- **Summary**: RV32I CPU를 Multi-cycle 구조로 확장하고, APB BUS를 통해 RAM, GPO, GPIO, FND, UART peripheral을 제어하는 MCU 형태로 구현했다.
- **My Role**: IF/ID/EX/MEM/WB state 기반 control path 설계, APB Master 구현, memory map 및 peripheral address decoding 구성, C/Assembly 기반 보드 동작 검증
- **Keywords**: `RV32I` `Multi-cycle CPU` `APB` `GPIO` `UART` `C` `FPGA`
- **More**: [RV32I](https://github.com/yameeee1348/Ondevice_RTL/tree/main/RV32I)

### 4. FPGA 기반 AI 포트홀 탐지 시스템
<div align="center">

</div>

- **Summary**: 도로 영상에서 포트홀을 탐지하고, 탐지 결과를 FPGA 출력 시스템과 연동해 경고 신호로 표시하는 임베디드 AI 시스템이다.
- **My Role**: AI 모델 구조 분석, OpenCV 기반 전처리, FPGA 리소스 제약을 고려한 경량화 구조 검토, 탐지 결과와 하드웨어 출력 timing 검증
- **Keywords**: `FPGA` `AI Hardware` `OpenCV` `CNN` `Image Processing` `UART/GPIO`
- **More**: 


## Repository Index
세부 구현 코드와 검증 환경은 아래 레포지토리에서 확인할 수 있다.

- [Ondevice_RTL](https://github.com/yameeee1348/Ondevice_RTL): RV32I, APB peripheral, AXI4-Lite SPI/I2C, UART/Sensor 등 RTL 설계 코드 모음
- [Ondevice_UVM](https://github.com/yameeee1348/Ondevice_UVM): SPI/I2C/UART/APB/CAM_Set 등 UVM 검증 환경 및 coverage 기반 테스트 코드 모음
