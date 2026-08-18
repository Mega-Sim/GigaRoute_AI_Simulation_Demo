# GigaRoute AI — Linux Native Preview

[English](README.md) | [한국어](README_KO.md) | [简体中文](README_ZH.md) | **日本語**

**Ubuntu 22.04 x86_64 環境で Linux ネイティブ実行を確認済みです。**

GigaRoute Auto Simulation はクロスプラットフォームのシミュレーション製品として公開準備を進めています。現在の Public Preview では Linux ネイティブのスタンドアロン配布パッケージを提供しています。

## Quick Start — 何をダウンロードすればよいですか？

### 1. プログラムは GitHub Release からダウンロード

**Linux Release:** https://github.com/Mega-Sim/GigaRoute_AI_Simulation_Demo/releases/tag/public-preview-526-linux

Release ページ下部の **Assets** から次のファイルをダウンロードしてください。

`GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz`

> **`Source code (zip)` / `Source code (tar.gz)` は GigaRoute の実行プログラムではありません。** GitHub が自動生成する公開 Demo リポジトリのスナップショットです。

同梱の `.sha256` ファイルでダウンロードしたアプリケーションパッケージの整合性を確認できます。

### 2. サンプル DXF は Repository から別途ダウンロード

**サンプルレイアウト:** [`Sample/Layout_Example.dxf`](Sample/Layout_Example.dxf)

サンプルレイアウトは Release のアプリケーションパッケージとは別に Repository の `Sample/` フォルダで管理しています。上記ファイルリンクを開き、**Download raw file** で `Layout_Example.dxf` をローカルに保存してください。

### 3. プログラムを実行

```bash
tar -xzf GigaRoute-Auto-Simulation-Demo-Linux-x86_64.tar.gz
cd GigaRoute-Auto-Simulation-Demo
chmod +x run_gigaroute.sh
./run_gigaroute.sh
```

起動後：

**Open Layout → 別途ダウンロードした `Layout_Example.dxf` を選択 → Simulation を実行。**

### ダウンロード先の要約

- **アプリケーション:** GitHub **Releases / Assets のみ**からダウンロード
- **サンプル DXF:** Repository の **`Sample/` フォルダ**からダウンロード
- **GitHub Source code 圧縮ファイル:** アプリケーションのダウンロードファイルではありません

検証環境:

- Ubuntu 22.04 x86_64
- GCC 11.x
- Native C++/Qt6 実行ファイル
- Qt runtime を同梱した source-free Public Preview パッケージ

これは GigaRoute Auto Simulation のネイティブ Linux ビルドであり、ブラウザ Demo や Windows 実行ファイルをエミュレーションで動かすものではありません。

**Public Preview 状態**

| プラットフォーム | 状態 |
|---|---|
| Ubuntu 22.04 x86_64 | Public Preview リリース提供中 |
| Windows x64 | Public package 準備中 |

## セキュリティ / 配布

- Linux package には GigaRoute の C/C++ ソースコードを含みません。
- Public build では application QML の元ソースが顧客向け実行ファイルにそのまま含まれないように処理します。
- Debug symbol、object file、static/import library、private build path などの開発成果物は release audit で除外されます。
- 公開 Demo DXF には整理済みのサンプルレイアウトのみを含めます。
- ダウンロード後は同梱の `.sha256` ファイルで TGZ の整合性を確認できます。

> GitHub Release に自動表示される `Source code (zip)` / `Source code (tar.gz)` は、この **公開 Demo リポジトリのスナップショット**です。private `Sim_Core` ソースリポジトリではありません。

---

## 大規模 FAB シミュレーション性能テスト

GigaRoute Auto Simulation の大規模半導体 FAB レイアウト性能テストでは、以下の条件を使用しました。

- 7,354 graph nodes
- 8,655 edges
- 2,066 stations
- 500 autonomous vehicles
- 8,000 moves/hour
- シミュレーション時間 2 時間

2 時間分のシミュレーション全体は約 7 分で完了し、実時間比で約 17 倍の速度を記録しました。

テスト環境は 8 GB RAM / 内蔵グラフィックスの一般的なノート PC です。実行中は vehicle following、加減速、merge control、job assignment、station reservation、traffic recovery を継続的に処理しながら、システム全体の gridlock なしで完了しました。

<img width="1280" height="579" alt="image" src="https://github.com/user-attachments/assets/4ac90bb8-f133-4be7-be75-7fb334fe5284" />

CPU 使用率、ログ処理、並列化の面ではまだ最適化余地があります。次の目標は 1,000 → 2,000 → 3,000 台の Vehicle に対応しながら、シミュレーション速度、メモリ効率、大規模トラフィック安定性をさらに改善することです。

GigaRoute AI  
大規模自律搬送システム向けシミュレーション。
