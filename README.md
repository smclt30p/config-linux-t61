#Linux/x86 4.6.2 Kernel Configuration

 * Vendor: Lenovo
 * Model: T61 
 * Motherboard: 64576PG
 * BIOS: Middleton 2.29-1.08 (7LETC9WW 2.29 03/18/2011)
 * CPU: Core2 Family (Penryn) 
 * GPU: NVIDIA G86M [Quadro NVS 140M] 
 * Audio: Intel 82801H (ICH8 Family) HD Audio ControllerA
 * Audio codec: Analog Devices AD1984 
 * Ethernet: Intel 82566MM Gigabit Network Controller
 * Wireless: Intel PRO/Wireless 4965AG 
 * Bluetooth: Broadcom Corp. BCM2045B (BDC-2) 
 * Biometrics: STMicroelectronics 
 * SD Host Controller: Ricoh R5C822 SD/SDIO/MMC/MS/MSPro
 * IEEE 1394: Ricoh Co Ltd R5C832
 * CardBus: Ricoh Co Ltd RL5c476 II (rev ba)
 * SATA Controller: Intel Corporation 82801HM/HEM (ICH8M/ICH8M-E) [AHCI] 
 * Card Reader: Ricoh R5C822 + xD-Picture reader 
 
# Build command line:

```
make -j 3 CFLAGS="$CFLAGS -O3"
```
 

# Additional variable hardware:
 
 * SSD: KINGSTON SHFS37A/120G
 * CD/DVD: MATSHITA UJ-842

-----------

 * lspci

```
00:00.0 Host bridge: Intel Corporation Mobile PM965/GM965/GL960 Memory Controller Hub (rev 0c)
00:01.0 PCI bridge: Intel Corporation Mobile PM965/GM965/GL960 PCI Express Root Port (rev 0c)
00:19.0 Ethernet controller: Intel Corporation 82566MM Gigabit Network Connection (rev 03)
00:1a.0 USB controller: Intel Corporation 82801H (ICH8 Family) USB UHCI Controller #4 (rev 03)
00:1a.1 USB controller: Intel Corporation 82801H (ICH8 Family) USB UHCI Controller #5 (rev 03)
00:1a.7 USB controller: Intel Corporation 82801H (ICH8 Family) USB2 EHCI Controller #2 (rev 03)
00:1b.0 Audio device: Intel Corporation 82801H (ICH8 Family) HD Audio Controller (rev 03)
00:1c.0 PCI bridge: Intel Corporation 82801H (ICH8 Family) PCI Express Port 1 (rev 03)
00:1c.1 PCI bridge: Intel Corporation 82801H (ICH8 Family) PCI Express Port 2 (rev 03)
00:1c.2 PCI bridge: Intel Corporation 82801H (ICH8 Family) PCI Express Port 3 (rev 03)
00:1c.3 PCI bridge: Intel Corporation 82801H (ICH8 Family) PCI Express Port 4 (rev 03)
00:1c.4 PCI bridge: Intel Corporation 82801H (ICH8 Family) PCI Express Port 5 (rev 03)
00:1d.0 USB controller: Intel Corporation 82801H (ICH8 Family) USB UHCI Controller #1 (rev 03)
00:1d.1 USB controller: Intel Corporation 82801H (ICH8 Family) USB UHCI Controller #2 (rev 03)
00:1d.2 USB controller: Intel Corporation 82801H (ICH8 Family) USB UHCI Controller #3 (rev 03)
00:1d.7 USB controller: Intel Corporation 82801H (ICH8 Family) USB2 EHCI Controller #1 (rev 03)
00:1e.0 PCI bridge: Intel Corporation 82801 Mobile PCI Bridge (rev f3)
00:1f.0 ISA bridge: Intel Corporation 82801HEM (ICH8M-E) LPC Interface Controller (rev 03)
00:1f.1 IDE interface: Intel Corporation 82801HM/HEM (ICH8M/ICH8M-E) IDE Controller (rev 03)
00:1f.2 SATA controller: Intel Corporation 82801HM/HEM (ICH8M/ICH8M-E) SATA Controller [AHCI mode] (rev 03)
00:1f.3 SMBus: Intel Corporation 82801H (ICH8 Family) SMBus Controller (rev 03)
01:00.0 VGA compatible controller: NVIDIA Corporation G86M [Quadro NVS 140M] (rev a1)
03:00.0 Network controller: Intel Corporation PRO/Wireless 4965 AG or AGN [Kedron] Network Connection (rev 61)
15:00.0 CardBus bridge: Ricoh Co Ltd RL5c476 II (rev ba)
15:00.1 FireWire (IEEE 1394): Ricoh Co Ltd R5C832 IEEE 1394 Controller (rev 04)
15:00.2 SD Host controller: Ricoh Co Ltd R5C822 SD/SDIO/MMC/MS/MSPro Host Adapter (rev 21)
15:00.4 System peripheral: Ricoh Co Ltd R5C592 Memory Stick Bus Host Adapter (rev 11)
15:00.5 System peripheral: Ricoh Co Ltd xD-Picture Card Controller (rev 11)
```

 * lsusb

```
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 007 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
Bus 006 Device 002: ID 17ef:1003 Lenovo Integrated Smart Card Reader
Bus 006 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
Bus 005 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 004 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
Bus 003 Device 003: ID 0483:2016 STMicroelectronics Fingerprint Reader
Bus 003 Device 002: ID 0a5c:2110 Broadcom Corp. BCM2045B (BDC-2) [Bluetooth Controller]
Bus 003 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
```
 * dmesg
