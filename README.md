# DPO_RT5572_LinuxSTA_2.6.1.3_20121022

Slightly modified vendor driver:
- `HAS_WPA_SUPPLICANT=y`
- `HAS_NATIVE_WPA_SUPPLICANT_SUPPORT=y`
- `-Wno-error=date-time`
- `CHIPSET=5370`
- no `-DDBG`, modified `sta/sta-cfg.c` (according to http://ubuntuforums.org/showthread.php?t=2118379&page=3&p=12562670#post12562670)
- modified `rt_linux.h` (according to http://unix.stackexchange.com/a/158032)

```
sudo make
sudo make install
sudo modprobe rt5572sta # why not rt2870/rt5730? idk, CHIPSET var changes nothing..
```
