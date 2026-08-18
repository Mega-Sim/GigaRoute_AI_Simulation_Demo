# GigaRoute Auto Simulation — Linux Public Preview

> **Download the application from the Assets section below.**  
> Do **not** use GitHub's automatically generated `Source code (zip)` or `Source code (tar.gz)` as the application package.

## 1. Download the application

Under **Assets**, download:

`GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz`

The accompanying `.sha256` file can be used to verify the downloaded package.

## 2. Download the sample DXF separately

The example layout is maintained in the repository and is **not the GitHub Source code archive**.

**Sample layout:** [Sample/Layout_Example.dxf](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/Sample/Layout_Example.dxf)

Open the link above and use **Download raw file** to save `Layout_Example.dxf` locally.

## 3. Run GigaRoute Auto Simulation

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

After the application starts:

**Open Layout → select the downloaded `Layout_Example.dxf` → run the simulation.**

## Quick guide for Korean users

- **프로그램:** 이 Release 페이지 아래 **Assets**에서 `GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz` 다운로드
- **받지 말 것:** GitHub가 자동 생성한 `Source code (zip)` / `Source code (tar.gz)`는 실행 프로그램이 아닙니다.
- **예제 도면:** [Sample/Layout_Example.dxf](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/Sample/Layout_Example.dxf)를 별도로 다운로드
- **실행:** 압축 해제 → `run_gigaroute.sh` → **Open Layout** → 다운로드한 `Layout_Example.dxf` 선택

## Documentation

- [English README](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/README.md)
- [한국어 README](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/README_KO.md)
- [简体中文 README](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/README_ZH.md)
- [日本語 README](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/blob/main/README_JA.md)

**Verified environment:** Ubuntu 22.04 x86_64 / Native C++ & Qt6
