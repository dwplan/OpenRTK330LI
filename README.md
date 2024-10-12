# Quick start of using OpenRTK330LI EVK for RTK and INS

The EVK hosts the main positioning module OpenRTK330LI with built-in GNSS RTK and INS functions. It features:
-   Multi-constellation dual-frequency (L1/L2) GNSS satellite signals
-   1 Hz RTK solution and 100 Hz INS PVA solution
-   10 HZ RTCM data and 100 HZ IMU data output
-   Rich peripheral interfaces
-   ...

## Prerequisites

### Hardware
- GNSS multi-frequency antenna with SMA interfaces
- Micro-USB cable
- Laptop
- RJ45 cable
- (Optional) 12V DC adapter
  
### Software
- [ans-devices.exe](https://github.com/Aceinna/python-openimu/releases/tag/v2.7.0) v2.7.0 
- (OR) [strsvr](https://github.com/rtklibexplorer/RTKLIB/releases) from RTKLIB
- (Optional) NTRIP caster [SNIP](http://rtk2go.com/) by rtk2go

### RTK correction service
Choose one of these open/commercial services and use the NTRIP conredentials provided:
- [rtk2go](http://rtk2go.com/)
- [CentipedeRTK](https://docs.centipede.fr/)
- [Geodnet](https://geodnet.com/)
- [Onocoy](https://console.onocoy.com/explorer)
- [RTK Direct](https://rtkdirect.com/)
- etc...

Or use your own base station with a NTRIP caster 
- OpenRTK330LI EVK (configure it into a base station that will be described in another section of this text)
- [rtkbase](https://github.com/Stefal/rtkbase) by Stefal


## Go for RTK positioning

### Connect
As desribed by the photo below: 
- usb to laptop for power and UART data io
- Ethernet to receive RTK correction or base station RTCM data
![alt text](/doc/img/connect.jpg)


### Operation
Follow the steps in the [manual](https://openrtk.readthedocs.io/en/latest/useOpenRTK/On-a-PC.html) for the RTK operations and data logging/parsing. 

Note the RTK positioing succeed if all three colored mini LEDs are blinking:
- Left yellow LED: GNSS signal valid
- Middle red LED: RTK correction received and valid
- Right green LED: GNSS positioning valid