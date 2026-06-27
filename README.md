# barebone-windows

## ⚡ Minimalist Legacy OS Archives

An open-source repository dedicated to stripping down legacy Windows installation media to their absolute core system binaries. This project bypasses 1990s web-integration bloat, defunct ISP software, and marketing telemetry to achieve the smallest possible disk footprint for emulation (VMware Only For Now) and legacy old machines.

---

# Screenshots

<img width="742" height="520" alt="image" src="https://github.com/user-attachments/assets/9a214906-5dc6-48eb-a091-b878c4c8e842" />

Windows 95 Ultimate Barebone - 56.1MB

<img width="704" height="534" alt="win2kbbstd" src="https://github.com/user-attachments/assets/9d37a7c2-817f-408f-8eae-e9dbcab25f88" />

Windows 2000 Standard Barebone - 349MB

<img width="820" height="622" alt="winxpsp3bbstd" src="https://github.com/user-attachments/assets/383f69b4-1594-40d2-81eb-0b66c21b91ea" />

Windows XP PRO SP3 Standard Barebone - 377MB - ISO SIZE ~217MB

---

## 🎯 Project Highlights: Windows 95 OSR2
* **Original ISO Size:** 592 MB ➔ **Optimized ISO Size:** 50.6 MB (91.4% reduction!)
* **Out-of-the-Box C: Drive Footprint:** 56.1 MB (Clean, lightweight FAT32 structure)
* **Idle RAM Utilization:** ~4 MB or Might be ~2 MB

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

---

## 🎯 Project Highlights: Windows 2000 Professional SP4
* **Original ISO Size:** 363 MB ➔ **Optimized ISO Size:** 160.5 MB (55.7% reduction!)
* **Out-of-the-Box C: Drive Footprint:** 349 MB (Includes a customized 32-64MB memory heap fallback cache)
* **Status Profile:** Standard Barebone (Retains standard physical driver support layers, Microsoft Paint, 3D Pinball Space Cadet, and MS Agent character libraries)

PLEASE NOTE THAT THE CUSTOMIZED PAGE FILE SIZE IS ONLY AVAILABLE TO THE VMWARE USERS , AND ALSO TO GET THE SPACE LOW , WE HAVE TO UNCHECK THE INDEXING FILES IN THE PROPERTIES OF THE C: DRIVE AND CHECK COMPRESS THIS DISK TO LOWER THE SPACE USED.

---

## 🛠️ Windows 2000 Professional Slim Architecture Blueprints

### Step 1: Structural Extraction Layer
Extract your pristine Windows 2000 SP4 ISO into a working directory on your host desktop. Ensure the core `I386` directory layer sits right alongside its companion master CD identification files (`CDROM_IP.5`, `CDROM_NT.5`, etc.) to clear administrative validation checks inside the compiler engine.

### Step 2: Surgical Component Extraction Matrices
Fire up classic **nLite v1.4.9.3**, target your workspace directory, and execute these targeted purging parameters across the task selection grid columns:
* **Languages**: Complete global purge (Deletes all international font families and translation modules except English, instantly carving out ~40-50MB of system weight).
* **Directories**: Wipe `BOOTDISK`, `DISCOVER` (system tour logs), `SUPPORT`, and `VALUEADD` subfolders entirely from the root image map.
* **Multimedia**: Clean out bulky legacy Windows Media Player bundles, sound schemes, and sample image data caches while safely maintaining core `DirectX` and `OpenGL Support` vectors.
* **Services & Performance**: Toggle automatic file logging trackers off. Check `Indexing Service`, `Remote Registry`, `Fax Service`, and corporate `Kerberos KDC` background servers for complete removal to prevent active storage latency cycles.

### Step 3: Product Key
Because Windows 2k errors out in installation , we have to give it a different product key , so after clicking "ok" 2 times , enter this product key - 
`DDTPV-TXMX7-BBGJ9-WGY8K-B9GHM`

---

### Step 4: Storage Optimization Post-Install Fix
Once the automated graphical text installer boots you into the live desktop space, perform these two manual steps to shrink the final partition blocks down to the **349 MB record floor**:
1. Open **My Computer** ➔ Right-click **C: Drive Properties** ➔ Check **"Compress drive to save disk space"** and click Apply.
2. Right-click **My Computer** ➔ **Properties** ➔ **Advanced** ➔ **Performance Options** ➔ **Virtual Memory Change**. Drop your active `pagefile.sys` allocation down to an Initial of **32 MB** and a Maximum of **64 MB**, click **Set**, and perform a single system reboot sequence.

---
---

## 🎯 Project Highlights: Windows XP Professional SP3
* **Original Microsoft ISO Footprint:** 589 MB ➔ **Surgically Shrunk ISO Size:** 217 MB (A massive 63% reduction!)
* **Live Installation Record Footprint:** **377 MB on the C: Drive** (Achieved by running a localized filesystem compression and structuring a 32–64MB memory heap fallback cache).
* **Aesthetic & Usability Profile:** 100% Authentic. Fully retains the iconic blue-and-green Luna desktop theme, default background wallpapers, and welcome screen interfaces. 
* **Nostalgic Features Preserved:** 3D Pinball Space Cadet, Microsoft Paint, Calculator, WordPad, and MS Agent animation libraries are completely intact and fully functional out of the box.

---

## 🛠️ Windows XP SP3 Standard Barebone Customization Matrix

