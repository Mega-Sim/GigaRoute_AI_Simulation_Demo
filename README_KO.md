# GigaRoute AI — Linux Native Preview

[English](README.md) | **한국어** | [简体中文](README_ZH.md) | [日本語](README_JA.md)

**Ubuntu 22.04 x86_64 환경에서 Linux 네이티브 실행을 확인했습니다.**

GigaRoute Auto Simulation은 크로스플랫폼 시뮬레이션 제품으로 준비 중이며, 현재 Public Preview는 Linux 네이티브 독립 실행 패키지 형태로 공개되어 있습니다.

## Quick Start — 무엇을 다운로드해야 하나요?

### 1. 프로그램은 GitHub Release에서 다운로드

**Linux Release:** https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/tag/public-preview-526-linux

Release 페이지의 **Assets**에서 아래 파일을 다운로드해 주세요.

`GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz`

> **`Source code (zip)` / `Source code (tar.gz)`는 프로그램이 아닙니다. 다운로드하지 않아도 됩니다.** GitHub가 자동 생성하는 공개 Demo 저장소 스냅샷이며 GigaRoute 실행 패키지가 아닙니다.

함께 제공되는 `.sha256` 파일로 다운로드한 프로그램 패키지의 무결성을 확인할 수 있습니다.

### 2. 예제 DXF는 Repository에서 별도로 다운로드

**예제 도면:** [`Sample/Layout_Example.dxf`](Sample/Layout_Example.dxf)

예제 도면은 프로그램 Release 패키지와 별도로 Repository의 `Sample/` 폴더에서 관리합니다. 위 파일 링크를 연 뒤 **Download raw file**로 `Layout_Example.dxf`를 PC에 저장해 주세요.

### 3. 프로그램 실행

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

실행 후:

**Open Layout → 별도로 다운로드한 `Layout_Example.dxf` 선택 → Simulation 실행**

## 화면 조작 및 단축키

GigaRoute의 2D와 3D 화면은 조작 방식이 조금 다릅니다. 처음부터 모든 단축키를 외우실 필요는 없으며, 일반적인 확인 작업은 **마우스 휠 + 화면 이동/회전 조작**만 알아도 충분합니다.

### 2D 화면

| 입력 | 동작 |
|---|---|
| **마우스 휠** | 마우스 커서 위치를 기준으로 확대 / 축소 |
| **가운데 버튼(MMB) + 드래그** | 도면 화면 이동(Pan) |
| **Shift + 왼쪽 버튼(LMB) + 드래그** | 도면 화면 이동(Pan) |
| **Ctrl + Shift + LMB + 드래그** | 드래그 방식 확대 / 축소 |
| **LMB 클릭** | 객체 선택 |
| **LMB 더블클릭 후 드래그** | 화면 이동(Pan) |
| **V**, **Home**, 또는 **0** | 전체 도면이 화면에 들어오도록 자동 맞춤(Fit) |
| **Ctrl + T** | 도면 / Station 텍스트 표시 ON/OFF |
| **Ctrl + D** | 진행 방향 화살표 표시 ON/OFF |

**2D에서 가장 편한 방법:** 확대/축소는 **마우스 휠**, 화면 이동은 **MMB + 드래그** 또는 **Shift + LMB + 드래그**를 사용하시면 됩니다. 화면을 너무 많이 확대하거나 이동해서 도면을 놓쳤다면 **V / Home / 0** 중 아무 키나 눌러 전체 도면을 다시 맞출 수 있습니다.

### 3D 화면

| 입력 | 동작 |
|---|---|
| **마우스 휠** | 확대 / 축소 |
| **Ctrl + LMB + 드래그** | 카메라 회전(Orbit) |
| **MMB + 드래그** | 카메라 화면 이동(Pan) |
| **Shift + Alt + LMB + 드래그** | 대체 화면 이동(Pan) 조작 |
| **Ctrl + Shift + Alt + LMB + 드래그** | 카메라 전후 이동(Dolly) |
| **LMB + 드래그** | 영역을 드래그하여 객체 선택 |
| **오른쪽 버튼(RMB)** | Context Menu 열기 |
| **Ctrl + D** | 3D 진행 방향 Marker 표시 ON/OFF |

