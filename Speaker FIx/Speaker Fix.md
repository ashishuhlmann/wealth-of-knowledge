Fix your speaker firmware on Kernel 6 and 7.
![[volume.png|700]]
![[output.png|700]]
## Specs

**Dell Inc. XPS 9640**
- 22x Intel® Core™ Ultra 7 Processor 155H (16-Core, 24MB Cache, up to 5.0 GHz)
- 32 GB: LPDDR5X, 6400 MT/s (onboard)
- NVIDIA GeForce RTX 4050 Laptop GPU
- 1 TB, M.2 2280, PCIe NVMe Gen4, SSD

**Pop! OS 22.04 LTS**
- 64-bit
- GNOME 42.9
- X11 Windowing
## The Solution

1. Check audio hardware.
```bash
lspci -v | grep -A6 Audio
```
```
0000:00:1f.3 Audio device: Intel Corporation Device 7e28 (rev 20) (prog-if 80)
	Subsystem: Dell Device 0c63
	Flags: bus master, fast devsel, latency 64, IRQ 16, IOMMU group 21
	Memory at 5a2d310000 (64-bit, non-prefetchable) [size=16K]
	Memory at 5a2d000000 (64-bit, non-prefetchable) [size=2M]
	Capabilities: <access denied>
	Kernel driver in use: sof-audio-pci-intel-mtl
```

2. Search for **Sound Open Firmware** (SOF) messages in the **kernel ring buffer**:
```bash
sudo dmesg | grep -i sof
```
- This should return something like
```
[   22.672615] sof-audio-pci-intel-mtl 0000:00:1f.3: SOF firmware and/or topology file not found.
[   22.672618] sof-audio-pci-intel-mtl 0000:00:1f.3: Supported default profiles
[   22.672619] sof-audio-pci-intel-mtl 0000:00:1f.3: - ipc type 1 (Requested):
[   22.672620] sof-audio-pci-intel-mtl 0000:00:1f.3:  Firmware file: intel/sof-ipc4/mtl/sof-mtl.ri
[   22.672621] sof-audio-pci-intel-mtl 0000:00:1f.3:  Topology file: intel/sof-ipc4-tplg/sof-mtl-cs42l43-l0-cs35l56-l23.tplg
[   22.672621] sof-audio-pci-intel-mtl 0000:00:1f.3: Check if you have 'sof-firmware' package installed.
[   22.672622] sof-audio-pci-intel-mtl 0000:00:1f.3: Optionally it can be manually downloaded from:
[   22.672622] sof-audio-pci-intel-mtl 0000:00:1f.3:    https://github.com/thesofproject/sof-bin/
[   33.801644] sof-audio-pci-intel-mtl 0000:00:1f.3: error: sof_probe_work failed err: -2

```

On Kernel 6, it will probably show a different location for the topology file.
```
[   22.672621] sof-audio-pci-intel-mtl 0000:00:1f.3:  Topology file: intel/sof-ace-tplg/sof-mtl-cs42l43-l0-cs35l56-l23.tplg
```

3. Go to `user/lib/firmware`. Ensure the firmware file is correctly within `intel/sof-ipc4/mtl/sof-mtl.ri`. Then, notice the missing topology file in `intel/sof-ipc4-tplg/sof-mtl-cs42l43-l0-cs35l56-l23.tplg` (or `intel/sof-ace-tplg/sof-mtl-cs42l43-l0-cs35l56-l23.tplg` on Kernel 6).

4. Go to the [sof-bin](https://github.com/thesofproject/sof-bin.git), and download the missing files/directories. Add them to the correct locations above. The directories `sof-ipc4-tplg` or `sof-ace-tplg` may not already exist on the computer. If this is the case, download them from the version 2.14 directory and move them into `intel`. If the folders do exist, simply copy the missing toplogy file. If there isn't an exact match for the name of the topology file from the Github repository, just find the closest one and rename it to whatever the terminal output was.

5. Restart the computer.

```bash
sudo alsactl init
```

https://github.com/alsa-project/alsa-ucm-conf/tree/master

