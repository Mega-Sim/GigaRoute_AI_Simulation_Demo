# GigaRoute AI Simulation Demo — Linux

## Download

Download the current Linux Public Preview from GitHub Releases:

- [GigaRoute Auto Simulation Demo — Linux Public Preview](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/tag/public-preview-526-linux)
- [Direct download: Linux x86_64 TGZ](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/download/public-preview-526-linux/GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz)
- [SHA-256 checksum](https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/download/public-preview-526-linux/GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz.sha256)

## Demo layout

For the Public Preview, use the repository sample layout below:

- [Sample/Layout_Example.dxf](../Sample/Layout_Example.dxf)

After launching GigaRoute Auto Simulation, choose **Open Layout** and open `Layout_Example.dxf`.

The public sample is sanitized for distribution and contains only the supported LINE / ARC / TEXT / MTEXT entity classes required by the demo importer. Unnecessary author, timestamp, GUID, proxy and other private DXF metadata are not included.

## Run

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

Then open the downloaded repository sample `Sample/Layout_Example.dxf` from **Open Layout**.

The package includes the GigaRoute executable and the required bundled Qt runtime.

## Security / distribution

- GigaRoute C/C++ source code is **not** included in the Linux package.
- Application QML source is discarded from the customer binary during the hardened public build.
- Debug symbols, object files, static/import libraries, private build paths, and other development artifacts are excluded by the release audit.
- `Sample/Layout_Example.dxf` is the designated public demo layout.
- Verify the downloaded TGZ against the accompanying `.sha256` file before use.

> GitHub automatically displays `Source code (zip)` and `Source code (tar.gz)` for every tagged release. Those archives contain only this **public demo repository snapshot**; they are not archives of the private `Sim_Core` source repository.