**3D에서 가장 편한 방법:** **Ctrl + LMB + 드래그**로 모델을 회전해서 보고, **MMB + 드래그**로 화면을 옮기며, **마우스 휠**로 확대/축소하시면 됩니다.

### 마우스 버튼 표기

- **LMB** = Left Mouse Button = 마우스 왼쪽 버튼
- **MMB** = Middle Mouse Button = 마우스 가운데 버튼 / 휠 클릭
- **RMB** = Right Mouse Button = 마우스 오른쪽 버튼

> 팁: 2D 화면에서 도면 위치를 잃어버렸다면 **V**, **Home**, **0** 중 하나를 누르시면 전체 도면을 다시 화면에 맞출 수 있습니다.

### 다운로드 위치 요약

- **프로그램 실행파일:** GitHub **Releases / Assets에서만 다운로드**
- **예제 DXF:** Repository **`Sample/` 폴더에서 다운로드**
- **GitHub Source code 압축파일:** 프로그램 다운로드 파일이 아님

검증 환경:

- Ubuntu 22.04 x86_64
- GCC 11.x
- Native C++/Qt6 실행파일
- Qt runtime이 포함된 source-free Public Preview 패키지

이 버전은 브라우저 데모나 Windows 실행파일의 에뮬레이션이 아니라 GigaRoute Auto Simulation의 네이티브 Linux 빌드입니다.

**Public Preview 상태**

| 플랫폼 | 상태 |
|---|---|
| Ubuntu 22.04 x86_64 | Public Preview 릴리즈 제공 중 |
| Windows x64 | 공개 패키지 준비 중 |

## 보안 / 배포

- GigaRoute C/C++ 소스 코드는 Linux 패키지에 포함되지 않습니다.
- 공개 빌드에서는 application QML 원문이 고객 실행파일에 포함되지 않도록 처리합니다.
- 디버그 심볼, object 파일, static/import library, private build path 및 기타 개발 산출물은 release audit에서 제외됩니다.
- 공개 샘플 DXF는 데모용으로 정리된 레이아웃만 제공합니다.
- 다운로드 후 함께 제공되는 `.sha256` 파일로 TGZ 무결성을 확인할 수 있습니다.

> GitHub Release에 자동으로 표시되는 `Source code (zip)` / `Source code (tar.gz)`는 이 **공개 Demo 저장소의 스냅샷**이며 private `Sim_Core` 저장소 소스가 아닙니다.

---

## 대규모 FAB 시뮬레이션 성능 테스트

GigaRoute Auto Simulation의 대규모 반도체 FAB 레이아웃 성능 테스트에서는 다음 조건을 사용했습니다.

- 7,354 graph nodes
- 8,655 edges
- 2,066 stations
- 500 autonomous vehicles
- 8,000 moves/hour
- 시뮬레이션 시간 2시간

전체 2시간 시뮬레이션은 약 7분에 완료되어 약 17배의 실시간 대비 속도를 기록했습니다.

테스트 환경은 8 GB RAM, 내장 그래픽을 사용하는 일반 노트북이었습니다. 전체 실행 동안 vehicle following, 가감속, merge control, job assignment, station reservation, traffic recovery를 처리하면서 시스템 전체 gridlock 없이 완료되었습니다.

<img width="1280" height="579" alt="image" src="https://github.com/user-attachments/assets/4ac90bb8-f133-4be7-be75-7fb334fe5284" />

현재도 CPU 사용률과 로깅 비용 측면에서 추가 최적화 여지가 있으며, 다음 목표는 1,000 → 2,000 → 3,000대 Vehicle 규모까지 시뮬레이션 성능과 메모리 효율, 대규모 트래픽 안정성을 지속적으로 개선하는 것입니다.

GigaRoute AI  
대규모 자율 물류 시스템을 위한 시뮬레이션.