```
[    0.000000] Linux version 4.6.2-t61 (gala@thinkpad) (gcc version 5.3.1 20160413 (Ubuntu 5.3.1-14ubuntu2.1) ) #5 SMP PREEMPT Sun Jun 19 23:33:16 CEST 2016
[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-4.6.2-t61 root=UUID=ba6e0f3e-b3e6-4293-b0b3-0ab5602dcda9 ro quiet splash vt.handoff=7
[    0.000000] x86/fpu: Legacy x87 FPU detected.
[    0.000000] x86/fpu: Using 'eager' FPU context switches.
[    0.000000] e820: BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009d7ff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009d800-0x000000000009ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000000d2000-0x00000000000d3fff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000000e0000-0x00000000000fffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x00000000beeaffff] usable
[    0.000000] BIOS-e820: [mem 0x00000000beeb0000-0x00000000beecbfff] ACPI data
[    0.000000] BIOS-e820: [mem 0x00000000beecc000-0x00000000beefffff] ACPI NVS
[    0.000000] BIOS-e820: [mem 0x00000000bef00000-0x00000000beffffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000f0000000-0x00000000f3ffffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fec00000-0x00000000fec0ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fed00000-0x00000000fed003ff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fed14000-0x00000000fed19fff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fed1c000-0x00000000fed8ffff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000fee00000-0x00000000fee00fff] reserved
[    0.000000] BIOS-e820: [mem 0x00000000ff000000-0x00000000ffffffff] reserved
[    0.000000] NX (Execute Disable) protection: active
[    0.000000] SMBIOS 2.4 present.
[    0.000000] DMI: LENOVO 64576PG/64576PG, BIOS 7LETC9WW (2.29 ) 03/18/2011
[    0.000000] e820: update [mem 0x00000000-0x00000fff] usable ==> reserved
[    0.000000] e820: remove [mem 0x000a0000-0x000fffff] usable
[    0.000000] e820: last_pfn = 0xbeeb0 max_arch_pfn = 0x400000000
[    0.000000] MTRR default type: uncachable
[    0.000000] MTRR fixed ranges enabled:
[    0.000000]   00000-9FFFF write-back
[    0.000000]   A0000-BFFFF uncachable
[    0.000000]   C0000-CFFFF write-protect
[    0.000000]   D0000-DFFFF uncachable
[    0.000000]   E0000-FFFFF write-protect
[    0.000000] MTRR variable ranges enabled:
[    0.000000]   0 base 0BF000000 mask FFF000000 uncachable
[    0.000000]   1 base 000000000 mask F80000000 write-back
[    0.000000]   2 base 080000000 mask FC0000000 write-back
[    0.000000]   3 base 0BEF00000 mask FFFF00000 uncachable
[    0.000000]   4 disabled
[    0.000000]   5 disabled
[    0.000000]   6 disabled
[    0.000000]   7 disabled
[    0.000000] x86/PAT: Configuration [0-7]: WB  WC  UC- UC  WB  WC  UC- WT  
[    0.000000] found SMP MP-table at [mem 0x000f68f0-0x000f68ff] mapped at [ffff8800000f68f0]
[    0.000000] Scanning 1 areas for low memory corruption
[    0.000000] Base memory trampoline at [ffff880000097000] 97000 size 24576
[    0.000000] BRK [0x0206b000, 0x0206bfff] PGTABLE
[    0.000000] BRK [0x0206c000, 0x0206cfff] PGTABLE
[    0.000000] BRK [0x0206d000, 0x0206dfff] PGTABLE
[    0.000000] BRK [0x0206e000, 0x0206efff] PGTABLE
[    0.000000] BRK [0x0206f000, 0x0206ffff] PGTABLE
[    0.000000] RAMDISK: [mem 0x36d50000-0x3769ffff]
[    0.000000] ACPI: Early table checksum verification disabled
[    0.000000] ACPI: RSDP 0x00000000000F68C0 000024 (v02 LENOVO)
[    0.000000] ACPI: XSDT 0x00000000BEEBB496 00009C (v01 LENOVO TP-7U    00002290  LTP 00000000)
[    0.000000] ACPI: FACP 0x00000000BEEBB600 0000F4 (v03 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI BIOS Warning (bug): 32/64X length mismatch in FADT/Gpe0Block: 64/32 (20160108/tbfadt-623)
[    0.000000] ACPI BIOS Warning (bug): 32/64X length mismatch in FADT/Gpe1Block: 0/32 (20160108/tbfadt-623)
[    0.000000] ACPI BIOS Warning (bug): Optional FADT field Gpe1Block has zero address or length: 0x000000000000102C/0x0 (20160108/tbfadt-654)
[    0.000000] ACPI: DSDT 0x00000000BEEBBA1D 01003C (v01 LENOVO TP-7U    00002290 MSFT 03000000)
[    0.000000] ACPI: FACS 0x00000000BEEE4000 000040
[    0.000000] ACPI: FACS 0x00000000BEEE4000 000040
[    0.000000] ACPI: SSDT 0x00000000BEEBB7B4 000269 (v01 LENOVO TP-7U    00002290 MSFT 03000000)
[    0.000000] ACPI: ECDT 0x00000000BEECBA59 000052 (v01 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI: TCPA 0x00000000BEECBAAB 000032 (v02 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI: APIC 0x00000000BEECBADD 000068 (v01 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI: MCFG 0x00000000BEECBB45 00003C (v01 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI: HPET 0x00000000BEECBB81 000038 (v01 LENOVO TP-7U    00002290 LNVO 00000001)
[    0.000000] ACPI: SLIC 0x00000000BEECBBB9 000176 (v01 LENOVO TP-7U    00002290  LTP 00000000)
[    0.000000] ACPI: SLAC 0x00000000BEECBDF0 000176 (v01 LENOVO TP-7U    00002290  LTP 00000000)
[    0.000000] ACPI: BOOT 0x00000000BEECBF66 000028 (v01 LENOVO TP-7U    00002290  LTP 00000001)
[    0.000000] ACPI: ASF! 0x00000000BEECBF8E 000072 (v16 LENOVO TP-7U    00002290 PTL  00000001)
[    0.000000] ACPI: SSDT 0x00000000BEEE271B 00025F (v01 LENOVO TP-7U    00002290 INTL 20050513)
[    0.000000] ACPI: SSDT 0x00000000BEEE297A 0000A6 (v01 LENOVO TP-7U    00002290 INTL 20050513)
[    0.000000] ACPI: SSDT 0x00000000BEEE2A20 0004F7 (v01 LENOVO TP-7U    00002290 INTL 20050513)
[    0.000000] ACPI: SSDT 0x00000000BEEE2F17 0001D8 (v01 LENOVO TP-7U    00002290 INTL 20050513)
[    0.000000] ACPI: Local APIC address 0xfee00000
[    0.000000] No NUMA configuration found
[    0.000000] Faking a node at [mem 0x0000000000000000-0x00000000beeaffff]
[    0.000000] NODE_DATA(0) allocated [mem 0xbeeac000-0xbeeaffff]
[    0.000000] Zone ranges:
[    0.000000]   DMA      [mem 0x0000000000001000-0x0000000000ffffff]
[    0.000000]   DMA32    [mem 0x0000000001000000-0x00000000beeaffff]
[    0.000000]   Normal   empty
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x0000000000001000-0x000000000009cfff]
[    0.000000]   node   0: [mem 0x0000000000100000-0x00000000beeaffff]
[    0.000000] Initmem setup node 0 [mem 0x0000000000001000-0x00000000beeaffff]
[    0.000000] On node 0 totalpages: 781900
[    0.000000]   DMA zone: 64 pages used for memmap
[    0.000000]   DMA zone: 21 pages reserved
[    0.000000]   DMA zone: 3996 pages, LIFO batch:0
[    0.000000]   DMA32 zone: 12155 pages used for memmap
[    0.000000]   DMA32 zone: 777904 pages, LIFO batch:31
[    0.000000] ACPI: PM-Timer IO Port: 0x1008
[    0.000000] ACPI: Local APIC address 0xfee00000
[    0.000000] ACPI: LAPIC_NMI (acpi_id[0x00] high edge lint[0x1])
[    0.000000] ACPI: LAPIC_NMI (acpi_id[0x01] high edge lint[0x1])
[    0.000000] IOAPIC[0]: apic_id 1, version 32, address 0xfec00000, GSI 0-23
[    0.000000] ACPI: INT_SRC_OVR (bus 0 bus_irq 0 global_irq 2 dfl dfl)
[    0.000000] ACPI: INT_SRC_OVR (bus 0 bus_irq 9 global_irq 9 high level)
[    0.000000] ACPI: IRQ0 used by override.
[    0.000000] ACPI: IRQ9 used by override.
[    0.000000] Using ACPI (MADT) for SMP configuration information
[    0.000000] ACPI: HPET id: 0x8086a201 base: 0xfed00000
[    0.000000] smpboot: Allowing 2 CPUs, 0 hotplug CPUs
[    0.000000] e820: [mem 0xbf000000-0xefffffff] available for PCI devices
[    0.000000] clocksource: refined-jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 1910969940391419 ns
[    0.000000] setup_percpu: NR_CPUS:2 nr_cpumask_bits:2 nr_cpu_ids:2 nr_node_ids:1
[    0.000000] percpu: Embedded 31 pages/cpu @ffff8800bea00000 s86808 r8192 d31976 u1048576
[    0.000000] pcpu-alloc: s86808 r8192 d31976 u1048576 alloc=1*2097152
[    0.000000] pcpu-alloc: [0] 0 1 
[    0.000000] Built 1 zonelists in Node order, mobility grouping on.  Total pages: 769660
[    0.000000] Policy zone: DMA32
[    0.000000] Kernel command line: BOOT_IMAGE=/boot/vmlinuz-4.6.2-t61 root=UUID=ba6e0f3e-b3e6-4293-b0b3-0ab5602dcda9 ro quiet splash vt.handoff=7
[    0.000000] PID hash table entries: 4096 (order: 3, 32768 bytes)
[    0.000000] Memory: 3051568K/3127600K available (8992K kernel code, 750K rwdata, 3584K rodata, 908K init, 772K bss, 76032K reserved, 0K cma-reserved)
[    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=2, Nodes=1
[    0.000000] Preemptible hierarchical RCU implementation.
[    0.000000] 	Build-time adjustment of leaf fanout to 64.
[    0.000000] NR_IRQS:4352 nr_irqs:440 16
[    0.000000] Console: colour dummy device 80x25
[    0.000000] console [tty0] enabled
[    0.000000] clocksource: hpet: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 133484882848 ns
[    0.000000] hpet clockevent registered
[    0.000000] tsc: Fast TSC calibration using PIT
[    0.000000] tsc: Detected 2393.817 MHz processor
[    0.001012] Calibrating delay loop (skipped), value calculated using timer frequency.. 4787.63 BogoMIPS (lpj=2393817)
[    0.001015] pid_max: default: 32768 minimum: 301
[    0.001020] ACPI: Core revision 20160108
[    0.012182] ACPI: 6 ACPI AML tables successfully acquired and loaded

[    0.012204] Security Framework initialized
[    0.012207] SELinux:  Initializing.
[    0.012218] SELinux:  Starting in permissive mode
[    0.012477] Dentry cache hash table entries: 524288 (order: 10, 4194304 bytes)
[    0.015177] Inode-cache hash table entries: 262144 (order: 9, 2097152 bytes)
[    0.016561] Mount-cache hash table entries: 8192 (order: 4, 65536 bytes)
[    0.016567] Mountpoint-cache hash table entries: 8192 (order: 4, 65536 bytes)
[    0.016952] CPU: Physical Processor ID: 0
[    0.016954] CPU: Processor Core ID: 0
[    0.016956] mce: CPU supports 6 MCE banks
[    0.016969] mce: [Hardware Error]: Machine check events logged
[    0.016973] CPU0: Thermal monitoring enabled (TM2)
[    0.016977] process: using mwait in idle threads
[    0.016982] Last level iTLB entries: 4KB 128, 2MB 4, 4MB 4
[    0.016983] Last level dTLB entries: 4KB 256, 2MB 0, 4MB 32, 1GB 0
[    0.017404] Freeing SMP alternatives memory: 36K (ffffffff81fa0000 - ffffffff81fa9000)
[    0.018169] smpboot: Max logical packages: 1
[    0.018171] smpboot: APIC(0) Converting physical 0 to logical package 0
[    0.018661] ..TIMER: vector=0x30 apic1=0 pin1=2 apic2=-1 pin2=-1
[    0.029000] smpboot: CPU0: Intel(R) Core(TM)2 Duo CPU     T8300  @ 2.40GHz (family: 0x6, model: 0x17, stepping: 0x6)
[    0.029000] Performance Events: PEBS fmt0+, 4-deep LBR, Core2 events, Intel PMU driver.
[    0.029000] ... version:                2
[    0.029000] ... bit width:              40
[    0.029000] ... generic registers:      2
[    0.029000] ... value mask:             000000ffffffffff
[    0.029000] ... max period:             000000007fffffff
[    0.029000] ... fixed-purpose events:   3
[    0.029000] ... event mask:             0000000700000003
[    0.038012] x86: Booting SMP configuration:
[    0.038015] .... node  #0, CPUs:      #1
[    0.099000] TSC synchronization [CPU#0 -> CPU#1]:
[    0.099000] Measured 396360 cycles TSC warp between CPUs, turning off TSC clock.
[    0.099000] tsc: Marking TSC unstable due to check_tsc_sync_source failed
[    0.002000] mce: [Hardware Error]: Machine check events logged
[    0.099055] x86: Booted up 1 node, 2 CPUs
[    0.099055] smpboot: Total of 2 processors activated (9575.40 BogoMIPS)
[    0.100206] devtmpfs: initialized
[    0.101234] PM: Registering ACPI NVS region [mem 0xbeecc000-0xbeefffff] (212992 bytes)
[    0.101301] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 1911260446275000 ns
[    0.101334] xor: measuring software checksum speed
[    0.102041] kworker/u4:0 (22) used greatest stack depth: 14472 bytes left
[    0.111004]    prefetch64-sse: 13344.000 MB/sec
[    0.121001]    generic_sse: 11348.000 MB/sec
[    0.121003] xor: using function: prefetch64-sse (13344.000 MB/sec)
[    0.121107] NET: Registered protocol family 16
[    0.121224] kworker/u4:1 (23) used greatest stack depth: 14176 bytes left
[    0.124012] cpuidle: using governor menu
[    0.124078] Simple Boot Flag at 0x35 set to 0x1
[    0.124094] ACPI FADT declares the system doesn't support PCIe ASPM, so disable it
[    0.124096] ACPI: bus type PCI registered
[    0.124155] PCI: MMCONFIG for domain 0000 [bus 00-3f] at [mem 0xf0000000-0xf3ffffff] (base 0xf0000000)
[    0.124159] PCI: MMCONFIG at [mem 0xf0000000-0xf3ffffff] reserved in E820
[    0.124167] PCI: Using configuration type 1 for base access
[    0.124304] mtrr: your CPUs had inconsistent variable MTRR settings
[    0.124305] mtrr: probably your BIOS does not setup all CPUs.
[    0.124306] mtrr: corrected configuration.
[    0.135396] HugeTLB registered 2 MB page size, pre-allocated 0 pages
[    0.152016] raid6: sse2x1   gen()  3953 MB/s
[    0.168950] raid6: sse2x1   xor()  4105 MB/s
[    0.185947] raid6: sse2x2   gen()  4183 MB/s
[    0.202946] raid6: sse2x2   xor()  5037 MB/s
[    0.219949] raid6: sse2x4   gen()  7117 MB/s
[    0.236947] raid6: sse2x4   xor()  5710 MB/s
[    0.236948] raid6: using algorithm sse2x4 gen() 7117 MB/s
[    0.236950] raid6: .... xor() 5710 MB/s, rmw enabled
[    0.236951] raid6: using ssse3x2 recovery algorithm
[    0.237000] ACPI: Added _OSI(Module Device)
[    0.237000] ACPI: Added _OSI(Processor Device)
[    0.237000] ACPI: Added _OSI(3.0 _SCP Extensions)
[    0.237000] ACPI: Added _OSI(Processor Aggregator Device)
[    0.237140] ACPI : EC: EC description table is found, configuring boot EC
[    0.237163] ACPI : EC: EC started
[    0.241817] [Firmware Bug]: ACPI: BIOS _OSI(Linux) query ignored
[    0.247064] ACPI: Dynamic OEM Table Load:
[    0.247072] ACPI: SSDT 0xFFFF8800BAFBA000 000306 (v01 PmRef  Cpu0Ist  00000100 INTL 20050513)
[    0.247616] ACPI: Dynamic OEM Table Load:
[    0.247623] ACPI: SSDT 0xFFFF8800BAFB3000 00085E (v01 PmRef  Cpu0Cst  00000100 INTL 20050513)
[    0.248329] ACPI: Dynamic OEM Table Load:
[    0.248335] ACPI: SSDT 0xFFFF8800BA18B300 0000C8 (v01 PmRef  Cpu1Ist  00000100 INTL 20050513)
[    0.248806] ACPI: Dynamic OEM Table Load:
[    0.248812] ACPI: SSDT 0xFFFF8800BA18A0C0 000085 (v01 PmRef  Cpu1Cst  00000100 INTL 20050513)
[    0.249404] ACPI: Interpreter enabled
[    0.249419] ACPI: (supports S0 S3 S5)
[    0.249421] ACPI: Using IOAPIC for interrupt routing
[    0.249451] PCI: Using host bridge windows from ACPI; if necessary, use "pci=nocrs" and report a bug
[    0.253752] ACPI: Power Resource [PUBS] (on)
[    0.259556] ACPI: PCI Interrupt Link [LNKA] (IRQs 3 4 5 6 7 9 *10 11)
[    0.259656] ACPI: PCI Interrupt Link [LNKB] (IRQs 3 4 5 6 7 9 10 *11)
[    0.259753] ACPI: PCI Interrupt Link [LNKC] (IRQs 3 4 5 6 7 9 10 *11)
[    0.259850] ACPI: PCI Interrupt Link [LNKD] (IRQs 3 4 5 6 7 9 10 *11)
[    0.259946] ACPI: PCI Interrupt Link [LNKE] (IRQs 3 4 5 6 7 9 10 *11)
[    0.260048] ACPI: PCI Interrupt Link [LNKF] (IRQs 3 4 5 6 7 9 10 *11)
[    0.260144] ACPI: PCI Interrupt Link [LNKG] (IRQs 3 4 5 6 7 9 10 *11)
[    0.260241] ACPI: PCI Interrupt Link [LNKH] (IRQs 3 4 5 6 7 9 10 *11)
[    0.260351] ACPI: PCI Root Bridge [PCI0] (domain 0000 [bus 00-ff])
[    0.260357] acpi PNP0A08:00: _OSC: OS supports [ExtendedConfig ASPM ClockPM Segments MSI]
[    0.260803] acpi PNP0A08:00: _OSC: OS now controls [PCIeHotplug PME AER PCIeCapability]
[    0.260806] acpi PNP0A08:00: FADT indicates ASPM is unsupported, using BIOS configuration
[    0.260816] acpi PNP0A08:00: [Firmware Info]: MMCONFIG for domain 0000 [bus 00-3f] only partially covers this bridge
[    0.260869] PCI host bridge to bus 0000:00
[    0.260872] pci_bus 0000:00: root bus resource [io  0x0000-0x0cf7 window]
[    0.260874] pci_bus 0000:00: root bus resource [io  0x0d00-0xffff window]
[    0.260877] pci_bus 0000:00: root bus resource [mem 0x000a0000-0x000bffff window]
[    0.260879] pci_bus 0000:00: root bus resource [mem 0x000d4000-0x000d7fff window]
[    0.260881] pci_bus 0000:00: root bus resource [mem 0x000d8000-0x000dbfff window]
[    0.260883] pci_bus 0000:00: root bus resource [mem 0x000dc000-0x000dffff window]
[    0.260885] pci_bus 0000:00: root bus resource [mem 0xbf000000-0xfebfffff window]
[    0.260887] pci_bus 0000:00: root bus resource [mem 0xfed40000-0xfed4bfff window]
[    0.260889] pci_bus 0000:00: root bus resource [bus 00-ff]
[    0.260899] pci 0000:00:00.0: [8086:2a00] type 00 class 0x060000
[    0.261012] pci 0000:00:01.0: [8086:2a01] type 01 class 0x060400
[    0.261056] pci 0000:00:01.0: PME# supported from D0 D3hot D3cold
[    0.261217] pci 0000:00:19.0: [8086:1049] type 00 class 0x020000
[    0.261251] pci 0000:00:19.0: reg 0x10: [mem 0xfe200000-0xfe21ffff]
[    0.261276] pci 0000:00:19.0: reg 0x14: [mem 0xfe225000-0xfe225fff]
[    0.261302] pci 0000:00:19.0: reg 0x18: [io  0x1840-0x185f]
[    0.261468] pci 0000:00:19.0: PME# supported from D0 D3hot D3cold
[    0.261520] pci 0000:00:19.0: System wakeup disabled by ACPI
[    0.261576] pci 0000:00:1a.0: [8086:2834] type 00 class 0x0c0300
[    0.261706] pci 0000:00:1a.0: reg 0x20: [io  0x1860-0x187f]
[    0.261831] pci 0000:00:1a.0: System wakeup disabled by ACPI
[    0.261886] pci 0000:00:1a.1: [8086:2835] type 00 class 0x0c0300
[    0.262008] pci 0000:00:1a.1: reg 0x20: [io  0x1880-0x189f]
[    0.262133] pci 0000:00:1a.1: System wakeup disabled by ACPI
[    0.262213] pci 0000:00:1a.7: [8086:283a] type 00 class 0x0c0320
[    0.262249] pci 0000:00:1a.7: reg 0x10: [mem 0xfe226c00-0xfe226fff]
[    0.262463] pci 0000:00:1a.7: PME# supported from D0 D3hot D3cold
[    0.262513] pci 0000:00:1a.7: System wakeup disabled by ACPI
[    0.262583] pci 0000:00:1b.0: [8086:284b] type 00 class 0x040300
[    0.262613] pci 0000:00:1b.0: reg 0x10: [mem 0xfe220000-0xfe223fff 64bit]
[    0.262781] pci 0000:00:1b.0: PME# supported from D0 D3hot D3cold
[    0.262845] pci 0000:00:1b.0: System wakeup disabled by ACPI
[    0.262906] pci 0000:00:1c.0: [8086:283f] type 01 class 0x060400
[    0.263040] pci 0000:00:1c.0: PME# supported from D0 D3hot D3cold
[    0.263103] pci 0000:00:1c.0: System wakeup disabled by ACPI
[    0.263164] pci 0000:00:1c.1: [8086:2841] type 01 class 0x060400
[    0.263285] pci 0000:00:1c.1: PME# supported from D0 D3hot D3cold
[    0.263347] pci 0000:00:1c.1: System wakeup disabled by ACPI
[    0.263407] pci 0000:00:1c.2: [8086:2843] type 01 class 0x060400
[    0.263526] pci 0000:00:1c.2: PME# supported from D0 D3hot D3cold
[    0.263576] pci 0000:00:1c.2: System wakeup disabled by ACPI
[    0.263637] pci 0000:00:1c.3: [8086:2845] type 01 class 0x060400
[    0.263760] pci 0000:00:1c.3: PME# supported from D0 D3hot D3cold
[    0.263823] pci 0000:00:1c.3: System wakeup disabled by ACPI
[    0.263884] pci 0000:00:1c.4: [8086:2847] type 01 class 0x060400
[    0.264006] pci 0000:00:1c.4: PME# supported from D0 D3hot D3cold
[    0.264059] pci 0000:00:1c.4: System wakeup disabled by ACPI
[    0.264123] pci 0000:00:1d.0: [8086:2830] type 00 class 0x0c0300
[    0.264249] pci 0000:00:1d.0: reg 0x20: [io  0x18a0-0x18bf]
[    0.264444] pci 0000:00:1d.0: System wakeup disabled by ACPI
[    0.265001] pci 0000:00:1d.1: [8086:2831] type 00 class 0x0c0300
[    0.265094] pci 0000:00:1d.1: reg 0x20: [io  0x18c0-0x18df]
[    0.265253] pci 0000:00:1d.2: [8086:2832] type 00 class 0x0c0300
[    0.265384] pci 0000:00:1d.2: reg 0x20: [io  0x18e0-0x18ff]
[    0.265521] pci 0000:00:1d.2: System wakeup disabled by ACPI
[    0.265596] pci 0000:00:1d.7: [8086:2836] type 00 class 0x0c0320
[    0.265636] pci 0000:00:1d.7: reg 0x10: [mem 0xfe227000-0xfe2273ff]
[    0.265860] pci 0000:00:1d.7: PME# supported from D0 D3hot D3cold
[    0.265912] pci 0000:00:1d.7: System wakeup disabled by ACPI
[    0.266000] pci 0000:00:1e.0: [8086:2448] type 01 class 0x060401
[    0.266108] pci 0000:00:1e.0: System wakeup disabled by ACPI
[    0.266168] pci 0000:00:1f.0: [8086:2811] type 00 class 0x060100
[    0.266318] pci 0000:00:1f.0: can't claim BAR 7 [io  0x1000-0x107f]: address conflict with ACPI CPU throttle [io  0x1010-0x1015]
[    0.266326] pci 0000:00:1f.0: quirk: [io  0x1180-0x11bf] claimed by ICH6 GPIO
[    0.266332] pci 0000:00:1f.0: ICH7 LPC Generic IO decode 1 PIO at 1600 (mask 007f)
[    0.266338] pci 0000:00:1f.0: ICH7 LPC Generic IO decode 2 PIO at 15e0 (mask 000f)
[    0.266344] pci 0000:00:1f.0: ICH7 LPC Generic IO decode 3 PIO at 1680 (mask 001f)
[    0.266485] pci 0000:00:1f.1: [8086:2850] type 00 class 0x01018a
[    0.266514] pci 0000:00:1f.1: reg 0x10: [io  0x0000-0x0007]
[    0.266537] pci 0000:00:1f.1: reg 0x14: [io  0x0000-0x0003]
[    0.266562] pci 0000:00:1f.1: reg 0x18: [io  0x0000-0x0007]
[    0.266587] pci 0000:00:1f.1: reg 0x1c: [io  0x0000-0x0003]
[    0.266613] pci 0000:00:1f.1: reg 0x20: [io  0x1830-0x183f]
[    0.266670] pci 0000:00:1f.1: legacy IDE quirk: reg 0x10: [io  0x01f0-0x01f7]
[    0.266672] pci 0000:00:1f.1: legacy IDE quirk: reg 0x14: [io  0x03f6]
[    0.266674] pci 0000:00:1f.1: legacy IDE quirk: reg 0x18: [io  0x0170-0x0177]
[    0.266676] pci 0000:00:1f.1: legacy IDE quirk: reg 0x1c: [io  0x0376]
[    0.266781] pci 0000:00:1f.2: [8086:2829] type 00 class 0x010601
[    0.266808] pci 0000:00:1f.2: reg 0x10: [io  0x1c48-0x1c4f]
[    0.266822] pci 0000:00:1f.2: reg 0x14: [io  0x1c1c-0x1c1f]
[    0.266835] pci 0000:00:1f.2: reg 0x18: [io  0x1c40-0x1c47]
[    0.266848] pci 0000:00:1f.2: reg 0x1c: [io  0x1c18-0x1c1b]
[    0.266861] pci 0000:00:1f.2: reg 0x20: [io  0x1c20-0x1c3f]
[    0.266874] pci 0000:00:1f.2: reg 0x24: [mem 0xfe226000-0xfe2267ff]
[    0.266936] pci 0000:00:1f.2: PME# supported from D3hot
[    0.267040] pci 0000:00:1f.3: [8086:283e] type 00 class 0x0c0500
[    0.267065] pci 0000:00:1f.3: reg 0x10: [mem 0xfe227400-0xfe2274ff]
[    0.267156] pci 0000:00:1f.3: reg 0x20: [io  0x1c60-0x1c7f]
[    0.267344] pci 0000:01:00.0: [10de:0429] type 00 class 0x030000
[    0.267362] pci 0000:01:00.0: reg 0x10: [mem 0xd6000000-0xd6ffffff]
[    0.267377] pci 0000:01:00.0: reg 0x14: [mem 0xe0000000-0xefffffff 64bit pref]
[    0.267392] pci 0000:01:00.0: reg 0x1c: [mem 0xd4000000-0xd5ffffff 64bit]
[    0.267402] pci 0000:01:00.0: reg 0x24: [io  0x2000-0x207f]
[    0.267412] pci 0000:01:00.0: reg 0x30: [mem 0x00000000-0x0001ffff pref]
[    0.267540] pci 0000:00:01.0: PCI bridge to [bus 01]
[    0.267543] pci 0000:00:01.0:   bridge window [io  0x2000-0x2fff]
[    0.267546] pci 0000:00:01.0:   bridge window [mem 0xd4000000-0xd6ffffff]
[    0.267550] pci 0000:00:01.0:   bridge window [mem 0xe0000000-0xefffffff 64bit pref]
[    0.267631] pci 0000:00:1c.0: PCI bridge to [bus 02]
[    0.267641] pci 0000:00:1c.0:   bridge window [io  0x3000-0x3fff]
[    0.267648] pci 0000:00:1c.0:   bridge window [mem 0xfc000000-0xfdffffff]
[    0.267657] pci 0000:00:1c.0:   bridge window [mem 0xf8000000-0xf80fffff 64bit pref]
[    0.267809] pci 0000:03:00.0: [8086:4230] type 00 class 0x028000
[    0.267885] pci 0000:03:00.0: reg 0x10: [mem 0xdf2fe000-0xdf2fffff 64bit]
[    0.268149] pci 0000:03:00.0: PME# supported from D0 D3hot D3cold
[    0.270048] pci 0000:00:1c.1: PCI bridge to [bus 03]
[    0.270057] pci 0000:00:1c.1:   bridge window [io  0x4000-0x4fff]
[    0.270064] pci 0000:00:1c.1:   bridge window [mem 0xdc100000-0xdf2fffff]
[    0.270073] pci 0000:00:1c.1:   bridge window [mem 0xdfd00000-0xdfdfffff 64bit pref]
[    0.270159] pci 0000:00:1c.2: PCI bridge to [bus 04]
[    0.270166] pci 0000:00:1c.2:   bridge window [io  0x5000-0x5fff]
[    0.270173] pci 0000:00:1c.2:   bridge window [mem 0xd8000000-0xd9ffffff]
[    0.270182] pci 0000:00:1c.2:   bridge window [mem 0xdfa00000-0xdfafffff 64bit pref]
[    0.270258] pci 0000:00:1c.3: PCI bridge to [bus 05-0c]
[    0.270268] pci 0000:00:1c.3:   bridge window [io  0x6000-0x6fff]
[    0.270274] pci 0000:00:1c.3:   bridge window [mem 0xd0000000-0xd1ffffff]
[    0.270284] pci 0000:00:1c.3:   bridge window [mem 0xdf700000-0xdf7fffff 64bit pref]
[    0.270358] pci 0000:00:1c.4: PCI bridge to [bus 0d-14]
[    0.270365] pci 0000:00:1c.4:   bridge window [io  0x7000-0x7fff]
[    0.270374] pci 0000:00:1c.4:   bridge window [mem 0xcc000000-0xcdffffff]
[    0.270383] pci 0000:00:1c.4:   bridge window [mem 0xdf400000-0xdf4fffff 64bit pref]
[    0.270456] pci 0000:15:00.0: [1180:0476] type 02 class 0x060700
[    0.270490] pci 0000:15:00.0: proprietary Ricoh MMC controller disabled (via cardbus function)
[    0.270492] pci 0000:15:00.0: MMC cards are now supported by standard SDHCI controller
[    0.270519] pci 0000:15:00.0: reg 0x10: [mem 0xf8100000-0xf8100fff]
[    0.270578] pci 0000:15:00.0: supports D1 D2
[    0.270580] pci 0000:15:00.0: PME# supported from D0 D1 D2 D3hot D3cold
[    0.270661] pci 0000:15:00.1: [1180:0832] type 00 class 0x0c0010
[    0.270701] pci 0000:15:00.1: reg 0x10: [mem 0xf8101000-0xf81017ff]
[    0.270908] pci 0000:15:00.1: supports D1 D2
[    0.270910] pci 0000:15:00.1: PME# supported from D0 D1 D2 D3hot D3cold
[    0.271004] pci 0000:15:00.2: [1180:0822] type 00 class 0x080500
[    0.271024] pci 0000:15:00.2: reg 0x10: [mem 0xf8101800-0xf81018ff]
[    0.271228] pci 0000:15:00.2: supports D1 D2
[    0.271230] pci 0000:15:00.2: PME# supported from D0 D1 D2 D3hot D3cold
[    0.271311] pci 0000:15:00.4: [1180:0592] type 00 class 0x088000
[    0.271355] pci 0000:15:00.4: reg 0x10: [mem 0xf8102000-0xf81020ff]
[    0.271560] pci 0000:15:00.4: supports D1 D2
[    0.271562] pci 0000:15:00.4: PME# supported from D0 D1 D2 D3hot D3cold
[    0.271638] pci 0000:15:00.5: [1180:0852] type 00 class 0x088000
[    0.271680] pci 0000:15:00.5: reg 0x10: [mem 0xf8102400-0xf81024ff]
[    0.271896] pci 0000:15:00.5: supports D1 D2
[    0.271898] pci 0000:15:00.5: PME# supported from D0 D1 D2 D3hot D3cold
[    0.272076] pci 0000:00:1e.0: PCI bridge to [bus 15-18] (subtractive decode)
[    0.272084] pci 0000:00:1e.0:   bridge window [io  0x8000-0xbfff]
[    0.272090] pci 0000:00:1e.0:   bridge window [mem 0xf8100000-0xfbffffff]
[    0.272100] pci 0000:00:1e.0:   bridge window [mem 0xf4000000-0xf7ffffff 64bit pref]
[    0.272102] pci 0000:00:1e.0:   bridge window [io  0x0000-0x0cf7 window] (subtractive decode)
[    0.272104] pci 0000:00:1e.0:   bridge window [io  0x0d00-0xffff window] (subtractive decode)
[    0.272106] pci 0000:00:1e.0:   bridge window [mem 0x000a0000-0x000bffff window] (subtractive decode)
[    0.272108] pci 0000:00:1e.0:   bridge window [mem 0x000d4000-0x000d7fff window] (subtractive decode)
[    0.272110] pci 0000:00:1e.0:   bridge window [mem 0x000d8000-0x000dbfff window] (subtractive decode)
[    0.272113] pci 0000:00:1e.0:   bridge window [mem 0x000dc000-0x000dffff window] (subtractive decode)
[    0.272115] pci 0000:00:1e.0:   bridge window [mem 0xbf000000-0xfebfffff window] (subtractive decode)
[    0.272117] pci 0000:00:1e.0:   bridge window [mem 0xfed40000-0xfed4bfff window] (subtractive decode)
[    0.272193] pci_bus 0000:16: busn_res: can not insert [bus 16-ff] under [bus 15-18] (conflicts with (null) [bus 15-18])
[    0.272200] pci_bus 0000:16: busn_res: [bus 16-ff] end is updated to 17
[    0.273375] ACPI: Enabled 3 GPEs in block 00 to 1F
[    0.273452] ACPI : EC: GPE = 0x12, I/O: command/status = 0x66, data = 0x62
[    0.273557] vgaarb: setting as boot device: PCI:0000:01:00.0
[    0.273557] vgaarb: device added: PCI:0000:01:00.0,decodes=io+mem,owns=io+mem,locks=none
[    0.273557] vgaarb: loaded
[    0.273557] vgaarb: bridge control possible 0000:01:00.0
[    0.273557] SCSI subsystem initialized
[    0.274036] libata version 3.00 loaded.
[    0.274090] ACPI: bus type USB registered
[    0.274135] usbcore: registered new interface driver usbfs
[    0.274153] usbcore: registered new interface driver hub
[    0.274171] usbcore: registered new device driver usb
[    0.274210] pps_core: LinuxPPS API ver. 1 registered
[    0.274212] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    0.274219] PTP clock support registered
[    0.275206] wmi: Mapper loaded
[    0.275236] Advanced Linux Sound Architecture Driver Initialized.
[    0.275265] PCI: Using ACPI for IRQ routing
[    0.277641] PCI: pci_cache_line_size set to 64 bytes
[    0.277851] e820: reserve RAM buffer [mem 0x0009d800-0x0009ffff]
[    0.277854] e820: reserve RAM buffer [mem 0xbeeb0000-0xbfffffff]
[    0.277998] Bluetooth: Core ver 2.21
[    0.278047] NET: Registered protocol family 31
[    0.278048] Bluetooth: HCI device and connection manager initialized
[    0.278052] Bluetooth: HCI socket layer initialized
[    0.278054] Bluetooth: L2CAP socket layer initialized
[    0.278066] Bluetooth: SCO socket layer initialized
[    0.278187] NetLabel: Initializing
[    0.278189] NetLabel:  domain hash size = 128
[    0.278190] NetLabel:  protocols = UNLABELED CIPSOv4
[    0.278207] NetLabel:  unlabeled traffic allowed by default
[    0.278327] HPET: 3 timers in total, 0 timers will be used for per-cpu timer
[    0.278338] hpet0: at MMIO 0xfed00000, IRQs 2, 8, 0
[    0.278342] hpet0: 3 comparators, 64-bit 14.318180 MHz counter
[    0.280043] clocksource: Switched to clocksource hpet
[    0.280085] VFS: Disk quotas dquot_6.6.0
[    0.280100] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
[    0.280205] pnp: PnP ACPI init
[    0.280638] system 00:00: [mem 0x00000000-0x0009ffff] could not be reserved
[    0.280638] system 00:00: [mem 0x000c0000-0x000c3fff] could not be reserved
[    0.280638] system 00:00: [mem 0x000c4000-0x000c7fff] could not be reserved
[    0.280638] system 00:00: [mem 0x000c8000-0x000cbfff] could not be reserved
[    0.280638] system 00:00: [mem 0x000cc000-0x000cffff] could not be reserved
[    0.280638] system 00:00: [mem 0x000d0000-0x000d3fff] could not be reserved
[    0.280638] system 00:00: [mem 0x000e0000-0x000e3fff] could not be reserved
[    0.280638] system 00:00: [mem 0x000e4000-0x000e7fff] could not be reserved
[    0.280638] system 00:00: [mem 0x000e8000-0x000ebfff] could not be reserved
[    0.280640] system 00:00: [mem 0x000ec000-0x000effff] could not be reserved
[    0.280642] system 00:00: [mem 0x000f0000-0x000fffff] could not be reserved
[    0.280645] system 00:00: [mem 0x00100000-0xbeffffff] could not be reserved
[    0.280647] system 00:00: [mem 0xfec00000-0xfed3ffff] could not be reserved
[    0.280650] system 00:00: [mem 0xfed4c000-0xffffffff] could not be reserved
[    0.280654] system 00:00: Plug and Play ACPI device, IDs PNP0c01 (active)
[    0.280782] system 00:01: [io  0x164e-0x164f] has been reserved
[    0.280785] system 00:01: [io  0x1000-0x107f] could not be reserved
[    0.280787] system 00:01: [io  0x1180-0x11bf] has been reserved
[    0.280790] system 00:01: [io  0x0800-0x080f] has been reserved
[    0.280792] system 00:01: [io  0x15e0-0x15ef] has been reserved
[    0.280794] system 00:01: [io  0x1600-0x165f] could not be reserved
[    0.280797] system 00:01: [mem 0xf0000000-0xf3ffffff] has been reserved
[    0.280800] system 00:01: [mem 0xfed1c000-0xfed1ffff] has been reserved
[    0.280802] system 00:01: [mem 0xfed14000-0xfed17fff] has been reserved
[    0.280804] system 00:01: [mem 0xfed18000-0xfed18fff] has been reserved
[    0.280807] system 00:01: [mem 0xfed19000-0xfed19fff] has been reserved
[    0.280809] system 00:01: [mem 0xfed45000-0xfed4bfff] has been reserved
[    0.280813] system 00:01: Plug and Play ACPI device, IDs PNP0c02 (active)
[    0.280875] pnp 00:02: Plug and Play ACPI device, IDs PNP0b00 (active)
[    0.280908] pnp 00:03: Plug and Play ACPI device, IDs PNP0303 (active)
[    0.280937] pnp 00:04: Plug and Play ACPI device, IDs IBM0057 PNP0f13 (active)
[    0.281333] pnp 00:05: Plug and Play ACPI device, IDs ATM1200 PNP0c31 (active)
[    0.281878] pnp: PnP ACPI: found 6 devices
[    0.288620] clocksource: acpi_pm: mask: 0xffffff max_cycles: 0xffffff, max_idle_ns: 2085701024 ns
[    0.288776] pci 0000:00:1f.0: BAR 7: [io  size 0x0080] has bogus alignment
[    0.288784] pci 0000:01:00.0: BAR 6: no space for [mem size 0x00020000 pref]
[    0.288787] pci 0000:01:00.0: BAR 6: failed to assign [mem size 0x00020000 pref]
[    0.288789] pci 0000:00:01.0: PCI bridge to [bus 01]
[    0.288792] pci 0000:00:01.0:   bridge window [io  0x2000-0x2fff]
[    0.288796] pci 0000:00:01.0:   bridge window [mem 0xd4000000-0xd6ffffff]
[    0.288799] pci 0000:00:01.0:   bridge window [mem 0xe0000000-0xefffffff 64bit pref]
[    0.288804] pci 0000:00:1c.0: PCI bridge to [bus 02]
[    0.288809] pci 0000:00:1c.0:   bridge window [io  0x3000-0x3fff]
[    0.288817] pci 0000:00:1c.0:   bridge window [mem 0xfc000000-0xfdffffff]
[    0.288824] pci 0000:00:1c.0:   bridge window [mem 0xf8000000-0xf80fffff 64bit pref]
[    0.288834] pci 0000:00:1c.1: PCI bridge to [bus 03]
[    0.288839] pci 0000:00:1c.1:   bridge window [io  0x4000-0x4fff]
[    0.288851] pci 0000:00:1c.1:   bridge window [mem 0xdc100000-0xdf2fffff]
[    0.288860] pci 0000:00:1c.1:   bridge window [mem 0xdfd00000-0xdfdfffff 64bit pref]
[    0.288877] pci 0000:00:1c.2: PCI bridge to [bus 04]
[    0.288882] pci 0000:00:1c.2:   bridge window [io  0x5000-0x5fff]
[    0.288890] pci 0000:00:1c.2:   bridge window [mem 0xd8000000-0xd9ffffff]
[    0.288897] pci 0000:00:1c.2:   bridge window [mem 0xdfa00000-0xdfafffff 64bit pref]
[    0.288913] pci 0000:00:1c.3: PCI bridge to [bus 05-0c]
[    0.288918] pci 0000:00:1c.3:   bridge window [io  0x6000-0x6fff]
[    0.288929] pci 0000:00:1c.3:   bridge window [mem 0xd0000000-0xd1ffffff]
[    0.288938] pci 0000:00:1c.3:   bridge window [mem 0xdf700000-0xdf7fffff 64bit pref]
[    0.288947] pci 0000:00:1c.4: PCI bridge to [bus 0d-14]
[    0.288952] pci 0000:00:1c.4:   bridge window [io  0x7000-0x7fff]
[    0.288960] pci 0000:00:1c.4:   bridge window [mem 0xcc000000-0xcdffffff]
[    0.288969] pci 0000:00:1c.4:   bridge window [mem 0xdf400000-0xdf4fffff 64bit pref]
[    0.288982] pci 0000:15:00.0: res[9]=[mem 0x04000000-0x03ffffff pref] res_to_dev_res add_size 4000000 min_align 4000000
[    0.288984] pci 0000:15:00.0: res[9]=[mem 0x04000000-0x07ffffff pref] res_to_dev_res add_size 4000000 min_align 4000000
[    0.288987] pci 0000:15:00.0: res[10]=[mem 0x04000000-0x03ffffff] res_to_dev_res add_size 4000000 min_align 4000000
[    0.288989] pci 0000:15:00.0: res[10]=[mem 0x04000000-0x07ffffff] res_to_dev_res add_size 4000000 min_align 4000000
[    0.288992] pci 0000:15:00.0: res[7]=[io  0x0100-0x00ff] res_to_dev_res add_size 100 min_align 100
[    0.288994] pci 0000:15:00.0: res[7]=[io  0x0100-0x01ff] res_to_dev_res add_size 100 min_align 100
[    0.288997] pci 0000:15:00.0: res[8]=[io  0x0100-0x00ff] res_to_dev_res add_size 100 min_align 100
[    0.288999] pci 0000:15:00.0: res[8]=[io  0x0100-0x01ff] res_to_dev_res add_size 100 min_align 100
[    0.289014] pci 0000:15:00.0: BAR 9: assigned [mem 0xf4000000-0xf7ffffff pref]
[    0.289019] pci 0000:15:00.0: BAR 10: assigned [mem 0xc0000000-0xc3ffffff]
[    0.289021] pci 0000:15:00.0: BAR 7: assigned [io  0x8000-0x80ff]
[    0.289023] pci 0000:15:00.0: BAR 8: assigned [io  0x8400-0x84ff]
[    0.289026] pci 0000:15:00.0: CardBus bridge to [bus 16-17]
[    0.289028] pci 0000:15:00.0:   bridge window [io  0x8000-0x80ff]
[    0.289035] pci 0000:15:00.0:   bridge window [io  0x8400-0x84ff]
[    0.289045] pci 0000:15:00.0:   bridge window [mem 0xf4000000-0xf7ffffff pref]
[    0.289052] pci 0000:15:00.0:   bridge window [mem 0xc0000000-0xc3ffffff]
[    0.289059] pci 0000:00:1e.0: PCI bridge to [bus 15-18]
[    0.289065] pci 0000:00:1e.0:   bridge window [io  0x8000-0xbfff]
[    0.289077] pci 0000:00:1e.0:   bridge window [mem 0xf8100000-0xfbffffff]
[    0.289084] pci 0000:00:1e.0:   bridge window [mem 0xf4000000-0xf7ffffff 64bit pref]
[    0.289101] pci_bus 0000:00: resource 4 [io  0x0000-0x0cf7 window]
[    0.289104] pci_bus 0000:00: resource 5 [io  0x0d00-0xffff window]
[    0.289106] pci_bus 0000:00: resource 6 [mem 0x000a0000-0x000bffff window]
[    0.289108] pci_bus 0000:00: resource 7 [mem 0x000d4000-0x000d7fff window]
[    0.289110] pci_bus 0000:00: resource 8 [mem 0x000d8000-0x000dbfff window]
[    0.289112] pci_bus 0000:00: resource 9 [mem 0x000dc000-0x000dffff window]
[    0.289114] pci_bus 0000:00: resource 10 [mem 0xbf000000-0xfebfffff window]
[    0.289116] pci_bus 0000:00: resource 11 [mem 0xfed40000-0xfed4bfff window]
[    0.289118] pci_bus 0000:01: resource 0 [io  0x2000-0x2fff]
[    0.289120] pci_bus 0000:01: resource 1 [mem 0xd4000000-0xd6ffffff]
[    0.289122] pci_bus 0000:01: resource 2 [mem 0xe0000000-0xefffffff 64bit pref]
[    0.289124] pci_bus 0000:02: resource 0 [io  0x3000-0x3fff]
[    0.289126] pci_bus 0000:02: resource 1 [mem 0xfc000000-0xfdffffff]
[    0.289128] pci_bus 0000:02: resource 2 [mem 0xf8000000-0xf80fffff 64bit pref]
[    0.289131] pci_bus 0000:03: resource 0 [io  0x4000-0x4fff]
[    0.289133] pci_bus 0000:03: resource 1 [mem 0xdc100000-0xdf2fffff]
[    0.289135] pci_bus 0000:03: resource 2 [mem 0xdfd00000-0xdfdfffff 64bit pref]
[    0.289137] pci_bus 0000:04: resource 0 [io  0x5000-0x5fff]
[    0.289139] pci_bus 0000:04: resource 1 [mem 0xd8000000-0xd9ffffff]
[    0.289141] pci_bus 0000:04: resource 2 [mem 0xdfa00000-0xdfafffff 64bit pref]
[    0.289143] pci_bus 0000:05: resource 0 [io  0x6000-0x6fff]
[    0.289145] pci_bus 0000:05: resource 1 [mem 0xd0000000-0xd1ffffff]
[    0.289147] pci_bus 0000:05: resource 2 [mem 0xdf700000-0xdf7fffff 64bit pref]
[    0.289149] pci_bus 0000:0d: resource 0 [io  0x7000-0x7fff]
[    0.289151] pci_bus 0000:0d: resource 1 [mem 0xcc000000-0xcdffffff]
[    0.289153] pci_bus 0000:0d: resource 2 [mem 0xdf400000-0xdf4fffff 64bit pref]
[    0.289155] pci_bus 0000:15: resource 0 [io  0x8000-0xbfff]
[    0.289157] pci_bus 0000:15: resource 1 [mem 0xf8100000-0xfbffffff]
[    0.289159] pci_bus 0000:15: resource 2 [mem 0xf4000000-0xf7ffffff 64bit pref]
[    0.289161] pci_bus 0000:15: resource 4 [io  0x0000-0x0cf7 window]
[    0.289163] pci_bus 0000:15: resource 5 [io  0x0d00-0xffff window]
[    0.289165] pci_bus 0000:15: resource 6 [mem 0x000a0000-0x000bffff window]
[    0.289167] pci_bus 0000:15: resource 7 [mem 0x000d4000-0x000d7fff window]
[    0.289169] pci_bus 0000:15: resource 8 [mem 0x000d8000-0x000dbfff window]
[    0.289171] pci_bus 0000:15: resource 9 [mem 0x000dc000-0x000dffff window]
[    0.289173] pci_bus 0000:15: resource 10 [mem 0xbf000000-0xfebfffff window]
[    0.289175] pci_bus 0000:15: resource 11 [mem 0xfed40000-0xfed4bfff window]
[    0.289177] pci_bus 0000:16: resource 0 [io  0x8000-0x80ff]
[    0.289179] pci_bus 0000:16: resource 1 [io  0x8400-0x84ff]
[    0.289181] pci_bus 0000:16: resource 2 [mem 0xf4000000-0xf7ffffff pref]
[    0.289183] pci_bus 0000:16: resource 3 [mem 0xc0000000-0xc3ffffff]
[    0.289219] NET: Registered protocol family 2
[    0.289420] TCP established hash table entries: 32768 (order: 6, 262144 bytes)
[    0.289525] TCP bind hash table entries: 32768 (order: 7, 524288 bytes)
[    0.289717] TCP: Hash tables configured (established 32768 bind 32768)
[    0.289778] UDP hash table entries: 2048 (order: 4, 65536 bytes)
[    0.289804] UDP-Lite hash table entries: 2048 (order: 4, 65536 bytes)
[    0.289866] NET: Registered protocol family 1
[    0.290913] pci 0000:01:00.0: Video device with shadowed ROM at [mem 0x000c0000-0x000dffff]
[    0.290950] PCI: CLS mismatch (64 != 32), using 64 bytes
[    0.291051] Trying to unpack rootfs image as initramfs...
[    0.463310] Freeing initrd memory: 9536K (ffff880036d50000 - ffff8800376a0000)
[    0.463830] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x228166e438d, max_idle_ns: 440795306535 ns
[    0.464111] Scanning for low memory corruption every 60 seconds
[    0.464386] futex hash table entries: 512 (order: 3, 32768 bytes)
[    0.464425] audit: initializing netlink subsys (disabled)
[    0.464455] audit: type=2000 audit(1466377175.463:1): initialized
[    0.466080] workingset: timestamp_bits=54 max_order=20 bucket_order=0
[    0.469296] fuse init (API version 7.24)
[    0.469617] SELinux:  Registering netfilter hooks
[    0.471398] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 251)
[    0.471403] io scheduler noop registered
[    0.471448] io scheduler cfq registered (default)
[    0.473110] pcieport 0000:00:01.0: Signaling PME through PCIe PME interrupt
[    0.473114] pci 0000:01:00.0: Signaling PME through PCIe PME interrupt
[    0.473118] pcie_pme 0000:00:01.0:pcie01: service driver pcie_pme loaded
[    0.473154] pcieport 0000:00:1c.0: Signaling PME through PCIe PME interrupt
[    0.473162] pcie_pme 0000:00:1c.0:pcie01: service driver pcie_pme loaded
[    0.473194] pcieport 0000:00:1c.1: Signaling PME through PCIe PME interrupt
[    0.473196] pci 0000:03:00.0: Signaling PME through PCIe PME interrupt
[    0.473205] pcie_pme 0000:00:1c.1:pcie01: service driver pcie_pme loaded
[    0.473243] pcieport 0000:00:1c.2: Signaling PME through PCIe PME interrupt
[    0.473252] pcie_pme 0000:00:1c.2:pcie01: service driver pcie_pme loaded
[    0.473298] pcieport 0000:00:1c.3: Signaling PME through PCIe PME interrupt
[    0.473305] pcie_pme 0000:00:1c.3:pcie01: service driver pcie_pme loaded
[    0.473351] pcieport 0000:00:1c.4: Signaling PME through PCIe PME interrupt
[    0.473358] pcie_pme 0000:00:1c.4:pcie01: service driver pcie_pme loaded
[    0.473468] nvidiafb: Device ID: 10de0429 
[    0.473470] nvidiafb: unknown NV_ARCH
[    0.473494] intel_idle: does not run on family 6 model 23
[    0.473719] ACPI: AC Adapter [AC] (on-line)
[    0.473817] input: Lid Switch as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0D:00/input/input0
[    0.473970] ACPI: Lid Switch [LID]
[    0.474112] input: Sleep Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0E:00/input/input1
[    0.474116] ACPI: Sleep Button [SLPB]
[    0.474172] input: Power Button as /devices/LNXSYSTM:00/LNXPWRBN:00/input/input2
[    0.474175] ACPI: Power Button [PWRF]
[    0.474289] ACPI: Video Device [VID1] (multi-head: yes  rom: no  post: no)
[    0.476774] acpi device:06: registered as cooling_device0
[    0.476845] input: Video Bus as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0A08:00/device:05/LNXVIDEO:01/input/input3
[    0.477449] Monitor-Mwait will be used to enter C-1 state
[    0.477465] Monitor-Mwait will be used to enter C-2 state
[    0.477479] Monitor-Mwait will be used to enter C-3 state
[    0.481038] thermal LNXTHERM:00: registered as thermal_zone0
[    0.481040] ACPI: Thermal Zone [THM0] (60 C)
[    0.482382] thermal LNXTHERM:01: registered as thermal_zone1
[    0.482384] ACPI: Thermal Zone [THM1] (57 C)
[    0.482536] Serial: 8250/16550 driver, 4 ports, IRQ sharing enabled
[    0.482625] ACPI: Battery Slot [BAT0] (battery absent)
[    0.483137] Non-volatile memory driver v1.3
[    0.483175] Linux agpgart interface v0.103
[    0.483333] [drm] Initialized drm 1.1.0 20060810
[    0.483406] nouveau 0000:01:00.0: NVIDIA G86 (086900a2)
[    0.503967] nouveau 0000:01:00.0: bios: version 60.86.3e.00.00
[    0.525576] nouveau 0000:01:00.0: fb: 128 MiB GDDR3
[    0.575282] [TTM] Zone  kernel: Available graphics memory: 1530570 kiB
[    0.575319] [TTM] Initializing pool allocator
[    0.575326] [TTM] Initializing DMA pool allocator
[    0.575338] nouveau 0000:01:00.0: DRM: VRAM: 128 MiB
[    0.575340] nouveau 0000:01:00.0: DRM: GART: 1048576 MiB
[    0.575344] nouveau 0000:01:00.0: DRM: TMDS table version 2.0
[    0.575346] nouveau 0000:01:00.0: DRM: DCB version 4.0
[    0.575349] nouveau 0000:01:00.0: DRM: DCB outp 00: 01000323 00010034
[    0.575352] nouveau 0000:01:00.0: DRM: DCB outp 01: 02811300 00000028
[    0.575354] nouveau 0000:01:00.0: DRM: DCB outp 02: 02822312 00010030
[    0.575356] nouveau 0000:01:00.0: DRM: DCB outp 03: 014333f1 0080c080
[    0.575359] nouveau 0000:01:00.0: DRM: DCB conn 00: 0040
[    0.575361] nouveau 0000:01:00.0: DRM: DCB conn 01: 0100
[    0.575363] nouveau 0000:01:00.0: DRM: DCB conn 02: 1231
[    0.575365] nouveau 0000:01:00.0: DRM: DCB conn 03: 0311
[    0.584153] nouveau 0000:01:00.0: DRM: failed to create encoder 0/1/0: -19
[    0.584156] nouveau 0000:01:00.0: DRM: TV-1 has no encoders, removing
[    0.584192] [drm] Supports vblank timestamp caching Rev 2 (21.10.2013).
[    0.584194] [drm] Driver supports precise vblank timestamp query.
[    0.600238] nouveau 0000:01:00.0: DRM: MM: using CRYPT for buffer copies
[    1.933693] nouveau 0000:01:00.0: DRM: allocated 1680x1050 fb: 0x50000, bo ffff8800b91f1000
[    1.933810] fbcon: nouveaufb (fb0) is primary device
[    2.019662] Console: switching to colour frame buffer device 210x65
[    2.023471] nouveau 0000:01:00.0: fb0: nouveaufb frame buffer device
[    2.023475] [drm] Initialized nouveau 1.3.1 20120801 for 0000:01:00.0 on minor 0
[    2.024398] brd: module loaded
[    2.025993] loop: module loaded
[    2.026071] Uniform Multi-Platform E-IDE driver
[    2.026143] ide-gd driver 1.18
[    2.026395] ahci 0000:00:1f.2: version 3.0
[    2.026639] ahci 0000:00:1f.2: AHCI 0001.0100 32 slots 3 ports 3 Gbps 0x5 impl SATA mode
[    2.026643] ahci 0000:00:1f.2: flags: 64bit ncq sntf pm led clo pio slum part ccc 
[    2.027201] scsi host0: ahci
[    2.027349] scsi host1: ahci
[    2.027487] scsi host2: ahci
[    2.027547] ata1: SATA max UDMA/133 abar m2048@0xfe226000 port 0xfe226100 irq 31
[    2.027549] ata2: DUMMY
[    2.027553] ata3: SATA max UDMA/133 abar m2048@0xfe226000 port 0xfe226200 irq 31
[    2.027624] ata_piix 0000:00:1f.1: version 2.13
[    2.028318] scsi host3: ata_piix
[    2.028476] scsi host4: ata_piix
[    2.028526] ata4: PATA max UDMA/100 cmd 0x1f0 ctl 0x3f6 bmdma 0x1830 irq 14
[    2.028528] ata5: PATA max UDMA/100 cmd 0x170 ctl 0x376 bmdma 0x1838 irq 15
[    2.028552] e100: Intel(R) PRO/100 Network Driver, 3.5.24-k2-NAPI
[    2.028554] e100: Copyright(c) 1999-2006 Intel Corporation
[    2.028575] e1000e: Intel(R) PRO/1000 Network Driver - 3.2.6-k
[    2.028576] e1000e: Copyright(c) 1999 - 2015 Intel Corporation.
[    2.028774] e1000e 0000:00:19.0: Interrupt Throttling Rate (ints/sec) set to dynamic conservative mode
[    2.030709] ata5: port disabled--ignoring
[    2.183110] ata4.00: ATAPI: MATSHITADVD-RAM UJ-842, RB01, max UDMA/33
[    2.188205] ata4.00: configured for UDMA/33
[    2.331781] ata1: SATA link up 3.0 Gbps (SStatus 123 SControl 300)
[    2.332830] ata3: SATA link down (SStatus 0 SControl 300)
[    2.343769] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (unknown) succeeded
[    2.343772] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (unknown) filtered out
[    2.343775] ata1.00: ACPI cmd ef/10:03:00:00:00:a0 (unknown) filtered out
[    2.348528] e1000e 0000:00:19.0 eth0: (PCI Express:2.5GT/s:Width x1) 00:1e:37:d2:47:fa
[    2.348534] e1000e 0000:00:19.0 eth0: Intel(R) PRO/1000 Network Connection
[    2.348570] e1000e 0000:00:19.0 eth0: MAC: 6, PHY: 6, PBA No: 1008FF-0FF
[    2.348596] iwl4965: Intel(R) Wireless WiFi 4965 driver for Linux, in-tree:
[    2.348597] iwl4965: Copyright(c) 2003-2011 Intel Corporation
[    2.348643] iwl4965 0000:03:00.0: can't disable ASPM; OS doesn't have ASPM control
[    2.348809] iwl4965 0000:03:00.0: Detected Intel(R) Wireless WiFi Link 4965AGN, REV=0x4
[    2.350768] ata1.00: ATA-8: KINGSTON SHFS37A120G, 603ABBF0, max UDMA/133
[    2.350770] ata1.00: 234441648 sectors, multi 1: LBA48 NCQ (depth 31/32), AA
[    2.356141] ata1.00: ACPI cmd ef/02:00:00:00:00:a0 (unknown) succeeded
[    2.356144] ata1.00: ACPI cmd f5/00:00:00:00:00:a0 (unknown) filtered out
[    2.356147] ata1.00: ACPI cmd ef/10:03:00:00:00:a0 (unknown) filtered out
[    2.361531] ata1.00: configured for UDMA/133
[    2.362680] scsi 0:0:0:0: Direct-Access     ATA      KINGSTON SHFS37A BBF0 PQ: 0 ANSI: 5
[    2.370264] sd 0:0:0:0: [sda] 234441648 512-byte logical blocks: (120 GB/112 GiB)
[    2.370337] sd 0:0:0:0: [sda] Write Protect is off
[    2.370340] sd 0:0:0:0: [sda] Mode Sense: 00 3a 00 00
[    2.370365] sd 0:0:0:0: [sda] Write cache: enabled, read cache: enabled, doesn't support DPO or FUA
[    2.370532] sd 0:0:0:0: Attached scsi generic sg0 type 0
[    2.371122]  sda: sda1 sda2 < sda5 >
[    2.371489] sd 0:0:0:0: [sda] Attached SCSI disk
[    2.373715] scsi 3:0:0:0: CD-ROM            MATSHITA DVD-RAM UJ-842   RB01 PQ: 0 ANSI: 5
[    2.391802] iwl4965 0000:03:00.0: device EEPROM VER=0x36, CALIB=0x5
[    2.391812] iwl4965 0000:03:00.0: Tunable channels: 13 802.11bg, 19 802.11a channels
[    2.392067] iwl4965 0000:03:00.0: loaded firmware version 228.61.2.24
[    2.392353] ieee80211 phy0: Selected rate control algorithm 'iwl-4965-rs'
[    2.393736] pci 0000:00:1e.0: enabling device (0005 -> 0007)
[    2.397937] sr 3:0:0:0: [sr0] scsi3-mmc drive: 24x/24x writer dvd-ram cd/rw xa/form2 cdda tray
[    2.397940] cdrom: Uniform CD-ROM driver Revision: 3.20
[    2.398107] sr 3:0:0:0: Attached scsi CD-ROM sr0
[    2.398249] sr 3:0:0:0: Attached scsi generic sg1 type 5
[    2.446087] firewire_ohci 0000:15:00.1: added OHCI v1.10 device as card 0, 4 IR + 4 IT contexts, quirks 0x11
[    2.446186] yenta_cardbus 0000:15:00.0: CardBus bridge found [17aa:20c6]
[    2.568908] yenta_cardbus 0000:15:00.0: ISA IRQ mask 0x0cb8, PCI irq 16
[    2.568920] yenta_cardbus 0000:15:00.0: Socket status: 30000006
[    2.568924] yenta_cardbus 0000:15:00.0: pcmcia: parent PCI bridge window: [io  0x8000-0xbfff]
[    2.568926] yenta_cardbus 0000:15:00.0: pcmcia: parent PCI bridge window: [mem 0xf8100000-0xfbffffff]
[    2.568928] pcmcia_socket pcmcia_socket0: cs: memory probe 0xf8100000-0xfbffffff:
[    2.568932]  excluding 0xf8100000-0xf84effff
[    2.568940] yenta_cardbus 0000:15:00.0: pcmcia: parent PCI bridge window: [mem 0xf4000000-0xf7ffffff 64bit pref]
[    2.568942] pcmcia_socket pcmcia_socket0: cs: memory probe 0xf4000000-0xf7ffffff:
[    2.568945]  excluding 0xf4000000-0xf7ffffff
[    2.569502] ehci_hcd: USB 2.0 'Enhanced' Host Controller (EHCI) Driver
[    2.569505] ehci-pci: EHCI PCI platform driver
[    2.569629] ehci-pci 0000:00:1a.7: EHCI Host Controller
[    2.569686] ehci-pci 0000:00:1a.7: new USB bus registered, assigned bus number 1
[    2.573624] ehci-pci 0000:00:1a.7: cache line size of 64 is not supported
[    2.573638] ehci-pci 0000:00:1a.7: irq 22, io mem 0xfe226c00
[    2.579064] ehci-pci 0000:00:1a.7: USB 2.0 started, EHCI 1.00
[    2.579133] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002
[    2.579136] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.579138] usb usb1: Product: EHCI Host Controller
[    2.579140] usb usb1: Manufacturer: Linux 4.6.2-t61 ehci_hcd
[    2.579141] usb usb1: SerialNumber: 0000:00:1a.7
[    2.579308] hub 1-0:1.0: USB hub found
[    2.579321] hub 1-0:1.0: 4 ports detected
[    2.579558] ehci-pci 0000:00:1d.7: EHCI Host Controller
[    2.579642] ehci-pci 0000:00:1d.7: new USB bus registered, assigned bus number 2
[    2.579664] ehci-pci 0000:00:1d.7: debug port 1
[    2.583575] ehci-pci 0000:00:1d.7: cache line size of 64 is not supported
[    2.583588] ehci-pci 0000:00:1d.7: irq 19, io mem 0xfe227000
[    2.589066] ehci-pci 0000:00:1d.7: USB 2.0 started, EHCI 1.00
[    2.589091] usb usb2: New USB device found, idVendor=1d6b, idProduct=0002
[    2.589093] usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.589095] usb usb2: Product: EHCI Host Controller
[    2.589097] usb usb2: Manufacturer: Linux 4.6.2-t61 ehci_hcd
[    2.589099] usb usb2: SerialNumber: 0000:00:1d.7
[    2.589258] hub 2-0:1.0: USB hub found
[    2.589266] hub 2-0:1.0: 6 ports detected
[    2.589457] ohci_hcd: USB 1.1 'Open' Host Controller (OHCI) Driver
[    2.589470] ohci-pci: OHCI PCI platform driver
[    2.589508] uhci_hcd: USB Universal Host Controller Interface driver
[    2.589593] uhci_hcd 0000:00:1a.0: UHCI Host Controller
[    2.589681] uhci_hcd 0000:00:1a.0: new USB bus registered, assigned bus number 3
[    2.589721] uhci_hcd 0000:00:1a.0: irq 20, io base 0x00001860
[    2.589771] usb usb3: New USB device found, idVendor=1d6b, idProduct=0001
[    2.589774] usb usb3: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.589776] usb usb3: Product: UHCI Host Controller
[    2.589778] usb usb3: Manufacturer: Linux 4.6.2-t61 uhci_hcd
[    2.589780] usb usb3: SerialNumber: 0000:00:1a.0
[    2.589926] hub 3-0:1.0: USB hub found
[    2.589934] hub 3-0:1.0: 2 ports detected
[    2.590139] uhci_hcd 0000:00:1a.1: UHCI Host Controller
[    2.590216] uhci_hcd 0000:00:1a.1: new USB bus registered, assigned bus number 4
[    2.590272] uhci_hcd 0000:00:1a.1: irq 21, io base 0x00001880
[    2.590321] usb usb4: New USB device found, idVendor=1d6b, idProduct=0001
[    2.590323] usb usb4: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.590325] usb usb4: Product: UHCI Host Controller
[    2.590327] usb usb4: Manufacturer: Linux 4.6.2-t61 uhci_hcd
[    2.590329] usb usb4: SerialNumber: 0000:00:1a.1
[    2.590482] hub 4-0:1.0: USB hub found
[    2.590489] hub 4-0:1.0: 2 ports detected
[    2.590673] uhci_hcd 0000:00:1d.0: UHCI Host Controller
[    2.590746] uhci_hcd 0000:00:1d.0: new USB bus registered, assigned bus number 5
[    2.590778] uhci_hcd 0000:00:1d.0: irq 16, io base 0x000018a0
[    2.590931] usb usb5: New USB device found, idVendor=1d6b, idProduct=0001
[    2.590935] usb usb5: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.590937] usb usb5: Product: UHCI Host Controller
[    2.590939] usb usb5: Manufacturer: Linux 4.6.2-t61 uhci_hcd
[    2.590941] usb usb5: SerialNumber: 0000:00:1d.0
[    2.591075] hub 5-0:1.0: USB hub found
[    2.591083] hub 5-0:1.0: 2 ports detected
[    2.591270] uhci_hcd 0000:00:1d.1: UHCI Host Controller
[    2.591326] uhci_hcd 0000:00:1d.1: new USB bus registered, assigned bus number 6
[    2.591361] uhci_hcd 0000:00:1d.1: irq 17, io base 0x000018c0
[    2.591484] usb usb6: New USB device found, idVendor=1d6b, idProduct=0001
[    2.591486] usb usb6: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.591489] usb usb6: Product: UHCI Host Controller
[    2.591491] usb usb6: Manufacturer: Linux 4.6.2-t61 uhci_hcd
[    2.591492] usb usb6: SerialNumber: 0000:00:1d.1
[    2.591621] hub 6-0:1.0: USB hub found
[    2.591629] hub 6-0:1.0: 2 ports detected
[    2.591818] uhci_hcd 0000:00:1d.2: UHCI Host Controller
[    2.591875] uhci_hcd 0000:00:1d.2: new USB bus registered, assigned bus number 7
[    2.591918] uhci_hcd 0000:00:1d.2: irq 18, io base 0x000018e0
[    2.592035] usb usb7: New USB device found, idVendor=1d6b, idProduct=0001
[    2.592037] usb usb7: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    2.592039] usb usb7: Product: UHCI Host Controller
[    2.592041] usb usb7: Manufacturer: Linux 4.6.2-t61 uhci_hcd
[    2.592043] usb usb7: SerialNumber: 0000:00:1d.2
[    2.592168] hub 7-0:1.0: USB hub found
[    2.592176] hub 7-0:1.0: 2 ports detected
[    2.592325] usbcore: registered new interface driver usblp
[    2.592340] usbcore: registered new interface driver uas
[    2.592381] usbcore: registered new interface driver usb-storage
[    2.592425] i8042: PNP: PS/2 Controller [PNP0303:KBD,PNP0f13:MOU] at 0x60,0x64 irq 1,12
[    2.601532] serio: i8042 KBD port at 0x60,0x64 irq 1
[    2.601581] serio: i8042 AUX port at 0x60,0x64 irq 12
[    2.601732] mousedev: PS/2 mouse device common for all mice
[    2.603093] rtc_cmos 00:02: RTC can wake from S4
[    2.603288] rtc_cmos 00:02: rtc core: registered rtc_cmos as rtc0
[    2.603328] rtc_cmos 00:02: alarms up to one month, y3k, 114 bytes nvram, hpet irqs
[    2.603467] i801_smbus 0000:00:1f.3: SMBus using PCI interrupt
[    2.605307] md: linear personality registered for level -1
[    2.605311] md: raid0 personality registered for level 0
[    2.605313] md: raid1 personality registered for level 1
[    2.605316] md: raid10 personality registered for level 10
[    2.605384] md: raid6 personality registered for level 6
[    2.605386] md: raid5 personality registered for level 5
[    2.605387] md: raid4 personality registered for level 4
[    2.605390] md: multipath personality registered for level -4
[    2.605393] md: faulty personality registered for level -5
[    2.605601] device-mapper: ioctl: 4.34.0-ioctl (2015-10-28) initialised: dm-devel@redhat.com
[    2.605631] usbcore: registered new interface driver btusb
[    2.605644] sdhci: Secure Digital Host Controller Interface driver
[    2.605646] sdhci: Copyright(c) Pierre Ossman
[    2.605668] sdhci-pci 0000:15:00.2: SDHCI controller found [1180:0822] (rev 21)
[    2.606746] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.607767] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.608838] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.610051] mmc0: SDHCI controller on PCI [0000:15:00.2] using DMA
[    2.610121] hidraw: raw HID events driver (C) Jiri Kosina
[    2.610237] usbcore: registered new interface driver usbhid
[    2.610238] usbhid: USB HID core driver
[    2.610343] thinkpad_acpi: ThinkPad ACPI Extras v0.25
[    2.610344] thinkpad_acpi: http://ibm-acpi.sf.net/
[    2.610346] thinkpad_acpi: ThinkPad BIOS 7LETC9WW (2.29 ), EC 7KHT24WW-1.08
[    2.610347] thinkpad_acpi: Lenovo ThinkPad T61, model 64576PG
[    2.610828] input: AT Translated Set 2 keyboard as /devices/platform/i8042/serio0/input/input4
[    2.612937] thinkpad_acpi: ACPI backlight control delay disabled
[    2.613104] thinkpad_acpi: radio switch found; radios are enabled
[    2.613132] thinkpad_acpi: This ThinkPad has standard ACPI backlight brightness control, supported by the ACPI video driver
[    2.613135] thinkpad_acpi: Disabling thinkpad-acpi brightness events by default...
[    2.615694] thinkpad_acpi: rfkill switch tpacpi_bluetooth_sw: radio is unblocked
[    2.616537] thinkpad_acpi: warning: userspace override of important firmware LEDs is enabled
[    2.621246] thinkpad_acpi: Standard ACPI backlight interface available, not loading native one
[    2.622990] input: ThinkPad Extra Buttons as /devices/platform/thinkpad_acpi/input/input6
[    2.623067] hdaps: inverting axis (3) readings
[    2.623069] hdaps: LENOVO ThinkPad T61 detected
[    2.623652] input: hdaps as /devices/platform/hdaps/input/input8
[    2.623733] hdaps: driver successfully loaded
[    2.624642] snd_hda_intel 0000:00:1b.0: probe_mask set to 0x1 for device 17aa:20ac
[    2.624694] Netfilter messages via NETLINK v0.30.
[    2.624711] nf_conntrack version 0.5.0 (16384 buckets, 65536 max)
[    2.624866] ctnetlink v0.93: registering with nfnetlink.
[    2.625060] ip_tables: (C) 2000-2006 Netfilter Core Team
[    2.625086] Initializing XFRM netlink socket
[    2.625258] NET: Registered protocol family 10
[    2.625645] ip6_tables: (C) 2000-2006 Netfilter Core Team
[    2.625906] sit: IPv6 over IPv4 tunneling driver
[    2.626092] NET: Registered protocol family 17
[    2.626136] Bluetooth: RFCOMM TTY layer initialized
[    2.626140] Bluetooth: RFCOMM socket layer initialized
[    2.626146] Bluetooth: RFCOMM ver 1.11
[    2.626157] Key type dns_resolver registered
[    2.627078] microcode: CPU0 sig=0x10676, pf=0x80, revision=0x60f
[    2.627086] microcode: CPU1 sig=0x10676, pf=0x80, revision=0x60f
[    2.627124] microcode: Microcode Update Driver: v2.01 <tigran@aivazian.fsnet.co.uk>, Peter Oruba
[    2.627373] registered taskstats version 1
[    2.628103] ALSA device list:
[    2.628105]   No soundcards found.
[    2.629457] Freeing unused kernel memory: 908K (ffffffff81ebd000 - ffffffff81fa0000)
[    2.629459] Write protecting the kernel read-only data: 14336k
[    2.630242] Freeing unused kernel memory: 1224K (ffff8800018ce000 - ffff880001a00000)
[    2.631829] Freeing unused kernel memory: 512K (ffff880001d80000 - ffff880001e00000)
[    2.661300] random: udevadm urandom read with 18 bits of entropy available
[    2.671369] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.725476] udevadm (1231) used greatest stack depth: 13000 bytes left
[    2.733198] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.745315] e1000e 0000:00:19.0 enp0s25: renamed from eth0
[    2.750220] iwl4965 0000:03:00.0 wlp3s0: renamed from wlan0
[    2.799849] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.866273] sdhci-pci 0000:15:00.2: Will use DMA mode even though HW doesn't fully claim to support it.
[    2.947137] firewire_core 0000:15:00.1: created device fw0: GUID 00061b032a251d75, S400
[    2.990627] snd_hda_codec_analog hdaudioC0D0: autoconfig for AD1984: line_outs=1 (0x12/0x0/0x0/0x0/0x0) type:speaker
[    2.990632] snd_hda_codec_analog hdaudioC0D0:    speaker_outs=0 (0x0/0x0/0x0/0x0/0x0)
[    2.990635] snd_hda_codec_analog hdaudioC0D0:    hp_outs=1 (0x11/0x0/0x0/0x0/0x0)
[    2.990637] snd_hda_codec_analog hdaudioC0D0:    mono: mono_out=0x0
[    2.990639] snd_hda_codec_analog hdaudioC0D0:    dig-out=0x1b/0x0
[    2.990641] snd_hda_codec_analog hdaudioC0D0:    inputs:
[    2.990643] snd_hda_codec_analog hdaudioC0D0:      Internal Mic=0x15
[    2.990645] snd_hda_codec_analog hdaudioC0D0:      Mic=0x14
[    2.990647] snd_hda_codec_analog hdaudioC0D0:      Dock Mic=0x1c
[    2.998166] input: HDA Intel Mic as /devices/pci0000:00/0000:00:1b.0/sound/card0/input9
[    2.998241] input: HDA Intel Dock Mic as /devices/pci0000:00/0000:00:1b.0/sound/card0/input10
[    2.998306] input: HDA Intel Headphone as /devices/pci0000:00/0000:00:1b.0/sound/card0/input11
[    3.059053] usb 3-1: new full-speed USB device number 2 using uhci_hcd
[    3.065045] usb 6-2: new full-speed USB device number 2 using uhci_hcd
[    3.067680] EXT4-fs (sda1): mounted filesystem with ordered data mode. Opts: (null)
[    3.160538] systemd[1]: systemd 229 running in system mode. (+PAM +AUDIT +SELINUX +IMA +APPARMOR +SMACK +SYSVINIT +UTMP +LIBCRYPTSETUP +GCRYPT +GNUTLS +ACL +XZ -LZ4 +SECCOMP +BLKID +ELFUTILS +KMOD -IDN)
[    3.160661] systemd[1]: Detected architecture x86-64.
[    3.160927] systemd[1]: Set hostname to <thinkpad>.
[    3.177157] systemd-rc-loca (1327) used greatest stack depth: 12936 bytes left
[    3.218094] usb 3-1: New USB device found, idVendor=0a5c, idProduct=2110
[    3.218102] usb 3-1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    3.218106] usb 3-1: Product: BCM2045B
[    3.218110] usb 3-1: Manufacturer: Broadcom Corp
[    3.240591] usb 6-2: New USB device found, idVendor=17ef, idProduct=1003
[    3.240599] usb 6-2: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    3.240603] usb 6-2: Product: Integrated Smart Card Reader
[    3.240608] usb 6-2: Manufacturer: Lenovo
[    3.247337] systemd[1]: Listening on udev Kernel Socket.
[    3.247432] systemd[1]: Listening on /dev/initctl Compatibility Named Pipe.
[    3.247452] systemd[1]: Reached target Remote File Systems (Pre).
[    3.247469] systemd[1]: Reached target Remote File Systems.
[    3.247537] systemd[1]: Created slice System Slice.
[    3.247626] systemd[1]: Listening on Journal Audit Socket.
[    3.247669] systemd[1]: Listening on Journal Socket (/dev/log).
[    3.247807] systemd[1]: Set up automount Arbitrary Executable File Formats File System Automount Point.
[    3.247860] systemd[1]: Started Forward Password Requests to Wall Directory Watch.
[    3.247913] systemd[1]: Created slice system-getty.slice.
[    3.247958] systemd[1]: Listening on udev Control Socket.
[    3.247998] systemd[1]: Created slice User and Session Slice.
[    3.248039] systemd[1]: Reached target Slices.
[    3.248072] systemd[1]: Listening on fsck to fsckd communication Socket.
[    3.248109] systemd[1]: Listening on Syslog Socket.
[    3.248124] systemd[1]: Reached target Encrypted Volumes.
[    3.248181] systemd[1]: Listening on Journal Socket.
[    3.252189] systemd[1]: Starting Braille Device Support...
[    3.252669] systemd[1]: Mounting Debug File System...
[    3.254604] systemd[1]: Mounting Huge Pages File System...
[    3.256968] systemd[1]: Starting Load Kernel Modules...
[    3.257649] systemd[1]: Starting Uncomplicated firewall...
[    3.258352] systemd[1]: Starting Journal Service...
[    3.259075] systemd[1]: Started Read required files in advance.
[    3.260709] systemd[1]: Mounting POSIX Message Queue File System...
[    3.261465] systemd[1]: Starting Nameserver information manager...
[    3.261933] systemd[1]: Reached target User and Group Name Lookups.
[    3.262698] systemd[1]: Starting Create list of required static device nodes for the current kernel...
[    3.264574] systemd[1]: Started Uncomplicated firewall.
[    3.269962] systemd[1]: Mounted Huge Pages File System.
[    3.270094] systemd[1]: Mounted Debug File System.
[    3.270517] systemd[1]: Started Load Kernel Modules.
[    3.274710] systemd[1]: Mounted POSIX Message Queue File System.
[    3.276407] systemd[1]: Started Create list of required static device nodes for the current kernel.
[    3.290250] systemd[1]: Started Nameserver information manager.
[    3.290895] systemd[1]: Started Braille Device Support.
[    3.301563] systemd[1]: ureadahead.service: Main process exited, code=exited, status=5/NOTINSTALLED
[    3.302777] systemd[1]: ureadahead.service: Unit entered failed state.
[    3.302820] systemd[1]: ureadahead.service: Failed with result 'exit-code'.
[    3.326211] systemd[1]: Starting Create Static Device Nodes in /dev...
[    3.326875] systemd[1]: Starting Apply Kernel Variables...
[    3.327379] systemd[1]: Mounting FUSE Control File System...
[    3.327439] psmouse serio1: synaptics: Touchpad model: 1, fw: 6.2, id: 0x81a0b1, caps: 0xa04793/0x300000/0x0/0x0, board id: 0, fw id: 67352
[    3.327445] psmouse serio1: synaptics: serio: Synaptics pass-through port at isa0060/serio1/input0
[    3.334035] systemd[1]: Mounted FUSE Control File System.
[    3.339303] systemd[1]: Started Apply Kernel Variables.
[    3.339516] systemd[1]: Started Create Static Device Nodes in /dev.
[    3.343281] systemd[1]: Starting udev Kernel Device Manager...
[    3.352926] systemd[1]: Started Journal Service.
[    3.372996] input: SynPS/2 Synaptics TouchPad as /devices/platform/i8042/serio1/input/input7
[    3.400564] EXT4-fs (sda1): re-mounted. Opts: discard,errors=remount-ro
[    3.419260] systemd-journald[1343]: Received request to flush runtime journal from PID 1
[    3.426118] usb 3-2: new full-speed USB device number 3 using uhci_hcd
[    3.588673] usb 3-2: New USB device found, idVendor=0483, idProduct=2016
[    3.588678] usb 3-2: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[    3.588680] usb 3-2: Product: Biometric Coprocessor
[    3.588683] usb 3-2: Manufacturer: STMicroelectronics
[    3.781623] pcmcia_socket pcmcia_socket0: cs: memory probe 0x0c0000-0x0fffff:
[    3.781633]  excluding 0xc0000-0xd3fff 0xe0000-0xfffff
[    3.781655] pcmcia_socket pcmcia_socket0: cs: memory probe 0xa0000000-0xa0ffffff:
[    3.781666]  excluding 0xa0000000-0xa0ffffff
[    3.781682] pcmcia_socket pcmcia_socket0: cs: memory probe 0x60000000-0x60ffffff:
[    3.781691]  excluding 0x60000000-0x60ffffff
[    3.827657] random: nonblocking pool is initialized
[    3.968601] Adding 3125244k swap on /dev/sda5.  Priority:-1 extents:1 across:3125244k SS
[    4.054979] cgroup: new mount options do not match the existing superblock, will be ignored
[    4.072794] psmouse serio2: trackpoint: IBM TrackPoint firmware: 0x0e, buttons: 3/3
[    4.307820] input: TPPS/2 IBM TrackPoint as /devices/platform/i8042/serio1/serio2/input/input12
[    4.552415] IPv6: ADDRCONF(NETDEV_UP): wlp3s0: link is not ready
[    4.813907] IPv6: ADDRCONF(NETDEV_UP): wlp3s0: link is not ready
[    4.821928] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
[    5.294275] IPv6: ADDRCONF(NETDEV_UP): enp0s25: link is not ready
[    5.476932] IPv6: ADDRCONF(NETDEV_UP): wlp3s0: link is not ready
[    7.721246] wlp3s0: authenticate with f0:7d:68:14:70:f0
[    7.732511] wlp3s0: send auth to f0:7d:68:14:70:f0 (try 1/3)
[    7.734691] wlp3s0: authenticated
[    7.735026] wlp3s0: associate with f0:7d:68:14:70:f0 (try 1/3)
[    7.739132] wlp3s0: RX AssocResp from f0:7d:68:14:70:f0 (capab=0x431 status=0 aid=1)
[    7.765996] wlp3s0: associated
```





