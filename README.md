# barebone-windows

## ⚡ Minimalist Legacy OS Archives

An open-source repository dedicated to stripping down legacy Windows installation media to their absolute core system binaries. This project bypasses 1990s web-integration bloat, defunct ISP software, and marketing telemetry to achieve the smallest possible disk footprint for emulation (VMware, VirtualBox, 86Box, PCem).

---

## 🎯 Project Highlights: Windows 95 OSR2
* **Original ISO Size:** 592 MB ➔ **Optimized ISO Size:** 50.6 MB (91.4% reduction!)
* **Out-of-the-Box C: Drive Footprint:** 56.1 MB (Clean, lightweight FAT32 structure)
* **Idle RAM Utilization:** ~6 MB to 10 MB

---

## 🛠️ Windows 95 OSR2 Automated Purge Blueprints

### Step 1: Automated Script Cleanup (Host PC)
Extract your untouched `WIN95` installation folder onto your modern Windows 11 desktop. Open **PowerShell** directly inside that directory and execute these targeted purge streams to strip the bloat:

```powershell
# Stream 1: Wipe Active Desktop, heavy language packs, and ISP configurations
Get-ChildItem -Include CHL*.CAB, IE4*.CAB, IELPK*.CAB, ICW*.CAB, PRO_*, MSGMS_*, MSMUS_*, CS3KIT.EXE, AOLSETUP.EXE, MSNSETUP.EXE, ATSETUP.EXE, MSAGENT.EXE, MSCHAT2.CAB, MSWALLET.CAB, NM21.CAB, PCVKIT.EXE, IR50_32.CAB, AMOVIE.CAB, ACTSETUP.CAB, HANDB*.CAB, OHRE.CAB, PINBALL.CAB, HOVER.CAB -Recurse | Remove-Item -Force -Verbose

# Stream 2: Purge 90s streaming plugins, IE4 setup wrappers, and default graphics logs
Get-ChildItem -Include AOL30*.EXE, IE4SETUP.*, IEJAVA.CAB, ISIGNUP.EXE, MAILNEWS.CAB, MSN251.EXE, R32MSIE4.EXE, SWDIR.CAB, SWFLASH.CAB, SWINST4.EXE, VDOLIVE.CAB, VRML2C.EXE, WB16OFF.EXE, WELCOME.EXE, CONTENT, AXA.CAB, WPIE4X86.CAB, SERVICES.TXT, README.TXT, AMOV4IE.CAB, JAVI386.CAB, NSIE4.CAB -Recurse | Remove-Item -Force -Verbose
```

### Step 2: Create a Single Bootable Master ISO (AnyBurn)
1. Launch **AnyBurn** and select **"Create image file from files/folders"**.
2. Add your ultra-lean **`WIN95`** folder compilation.
3. Click **More Ripper / Disc Tools** ➔ **"Add Boot Information"**.
4. Check **"Make image bootable"**, select your `Windows95b.img` floppy image file, and configure **Sectors to load** to exactly `4`.
5. Set output target string designation to standard `.ISO` format and build.

### Step 3: Installation & Kernel Bypass Switches
Mount your master ISO into your target virtual machine (unmount any separate virtual floppy disk hardware profiles). At the MS-DOS prompt (`A:\>`), run the initialize commands:

```text
A:\> fdisk                   # Select Y for Large Disk Support (FAT32) -> Create Primary Partition
[Restart Guest VM -> Boot from CD-ROM Track]
A:\> format c: /s            # Formats your C drive and copies core DOS booting flags
A:\> R:                      # Navigate to your active CD-ROM drive mapping
R:\> cd WIN95
R:\WIN95> setup /is /iq /id /iv
```

* **`/is` / `/iq`**: Completely bypasses legacy disk checking routines.
* **`/id`**: Bypasses total folder validation disk checks, forcing setup to look only at core items.
* **`/iv`**: Eliminates promotional marketing presentation billboards during file copying.
* *Crucial Selection:* When prompted by the graphical wizard layout, ensure you choose **Compact Setup** to finalize the barebone environment.

## Downloads

Windows 95 OSR 2 Barebone - [Download Here] https://drive.google.com/file/d/1REI-wrLITSUdMf_cszWbS7PKIBR6F25x/view?usp=sharing

---

## 📜 License
Distributed under the **MIT License**. See `LICENSE` for more information.

