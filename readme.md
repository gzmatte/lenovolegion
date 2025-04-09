# Unlock Hidden BIOS Settings & Unbrick Lenovo Legions BIOS (2025)
* This is a personal guide that i created for myself and to help others with the same problems i had.
* I'm using a LENOVO LEGION 5 15ACH6A for reference, but should be the same in others.

-------------


## ADVANCED BIOS SETTINGS
Usually Hidden BIOS Settings should appear with a key combination, this laptop doesn't.
So we gonna use a USB Pendrive in order to force-it.

- First, download the bootable iso. [DOWNLOAD](https://github.com/Thomashighbaugh/Lenovo-Legion-Advanced-Bios/releases/download/v0.0.1/lenovo_legion_advanced_bios.iso)  [MIRROR](https://github.com/gzmatte/lenovolegion/releases/download/1/lenovo_legion_advanced_bios-backup.iso)

- Now, install it to your pendrive via [RUFUS](https://github.com/pbatard/rufus/releases/download/v3.18/rufus-3.18.exe)

- Once ready, restart to your BIOS and check that you have enabled USB BOOT and Disable "Secure Boot" in order to use the pendrive.

- Now restart your PC and spam F9 in order to enter boot menu, select your pendrive and it should redirect you to the BIOS with more settings enabled. That's it!
+


BIOS EXPLAINED FOR PERFORMANCE

### CONFIGURATION
WIRELESS LAN - Enables WiFi, Disable in case u are on Ethernet.
GRAPHICS DEVICE > DISCRETE GRAPHIC - Discrete uses your dedicated GPU, use this ALWAYS, if u need custom resolutions just use gpu scaling.
UMA BUFFER > 512M - Leave it low but if you select dGPU this will not do anything.
VT / VM > VIRTUALIZATION, REQUIRED FOR EMULATORS OR HVCI (VALORANT/FACEIT), if you don't use anything of that, disable it.
ALWAYS ON USB > OFF, NOT REQUIRED.

### ADVANCED
PCI EXPRESS CONFIGURATIONS > PSPP POLICY > Disabled.
PCIE RESIZABLE BAR > Enabled.

> PERIPHERAL CONFIGURATION
Azalia > Disabled.

> IDE CONFIGURATION
SATA - Disable if you only have NVME.
SATA Controller - Disable All SATA Ports if you only have NVME.

> VIDEO
HDMI Audio - This disables HDMI Audio & Internal Speakers, disable if u don't need speakers on your laptop.

> CHIPSET CONFIGURATION
PCI Latency Timer - 32 should be default, sometimes 64. You can try 128, YOU NEED TO TEST FPS AND LATENCY WITH THIS SETTING.
STIBP Status - Should be disabled, if not; be careful this can brick.

> ACPI TABLE/FEATURES CONTROL
FACP C2 Latency > DISABLE
FACP C3 Latency > DISABLE
FACP - RTC S4 Wakeup > DISABLE
APIC - IO APIC Mode > DISABLE
HPET - HPET Support > DISABLE ONLY if you have a timer resolution or HPET disabled in Windows.

> CPU RELATED SETTINGS
DONT TOUCH ANYTHING ON LEGION 5 15ACH6, CAN BRICK.

> ABOVE 4G MMIO
ENABLE.

### POWER
Thermal Fan Control > DISABLE
Auto Wake on S5 > DISABLE
S5 Long Run Test > DISABLE

### BOOT
USB Boot > Disable if u are not going to use any pendrive to boot.

### AMD PBS
SSD POWER ENABLE > SSD x4
HDD POWER ENABLE > OFF if not using HDD
SPECIAL DISPLAY FEATURES > OFF
PRIMARY VIDEO ADAPTOR > EXT. GRAPHICS (PEG)
ACP POWER GATING > OFF
ACP CLOCK GATING > OFF
You can change more settings on this section, but be careful and test 1 by 1, this can brick your mother as it do with me.

### AMD CBS
> CPU COMMON OPTIONS
Performance > DO NOT PUT CUSTOM PCORES. THIS WILL BREAK YOUR BIOS! YOU WILL NEED TO REFLASH BIOS AND ITS NOT EASY AND MAYBE YOU BREAK IT AND CAN NEVER BE REPAIRED!

CORE WATCHDOG > DISABLE
CORE PERFORMANCE BOOST > ENABLE/AUTO
GLOBAL C-STATE CONTROL > OFF

> DRAM SETTINGS - DO NOT USE ANY FIXED MHZ, NOT TOUCH ANYTHING ON THE RAMS OR IT WILL BRICK YOUR BIOS.

**NBIO**
PSPP POLICY > DISABLE
XFR ENHANCEMENT > ACCEPT > PRECISION BOOST OVERDRIVE ENABLE

> SMU COMMON OPTIONS
SYSTEM TEMPERATURE TRACKING > DISABLED

> STAPM CONTROL - MANUAL
STAPM BOOST ENABLE.

> CPPC
CPPC PREFERRED CORES, TEST ENABLED OR DISABLE IT.

> FCH
SATA > DISABLE IF NOT USING SATA.
