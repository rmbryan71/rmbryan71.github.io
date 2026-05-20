---
layout: post
title: The Rig
date: 2026-05-20
categories: dsp, hardware
excerpt: Current tooling
---
This is the gear I use to study [digital signal processing](/articles/digital-signal-processing.htm):
1. [YouLoop single-loop passive magnetic loop antenna](https://www.rtl-sdr.com/product/youloop-portable-passive-magnetic-loop-antenna/)
2. [Airspy HF+ Discovery HF/VHF receiver](https://airspy.com/airspy-hf-discovery/)
3. A standard-issue MacBook Pro from 2019
4. A standard-issue WiFi router from 2017
5. Machine-zero, which is:

**Chassis**:  Dell Precision 3630 tower bought used on eBay from e-CyclePro in Lecanto, FL.

**Motherboard**
- Dell OEM (Precision 3630)
- Socket: LGA1151 (8th/9th gen Intel)
- Chipset: Intel C246 (workstation)
- RAM slots: 4× DDR4 DIMM
![The motherboard](/assets/mobo.jpeg)

**CPU** _(stock, although I did remove the fan, clean the heat-sink and apply fresh thermal paste)_
- Intel Core i7-8700K
- 6 cores / 12 threads
- 3.70 GHz

<div style="display: flex; gap: 10px;"> 
<img src="/assets/dirty-cpu.png" alt="A dirty cpu" style="width: 50%;"> 
<img src="/assets/clean-cpu.png" alt="A clean cpu" style="width: 50%;"> 
</div>

**RAM** _(stock, not replaced)_
- 32GB DDR4 2666MT/s dual channel
- 2× 16GB Micron Technology 16ATF2G64AZ-2G6E1
- Confirmed by memtest86
![Memtest86 pass screen](/assets/pass-memtest.png)

**PSU** _(replaced — stock Dell 300W wasn't big enough for the GPU)_
- Seasonic CORE GX 650W ATX 3.1, 80+ Gold, Fully Modular
- Connectors: 24-pin ATX, 8-pin EPS CPU, 2× 8-pin PCIe

**Storage** _(bought new)_: Kingston NV3 1TB NVMe PCIe 4.0

**GPU** _(used, won in an auction on eBay)_
- MSI GeForce RTX 3060 Ventus 2X OC 12GB GDDR6
- Model number: **912-V397-050**
- 12GB GDDR6 / 12288 MiB
- Dual fan (Torx 3.0)
- Stress test: PASS — gpu-burn 15 min, 0 errors, max temp 78°C, ~9,211 Gflop/s
![GPU installed in the chassis](/assets/gpu.jpeg)