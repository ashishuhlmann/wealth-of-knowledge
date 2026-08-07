Fix your speaker firmware on Kernel 6.

**Dell Inc. XPS 9640**
- 22x Intel® Core™ Ultra 7 Processor 155H (16-Core, 24MB Cache, up to 5.0 GHz)
- 32 GB: LPDDR5X, 6400 MT/s (onboard)
- NVIDIA GeForce RTX 4050 Laptop GPU
- 1 TB, M.2 2280, PCIe NVMe Gen4, SSD

**Pop! OS 22.04 LTS**
- 64-bit
- GNOME 42.9
- X11 Windowing

1. Check audio hardware.
```bash
lspci -v | grep -A6 Audio
```

2. Check **Sound Open Firmware** (SOF) messages:
```bash
sudo dmesg | grep -i sof
```
- This should return something like
```bash
  SOF firmware and/or topology file not found.
  Supported default profiles
  - ipc type 1 (Requested):
  Firmware file: intel/sof-ipc4/mtl/sof-mtl.ri
  Topology file: intel/sof-ipc4-tplg/sof-mtl-cs42l43-l0-cs35l56-l23.tplg
  Check if you have 'sof-firmware' package installed.
  Optionally it can be manually downloaded from:
  https://github.com/thesofproject/sof-bin/
  error: sof_probe_work failed err: -2
```
- Check if the firmware or topology file is missing in `user/lib/firmware`.

3. Go to the [sof-bin](https://github.com/thesofproject/sof-bin.git), and download the missing topology files. Add them to the locations above.

4. Restart the computer.

```bash
sudo alsactl init
```

https://github.com/alsa-project/alsa-ucm-conf/tree/master