### Step 1: Structural Extraction Layer
1. Download a clean, uncompressed Windows XP SP3 Volume License (VLK) ISO.
2. Extract the full ISO root structure into a working directory on your host desktop named `WinXP_Master`. Ensure all companion verification files sitting right alongside the `I386` folder are extracted cleanly to bypass nLite directory verification checks.

### Step 2: Component Slicing Configuration (Inside nLite)
Launch classic **nLite v1.4.9.3**, point it to your desktop `WinXP_Master` folder, and check these targeted parameters across the task selection grid rows:
* **Languages & Fonts:** Complete global extraction of all foreign translation dictionaries and localized font asset layout tables except English, immediately slicing out ~60-80MB of disc weight.
* **Multimedia Overhead:** Stripped out heavy movie production engines (Movie Maker), generic speech-to-text engines, Tablet PC handwriting extensions, and sample music caches. Safely preserved core `DirectX`, `OpenGL Support`, and `MIDI Audio` pipelines to guarantee fluid 3D legacy gaming performance.
* **Network Components:** Purged ancient dial-up/MSN Explorer packages, corporate server platforms (IIS), FrontPage links, and the experimental legacy IPv6 framework to keep standard IPv4 network file sharing lightweight and responsive.
* **Services & Diagnostics:** Checked `Indexing Service`, `Remote Registry`, `Error Reporting`, and corporate `Kerberos KDC` background engines for complete removal to prevent active storage read/write latency cycles.

### Step 3: Unattended Stream Realignment
Toggle the Unattended configuration variables to **Fully Automated**. Paste this master corporate deployment key directly into the configuration block to bypass manual text input pages during setup loops (this Volume License key completely cuts out Microsoft online activation requirements forever):
```text
TQMCY-42MBK-3R4YG-478KD-7FY3M
```

---

## 🚀 Post-Install Storage Optimization (The 377MB Fix)
Once the automated graphical installer drops you directly onto your fresh Luna desktop canvas, execute these two manual steps to shrink your final partition footprint from 1.39 GB down to your **377 MB record floor**:

1. **Enable NTFS Drive Compression**: Open **My Computer** ➔ Right-click your **C: Local Disk** and select **Properties** ➔ Check the box that says **"Compress drive to save disk space"** and uncheck **"Allow Indexing Service..."** ➔ Click **Apply** ➔ Select **"Apply changes to C:\, subfolders and files"** and hit OK. (Let the blue processing bar complete).
2. **Optimize the Virtual Memory Swap**: Right-click **My Computer** ➔ **Properties** ➔ **Advanced** tab ➔ Under *Performance*, click **Settings** ➔ **Advanced** tab ➔ Click **Change** under *Virtual Memory*. Highlight your **C:** drive, click **Custom size**, type exactly **32** for Initial and **64** for Maximum, then click **Set** (Crucial!). Click **OK** on all windows and trigger a single virtual machine reboot sequence.

---

# 🛠️ PreWare Utilities (Curated Retro Software Library)
An archive of verified, clean legacy applications and tools perfectly optimized to run flawlessly within your Barebone environments without bloating the file system.

### ⌨ 1. Essential Drivers For Performance

* VMware Tools 10.0.0 for Windows XP (VMware Exclusive)- *   **[VMware Tools v10.0.12 (Official Directory Target)](https://packages.vmware.com/tools/releases/10.0.12/windows/x86/)**: Broadcom officially maintains the legacy repository index endpoints for vintage guest operating systems. Open the official index pathway directory, select **`VMware-tools-10.0.12-4448496-i386.exe`**, and download the source package cleanly.
*   **[Alternative Pre-Vista ISO Mirror (Internet Archive)](https://archive.org)**: If you prefer mounting the complete system driver virtual disk directly into your virtual CD-ROM tray, you can fetch the public community archive mirror `winPreVista.iso`.

### 🌐 Old Web Browsers

### 🎮 2. Runtimes, Patches, & Gaming Support

### 🎬 3. Productivity & Legacy Media Playback

### 🕹️ 4. Verified Vintage Shareware Gaming Classics

---

## 💿 Downloads

Windows 95 OSR 2 Barebone Ultimate Bootable ISO - https://drive.google.com/file/d/1REI-wrLITSUdMf_cszWbS7PKIBR6F25x/view?usp=sharing

Windows 95 OSR 2 Ultimate Barebone VMware 17.5 or later - https://drive.google.com/file/d/1lh_ma6Gs_VnOlj6ZUMCIL-ZK8WO-LJKf/view?usp=sharing

Windows 2000 SP4 Standard Barebone Bootable ISO - https://drive.google.com/file/d/1qa16QhMfrkBMUs1OzEXEGN787b_Nudtk/view?usp=sharing

Windows 2000 SP4 Standard Barebone VMware Folder (Only VMware 12.x Or Later) - https://drive.google.com/file/d/1i1ekTwyiBF1svKZlvZvjiLgCgUmF4I8H/view?usp=sharing

Windows XP PRO SP3 Standard Barebone Bootable ISO - https://drive.google.com/file/d/1irgRRdyZwZ_uLO8aeN2ojLOkb6C8LYkJ/view?usp=sharing

Winodws XP PRO SP3 Standard Barebone VMware VM Folder (Only VMware 12.x Or Later) - https://drive.google.com/file/d/1tbL8Rb7ZFk74Pyvew-l-fi8IFuyfiFjn/view?usp=sharing

---

## 📜 License
Distributed under the **MIT License**. See `LICENSE` for more information.

