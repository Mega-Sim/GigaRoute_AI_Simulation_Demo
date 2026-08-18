# GigaRoute AI — Linux Native Preview

**Native Linux execution is now verified on Ubuntu 22.04 x86_64.**

GigaRoute Auto Simulation is being prepared as a cross-platform simulation product. While the Windows public package is still being prepared, the current Public Preview has now been built and launched successfully as a native Linux executable.

Verified environment:

- Ubuntu 22.04 x86_64
- GCC 11.x
- Qt 6.8.3 (`gcc_64`)
- Release build
- Native C++/Qt6 executable

Latest Linux build result:

```text
[52/52] Linking CXX executable gigaroute_qt
```

Launch command used for the verified build:

```bash
./build/public-preview-526/gigaroute_qt
```

This is a native Linux build of the same GigaRoute Auto Simulation product path — not a browser demo and not a Windows executable running through an emulation layer.

The Linux release path will continue to be maintained alongside Windows. The current verified preview uses a Qt 6.8.x runtime environment; a standalone Linux distribution bundle will be published as the packaging work is completed.

**Public Preview status**

| Platform | Status |
|---|---|
| Ubuntu 22.04 x86_64 | Native build and launch verified |
| Windows x64 | Public package in preparation |
| Standalone Linux bundle | Packaging in progress |

---

## Large-Scale FAB Simulation Performance Test

We are currently preparing GigaRoute Auto Simulation for its official release, and today I tested the simulation engine on a large semiconductor FAB layout using a standard laptop environment.

The simulation model included:

* 7,354 graph nodes
* 8,655 edges
* 2,066 stations
* 500 autonomous vehicles
* 8,000 moves/hour
* 2 hours of simulated operation

The full 2-hour simulation completed in approximately 7 minutes, achieving roughly 17× real-time simulation speed.

What makes this result particularly meaningful is the test environment:

8 GB RAM / integrated graphics / standard laptop

The simulation also completed without a system-wide traffic gridlock during the full 2-hour run, while continuously handling vehicle following, acceleration/deceleration, merge control, job assignment, station reservations, and traffic recovery.

<img width="1280" height="579" alt="image" src="https://github.com/user-attachments/assets/4ac90bb8-f133-4be7-be75-7fb334fe5284" />

And there is still significant room for optimization.

During this test, CPU utilization remained around 30–40%, while detailed simulation logging was enabled. The current engine is therefore not yet operating near its final performance ceiling.

The next targets for GigaRoute AI are clear:

1,000 → 2,000 → 3,000 vehicles

while continuing to improve simulation speed, memory efficiency, and large-scale traffic stability.

The goal is to make large-scale material handling and autonomous vehicle simulation accessible without requiring high-end workstation hardware.

GigaRoute AI  
Simulation for large-scale autonomous material handling systems.

#GigaRouteAI #Simulation #DigitalTwin #Semiconductor #SmartFactory #AMHS #OHT #AutonomousVehicles #Manufacturing #PhysicalAI #SoftwareEngineering #Linux
