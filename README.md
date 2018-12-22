# PCM-Installer

[![AppVeyor](https://img.shields.io/appveyor/ci/Silvenga/pcm-installer.svg?logo=appveyor&maxAge=3600&style=flat-square)](https://ci.appveyor.com/project/Silvenga/pcm-installer)
[![License](https://img.shields.io/github/license/silvenga/pcm-installer.svg?maxAge=86400&style=flat-square)](https://github.com/Silvenga/pcm-installer/blob/master/LICENSE)

Intel Performance Monitoring (PCM) Installer. This project provides MSI packaging for the [PCM project](https://github.com/opcm/pcm). The PCM project depends on several compiled and signed drivers:

- WinPMem
- WinRing0

This project includes these binaries, based on the recomeneded sources from the PCM project. More information can be found in the `vendor` directory.

## Installation

Packaged releases can be found on the [releases page](https://github.com/Silvenga/PCM-Installer/releases) or from the build server. Standard MSI flags are supported, e.g. `/qn` for silent installations.

> Requires `Microsoft Visual C++ 2015 Redistributable (x64)` or the PCM service will fail to start (which will cause the installer to fail and rollback).

## Usage

The primary purpose of the PCM service is to provide performance counters. A full list of these counters can be found below:

```
\PCM Core Counters(*)\Clockticks
\PCM Core Counters(*)\Instructions Retired
\PCM Core Counters(*)\L2 Cache Misses
\PCM Core Counters(*)\L3 Cache Misses
\PCM Core Counters(*)\Instructions Per Clocktick (IPC)
\PCM Core Counters(*)\Relative Frequency (%)
\PCM Core Counters(*)\Thermal Headroom below TjMax
\PCM Core Counters(*)\core C0-state residency (%)
\PCM Core Counters(*)\core C3-state residency (%)
\PCM Core Counters(*)\core C6-state residency (%)
\PCM Core Counters(*)\core C7-state residency (%)
\PCM QPI Counters(*)\QPI Link Bandwidth
\PCM Socket Counters(*)\Memory Read Bandwidth
\PCM Socket Counters(*)\Memory Write Bandwidth
\PCM Socket Counters(*)\Package/Socket Consumed Energy
\PCM Socket Counters(*)\DRAM/Memory Consumed Energy
\PCM Socket Counters(*)\package C2-state residency (%)
\PCM Socket Counters(*)\package C3-state residency (%)
\PCM Socket Counters(*)\package C6-state residency (%)
\PCM Socket Counters(*)\package C7-state residency (%)
```

The other PCM binaries can be found in the `C:\Program Files\Processor Counter Monitor` directory.