# 系统信息命令执行结果

## 1. `dmesg` 命令输出

显示内核环形缓冲区消息：

```
[    0.000000] Linux version 6.12.8+ (ubuntu@ip-10-0-0-10) (gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0, GNU ld (GNU Binutils for Ubuntu) 2.38) #11 SMP PREEMPT_DYNAMIC Sun Jul  6 04:56:39 UTC 2025
[    0.000000] Command line: console=ttyS0 root=/dev/vda random.trust_cpu=on ip=172.30.0.2::172.30.0.1:255.255.255.0::eth0:off rw cgroup_enable=memory swapaccount=1 systemd.unified_cgroup_hierarchy=0 rc_cgroup_mode=hybrid clocksource=kvm-clock lapic=notscdeadline rcupdate.rcu_cpu_stall_suppress_at_boot root=/dev/vda rw virtio_mmio.device=4K@0xd0000000:5 virtio_mmio.device=4K@0xd0001000:6 virtio_mmio.device=4K@0xd0002000:7
[    0.000000] x86/split lock detection: #DB: warning on user-space bus_locks
[    0.000000] BIOS-provided physical RAM map:
[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009fbff] usable
[    0.000000] BIOS-e820: [mem 0x000000000009fc00-0x00000000000fffff] reserved
[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x00000000cfffffff] usable
[    0.000000] BIOS-e820: [mem 0x0000000100000000-0x000000042fffffff] usable
[    0.000000] NX (Execute Disable) protection: active
[    0.000000] APIC: Static calls initialized
[    0.000000] DMI not present or invalid.
[    0.000000] Hypervisor detected: KVM
[    0.000000] kvm-clock: Using msrs 4b564d01 and 4b564d00
[    0.000000] kvm-clock: using sched offset of 40471302 cycles
[    0.000005] clocksource: kvm-clock: mask: 0xffffffffffffffff max_cycles: 0x1cd42e4dffb, max_idle_ns: 881590591483 ns
[    0.000015] tsc: Detected 2400.000 MHz processor
[    0.000098] e820: update [mem 0x00000000-0x00000fff] usable ==> reserved
[    0.000100] e820: remove [mem 0x000a0000-0x000fffff] usable
[    0.000103] last_pfn = 0x430000 max_arch_pfn = 0x400000000
[    0.000135] MTRRs disabled by BIOS
[    0.000142] x86/PAT: Configuration [0-7]: WB  WC  UC- UC  WB  WP  UC- WT  
[    0.000150] last_pfn = 0xd0000 max_arch_pfn = 0x400000000
[    0.000179] found SMP MP-table at [mem 0x0009fc00-0x0009fc0f]
[    0.000197] Using GB pages for direct mapping
[    0.000384] ACPI: Early table checksum verification disabled
[    0.000415] ACPI: RSDP 0x00000000000E0000 000024 (v02 FIRECK)
[    0.000423] ACPI: XSDT 0x00000000000A01CB 000034 (v01 FIRECK FCMVXSDT 00000000 FCAT 20240119)
[    0.000436] ACPI: FACP 0x00000000000A005F 000114 (v06 FIRECK FCVMFADT 00000000 FCAT 20240119)
[    0.000443] ACPI: DSDT 0x000000000009FD6C 0002F3 (v02 FIRECK FCVMDSDT 00000000 FCAT 20240119)
[    0.000447] ACPI: APIC 0x00000000000A0173 000058 (v06 FIRECK FCVMMADT 00000000 FCAT 20240119)
[    0.000449] ACPI: Reserving FACP table memory at [mem 0xa005f-0xa0172]
[    0.000450] ACPI: Reserving DSDT table memory at [mem 0x9fd6c-0xa005e]
[    0.000451] ACPI: Reserving APIC table memory at [mem 0xa0173-0xa01ca]
[    0.000691] No NUMA configuration found
[    0.000691] Faking a node at [mem 0x0000000000000000-0x000000042fffffff]
[    0.000697] NODE_DATA(0) allocated [mem 0x42ffdd3c0-0x42fffefff]
[    0.000823] Zone ranges:
[    0.000827]   DMA      [mem 0x0000000000001000-0x0000000000ffffff]
[    0.000828]   DMA32    [mem 0x0000000001000000-0x00000000ffffffff]
[    0.000830]   Normal   [mem 0x0000000100000000-0x000000042fffffff]
[    0.000833] Movable zone start for each node
[    0.000835] Early memory node ranges
[    0.000835]   node   0: [mem 0x0000000000001000-0x000000000009efff]
[    0.000838]   node   0: [mem 0x0000000000100000-0x00000000cfffffff]
[    0.000839]   node   0: [mem 0x0000000100000000-0x000000042fffffff]
[    0.000841] Initmem setup node 0 [mem 0x0000000000001000-0x000000042fffffff]
[    0.000856] On node 0, zone DMA: 1 pages in unavailable ranges
[    0.000992] On node 0, zone DMA: 97 pages in unavailable ranges
[    0.032850] IOAPIC[0]: apic_id 0, version 17, address 0xfec00000, GSI 0-23
[    0.032858] ACPI: Using ACPI (MADT) for SMP configuration information
[    0.032867] CPU topo: Max. logical packages:   1
[    0.032869] CPU topo: Max. logical dies:       1
[    0.032870] CPU topo: Max. dies per package:   1
[    0.032875] CPU topo: Max. threads per core:   1
[    0.032876] CPU topo: Num. cores per package:     4
[    0.032877] CPU topo: Num. threads per package:   4
[    0.032878] CPU topo: Allowing 4 present CPUs plus 0 hotplug CPUs
[    0.032897] kvm-guest: APIC: eoi() replaced with kvm_guest_apic_eoi_write()
[    0.032927] kvm-guest: KVM setup pv remote TLB flush
[    0.032930] kvm-guest: setup PV sched yield
[    0.032941] PM: hibernation: Registered nosave memory: [mem 0x00000000-0x00000fff]
[    0.032944] PM: hibernation: Registered nosave memory: [mem 0x0009f000-0x0009ffff]
[    0.032944] PM: hibernation: Registered nosave memory: [mem 0x000a0000-0x000fffff]
[    0.032945] PM: hibernation: Registered nosave memory: [mem 0xd0000000-0xffffffff]
[    0.032947] [mem 0xd0000000-0xffffffff] available for PCI devices
[    0.032948] Booting paravirtualized kernel on KVM
[    0.032949] clocksource: refined-jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645519600211568 ns
[    0.032960] setup_percpu: NR_CPUS:128 nr_cpumask_bits:4 nr_cpu_ids:4 nr_node_ids:1
[    0.034236] percpu: Embedded 58 pages/cpu s199448 r8192 d29928 u524288
[    0.034244] pcpu-alloc: s199448 r8192 d29928 u524288 alloc=1*2097152
[    0.034246] pcpu-alloc: [0] 0 1 2 3 
[    0.034275] kvm-guest: PV spinlocks enabled
[    0.034279] PV qspinlock hash table entries: 256 (order: 0, 4096 bytes, linear)
[    0.034282] Kernel command line: console=ttyS0 root=/dev/vda random.trust_cpu=on ip=172.30.0.2::172.30.0.1:255.255.255.0::eth0:off rw cgroup_enable=memory swapaccount=1 systemd.unified_cgroup_hierarchy=0 rc_cgroup_mode=hybrid clocksource=kvm-clock lapic=notscdeadline rcupdate.rcu_cpu_stall_suppress_at_boot root=/dev/vda rw virtio_mmio.device=4K@0xd0000000:5 virtio_mmio.device=4K@0xd0001000:6 virtio_mmio.device=4K@0xd0002000:7
[    0.034503] Booting kernel: `' invalid for parameter `rcupdate.rcu_cpu_stall_suppress_at_boot'
[    0.034519] Unknown kernel command line parameters "cgroup_enable=memory rc_cgroup_mode=hybrid", will be passed to user space.
[    0.034537] random: crng init done
[    0.043729] Dentry cache hash table entries: 2097152 (order: 12, 16777216 bytes, linear)
[    0.048312] Inode-cache hash table entries: 1048576 (order: 11, 8388608 bytes, linear)
[    0.048388] Fallback order for Node 0: 0 
[    0.048397] Built 1 zonelists, mobility grouping on.  Total pages: 4194206
[    0.048398] Policy zone: Normal
[    0.048399] mem auto-init: stack:off, heap alloc:off, heap free:off
[    0.048405] software IO TLB: area num 4.
[    0.103654] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=4, Nodes=1
[    0.103743] ftrace: allocating 52027 entries in 204 pages
[    0.117998] ftrace: allocated 204 pages with 4 groups
[    0.118899] Dynamic Preempt: none
[    0.119005] rcu: Preemptible hierarchical RCU implementation.
[    0.119007] rcu:     RCU restricting CPUs from NR_CPUS=128 to nr_cpu_ids=4.
[    0.119010]  Trampoline variant of Tasks RCU enabled.
[    0.119012]  Rude variant of Tasks RCU enabled.
[    0.119012]  Tracing variant of Tasks RCU enabled.
[    0.119013] rcu: RCU calculated value of scheduler-enlistment delay is 25 jiffies.
[    0.119014] rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=4
[    0.119020] RCU Tasks: Setting shift to 2 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=4.
[    0.119022] RCU Tasks Rude: Setting shift to 2 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=4.
[    0.119024] RCU Tasks Trace: Setting shift to 2 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=4.
[    0.121792] NR_IRQS: 8448, nr_irqs: 440, preallocated irqs: 0
[    0.121832] rcu: srcu_init: Setting srcu_struct sizes based on contention.
[    0.121906] Console: colour dummy device 80x25
[    0.121946] printk: legacy console [ttyS0] enabled
[    0.166107] ACPI: Core revision 20240827
[    0.166391] APIC: Switch to symmetric I/O mode setup
[    0.166860] x2apic enabled
[    0.167239] APIC: Switched APIC routing to: physical x2apic
[    0.167606] kvm-guest: APIC: send_IPI_mask() replaced with kvm_send_ipi_mask()
[    0.168097] kvm-guest: APIC: send_IPI_mask_allbutself() replaced with kvm_send_ipi_mask_allbutself()
[    0.168722] kvm-guest: setup PV IPIs
[    0.168989] clocksource: tsc-early: mask: 0xffffffffffffffff max_cycles: 0x22983777dd9, max_idle_ns: 440795300422 ns
[    0.169678] Calibrating delay loop (skipped) preset value.. 4800.00 BogoMIPS (lpj=9600000)
[    0.170312] x86/cpu: User Mode Instruction Prevention (UMIP) activated
[    0.170757] Last level iTLB entries: 4KB 0, 2MB 0, 4MB 0
[    0.171114] Last level dTLB entries: 4KB 0, 2MB 0, 4MB 0, 1GB 0
[    0.171513] Spectre V1 : Mitigation: usercopy/swapgs barriers and __user pointer sanitization
[    0.172080] Spectre V2 : Mitigation: Enhanced / Automatic IBRS
[    0.172450] Spectre V2 : Spectre v2 / SpectreRSB mitigation: Filling RSB on context switch
[    0.172980] Spectre V2 : Spectre v2 / PBRSB-eIBRS: Retire a single CALL on VMEXIT
[    0.173436] Spectre V2 : mitigation: Enabling conditional Indirect Branch Prediction Barrier
[    0.173676] Speculative Store Bypass: Mitigation: Speculative Store Bypass disabled via prctl
[    0.173676] TAA: Mitigation: TSX disabled
[    0.173676] x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x002: 'SSE registers'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x004: 'AVX registers'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x020: 'AVX-512 opmask'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x040: 'AVX-512 Hi256'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x080: 'AVX-512 ZMM_Hi256'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x200: 'Protection Keys User registers'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x20000: 'AMX Tile config'
[    0.173676] x86/fpu: Supporting XSAVE feature 0x40000: 'AMX Tile data'
[    0.173676] x86/fpu: xstate_offset[2]:  576, xstate_sizes[2]:  256
[    0.173676] x86/fpu: xstate_offset[5]:  832, xstate_sizes[5]:   64
[    0.173676] x86/fpu: xstate_offset[6]:  896, xstate_sizes[6]:  512
[    0.173676] x86/fpu: xstate_offset[7]: 1408, xstate_sizes[7]: 1024
[    0.173676] x86/fpu: xstate_offset[9]: 2432, xstate_sizes[9]:    8
[    0.173676] x86/fpu: xstate_offset[17]: 2496, xstate_sizes[17]:   64
[    0.173676] x86/fpu: xstate_offset[18]: 2560, xstate_sizes[18]: 8192
[    0.173676] x86/fpu: Enabled xstate features 0x602e7, context size is 10752 bytes, using 'compacted' format.
[    0.173676] Freeing SMP alternatives memory: 48K
[    0.173676] pid_max: default: 32768 minimum: 301
[    0.173676] LSM: initializing lsm=capability,selinux
[    0.173676] SELinux:  Initializing.
[    0.173676] Mount-cache hash table entries: 32768 (order: 6, 262144 bytes, linear)
[    0.173676] Mountpoint-cache hash table entries: 32768 (order: 6, 262144 bytes, linear)
[    0.173676] smpboot: CPU0: Intel(R) Xeon(R) Processor (family: 0x6, model: 0xcf, stepping: 0x2)
[    0.173676] Performance Events: unsupported p6 CPU model 207 no PMU driver, software events only.
[    0.173676] signal: max sigframe size: 11952
[    0.173676] rcu: Hierarchical SRCU implementation.
[    0.173676] rcu:     Max phase no-delay instances is 1000.
[    0.173676] Timer migration: 1 hierarchy levels; 8 children per group; 1 crossnode level
[    0.173676] smp: Bringing up secondary CPUs ...
[    0.173676] smpboot: x86: Booting SMP configuration:
[    0.173676] .... node  #0, CPUs:      #1 #2 #3
[    0.181985] smp: Brought up 1 node, 4 CPUs
[    0.182216] smpboot: Total of 4 processors activated (19200.00 BogoMIPS)
[    0.232378] node 0 deferred pages initialised in 48ms
[    0.232382] Memory: 16373680K/16776824K available (18432K kernel code, 9122K rwdata, 5448K rodata, 3892K init, 5228K bss, 397768K reserved, 0K cma-reserved)
[    0.234184] devtmpfs: initialized
[    0.234184] x86/mm: Memory block size: 128MB
[    0.235027] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645041785100000 ns
[    0.235027] futex hash table entries: 1024 (order: 4, 65536 bytes, linear)
[    0.238653] NET: Registered PF_NETLINK/PF_ROUTE protocol family
[    0.239076] audit: initializing netlink subsys (disabled)
[    0.239398] audit: type=2000 audit(1752817336.362:1): state=initialized audit_enabled=0 res=1
[    0.239398] thermal_sys: Registered thermal governor 'fair_share'
[    0.239398] thermal_sys: Registered thermal governor 'step_wise'
[    0.239398] thermal_sys: Registered thermal governor 'user_space'
[    0.239398] cpuidle: using governor ladder
[    0.241682] cpuidle: using governor menu
[    0.242363] ACPI FADT declares the system doesn't support MSI, so disable it
[    0.242778] ACPI FADT declares the system doesn't support PCIe ASPM, so disable it
[    0.243210] acpiphp: ACPI Hot Plug PCI Controller Driver version: 0.5
[    0.245679] PCI: Fatal: No config space access function found
[    0.247117] kprobes: kprobe jump-optimization is enabled. All kprobes are optimized if possible.
[    0.250075] HugeTLB: registered 1.00 GiB page size, pre-allocated 0 pages
[    0.250450] HugeTLB: 16380 KiB vmemmap can be freed for a 1.00 GiB page
[    0.250833] HugeTLB: registered 2.00 MiB page size, pre-allocated 0 pages
[    0.251227] HugeTLB: 28 KiB vmemmap can be freed for a 2.00 MiB page
[    0.251622] ACPI: Added _OSI(Module Device)
[    0.251622] ACPI: Added _OSI(Processor Device)
[    0.251622] ACPI: Added _OSI(3.0 _SCP Extensions)
[    0.251622] ACPI: Added _OSI(Processor Aggregator Device)
[    0.251622] ACPI: 1 ACPI AML tables successfully acquired and loaded
[    0.269975] ACPI: Interpreter enabled
[    0.269975] ACPI: PM: (supports S0)
[    0.270137] ACPI: Using IOAPIC for interrupt routing
[    0.270415] PCI: Using host bridge windows from ACPI; if necessary, use "pci=nocrs" and report a bug
[    0.270947] PCI: Using E820 reservations for host bridge windows
[    0.271646] iommu: Default domain type: Translated
[    0.271927] iommu: DMA domain TLB invalidation policy: lazy mode
[    0.272330] SCSI subsystem initialized
[    0.272551] pps_core: LinuxPPS API ver. 1 registered
[    0.273681] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    0.274202] PTP clock support registered
[    0.274757] NetLabel: Initializing
[    0.274953] NetLabel:  domain hash size = 128
[    0.275224] NetLabel:  protocols = UNLABELED CIPSOv4 CALIPSO
[    0.275571] NetLabel:  unlabeled traffic allowed by default
[    0.275906] PCI: Using ACPI for IRQ routing
[    0.276149] PCI: System does not support PCI
[    0.276415] vgaarb: loaded
[    0.276415] clocksource: Switched to clocksource kvm-clock
[    0.335374] VFS: Disk quotas dquot_6.6.0
[    0.335597] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
[    0.336034] netfs: FS-Cache loaded
[    0.336243] pnp: PnP ACPI init
[    0.336489] pnp: PnP ACPI: found 5 devices
[    0.339437] NET: Registered PF_INET protocol family
[    0.340807] IP idents hash table entries: 262144 (order: 9, 2097152 bytes, linear)
[    0.342852] tcp_listen_portaddr_hash hash table entries: 8192 (order: 5, 131072 bytes, linear)
[    0.343395] Table-perturb hash table entries: 65536 (order: 6, 262144 bytes, linear)
[    0.343836] TCP established hash table entries: 131072 (order: 8, 1048576 bytes, linear)
[    0.344903] TCP bind hash table entries: 65536 (order: 9, 2097152 bytes, linear)
[    0.346393] TCP: Hash tables configured (established 131072 bind 65536)
[    0.346838] UDP hash table entries: 8192 (order: 6, 262144 bytes, linear)
[    0.347373] UDP-Lite hash table entries: 8192 (order: 6, 262144 bytes, linear)
[    0.347973] NET: Registered PF_UNIX/PF_LOCAL protocol family
[    0.349113] RPC: Registered named UNIX socket transport module.
[    0.349485] RPC: Registered udp transport module.
[    0.349771] RPC: Registered tcp transport module.
[    0.350061] RPC: Registered tcp-with-tls transport module.
[    0.350378] RPC: Registered tcp NFSv4.1 backchannel transport module.
[    0.350749] PCI: CLS 0 bytes, default 64
[    0.350988] PCI-DMA: Using software bounce buffering for IO (SWIOTLB)
[    0.351360] software IO TLB: mapped [mem 0x00000000cc000000-0x00000000d0000000] (64MB)
[    0.351861] virtio-mmio: Registering device virtio-mmio.0 at 0xd0000000-0xd0000fff, IRQ 5.
[    0.352348] virtio-mmio: Registering device virtio-mmio.1 at 0xd0001000-0xd0001fff, IRQ 6.
[    0.352819] virtio-mmio: Registering device virtio-mmio.2 at 0xd0002000-0xd0002fff, IRQ 7.
[    0.354066] RAPL PMU: API unit is 2^-32 Joules, 1 fixed counters, 10737418240 ms ovfl timer
[    0.354559] RAPL PMU: hw unit of domain psys 2^-0 Joules
[    0.354886] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x22983777dd9, max_idle_ns: 440795300422 ns
[    0.355479] platform rtc_cmos: registered platform RTC device (no PNP device found)
[    0.358059] Initialise system trusted keyrings
[    0.358319] Key type blacklist registered
[    0.358617] workingset: timestamp_bits=36 max_order=22 bucket_order=0
[    0.359012] zbud: loaded
[    0.359261] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.359699] NFS: Registering the id_resolver key type
[    0.360003] Key type id_resolver registered
[    0.360257] Key type id_legacy registered
[    0.360500] nfs4filelayout_init: NFSv4 File Layout Driver Registering...
[    0.360883] nfs4flexfilelayout_init: NFSv4 Flexfile Layout Driver Registering...
[    0.361525] fuse: init (API version 7.41)
[    0.361797] ceph: loaded (mds proto 32)
[    0.367550] NET: Registered PF_ALG protocol family
[    0.367811] Key type asymmetric registered
[    0.368053] Asymmetric key parser 'x509' registered
[    0.368372] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 252)
[    0.370263] virtio-mmio virtio-mmio.0: error -EBUSY: can't request region for resource [mem 0xd0000000-0xd0000fff]
[    0.370839] virtio-mmio virtio-mmio.0: probe with driver virtio-mmio failed with error -16
[    0.371347] virtio-mmio virtio-mmio.1: error -EBUSY: can't request region for resource [mem 0xd0001000-0xd0001fff]
[    0.371981] virtio-mmio virtio-mmio.1: probe with driver virtio-mmio failed with error -16
[    0.372459] virtio-mmio virtio-mmio.2: error -EBUSY: can't request region for resource [mem 0xd0002000-0xd0002fff]
[    0.373048] virtio-mmio virtio-mmio.2: probe with driver virtio-mmio failed with error -16
[    0.373810] Serial: 8250/16550 driver, 1 ports, IRQ sharing disabled
[    0.374270] 00:00: ttyS0 at I/O 0x3f8 (irq = 28, base_baud = 115200) is a 16550A
[    0.374857] ACPI: bus type drm_connector registered
[    0.376655] loop: module loaded
[    0.380639] virtio_blk virtio0: 1/0/0 default/read/poll queues
[    0.381089] virtio_blk virtio0: [vda] 268435456 512-byte logical blocks (137 GB/128 GiB)
[    0.381807] rbd: loaded (major 253)
[    0.382046] Loading iSCSI transport class v2.0-870.
[    0.382452] iscsi: registered transport (tcp)
[    0.382875] wireguard: WireGuard 1.0.0 loaded. See www.wireguard.com for information.
[    0.383317] wireguard: Copyright (C) 2015-2019 Jason A. Donenfeld <Jason@zx2c4.com>. All Rights Reserved.
[    0.383903] tun: Universal TUN/TAP device driver, 1.6
[    0.385014] VFIO - User Level meta-driver version: 0.3
[    0.385375] i8042: PNP: PS/2 Controller [PNP0303:PS2] at 0x60,0x64 irq 30
[    0.385785] i8042: PNP: PS/2 appears to have AUX port disabled, if this is incorrect please boot with i8042.nopnp
[    0.386575] serio: i8042 KBD port at 0x60,0x64 irq 30
[    0.387093] device-mapper: ioctl: 4.48.0-ioctl (2023-03-01) initialised: dm-devel@lists.linux.dev
[    0.387695] intel_pstate: CPU model not supported
[    0.388015] hid: raw HID events driver (C) Jiri Kosina
[    0.388513] netem: version 1.3
[    0.391227] IPVS: Registered protocols (TCP, UDP, SCTP, AH, ESP)
[    0.391569] IPVS: Connection hash table configured (size=4096, memory=32Kbytes)
[    0.392084] IPVS: ipvs loaded.
[    0.392272] IPVS: [rr] scheduler registered.
[    0.392498] IPVS: [mh] scheduler registered.
[    0.393194] Initializing XFRM netlink socket
[    0.393438] NET: Registered PF_INET6 protocol family
[    0.394503] Segment Routing with IPv6
[    0.394699] In-situ OAM (IOAM) with IPv6
[    0.394925] NET: Registered PF_PACKET protocol family
[    0.395212] Bridge firewalling registered
[    0.395477] Key type dns_resolver registered
[    0.395720] Key type ceph registered
[    0.396509] libceph: loaded (mon/osd proto 15/24)
[    0.396833] NET: Registered PF_VSOCK protocol family
[    0.397192] IPI shorthand broadcast: enabled
[    0.399102] sched_clock: Marking stable (348981104, 47838292)->(544320067, -147500671)
[    0.401141] registered taskstats version 1
[    0.401457] Loading compiled-in X.509 certificates
[    0.402300] Loaded X.509 cert 'Build time autogenerated kernel key: b45194989cb73d2f9260dd61cf9439b36479723f'
[    0.404552] Demotion targets for Node 0: null
[    0.404808] Key type .fscrypt registered
[    0.405007] Key type fscrypt-provisioning registered
[    0.406088] Key type encrypted registered
[    0.910015] input: AT Raw Set 2 keyboard as /devices/platform/i8042/serio0/input/input0
[    0.924032] IP-Config: Complete:
[    0.924270]      device=eth0, hwaddr=82:2b:38:3d:bc:d0, ipaddr=172.30.0.2, mask=255.255.255.0, gw=172.30.0.1
[    0.924839]      host=172.30.0.2, domain=, nis-domain=(none)
[    0.925233]      bootserver=255.255.255.255, rootserver=255.255.255.255, rootpath=
[    0.936232] EXT4-fs (vda): mounted filesystem c9c67fd0-dd57-47c1-b1ee-a0dbbd99d0ba r/w with ordered data mode. Quota mode: none.
[    0.943179] VFS: Mounted root (ext4 filesystem) on device 254:0.
[    0.945620] devtmpfs: mounted
[    0.951340] Freeing unused kernel image (initmem) memory: 3892K
[    0.951573] Write protecting the kernel read-only data: 24576k
[    0.953285] Freeing unused kernel image (rodata/data gap) memory: 696K
[    0.953510] Run /sbin/init as init process
[    0.953655]   with arguments:
[    0.953656]     /sbin/init
[    0.953657]   with environment:
[    0.953657]     HOME=/
[    0.953657]     TERM=linux
[    0.953658]     cgroup_enable=memory
[    0.953658]     rc_cgroup_mode=hybrid
[    1.051132] systemd[1]: systemd 252.38-1~deb12u1 running in system mode (+PAM +AUDIT +SELINUX +APPARMOR +IMA +SMACK +SECCOMP +GCRYPT -GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 -IDN +IPTC +KMOD +LIBCRYPTSETUP +LIBFDISK +PCRE2 -PWQUALITY +P11KIT +QRENCODE +TPM2 +BZIP2 +LZ4 +XZ +ZLIB +ZSTD -BPF_FRAMEWORK -XKBCOMMON +UTMP +SYSVINIT default-hierarchy=unified)
[    1.052256] systemd[1]: Detected virtualization kvm.
[    1.052443] systemd[1]: Detected architecture x86-64.
[    1.103237] systemd[1]: Hostname set to <c9d7523bc008>.
[    1.237227] systemd[1]: /etc/systemd/system/docker-socat.service:13: Failed to parse output specifier, ignoring: console
[    1.237588] systemd[1]: /etc/systemd/system/docker-socat.service:14: Failed to parse output specifier, ignoring: console
[    1.253200] systemd[1]: Queued start job for default target multi-user.target.
[    1.286931] systemd[1]: Created slice system-getty.slice - Slice /system/getty.
[    1.287886] systemd[1]: Created slice system-modprobe.slice - Slice /system/modprobe.
[    1.289012] systemd[1]: Created slice system-serial\x2dgetty.slice - Slice /system/serial-getty.
[    1.290096] systemd[1]: Created slice user.slice - User and Session Slice.
[    1.290878] systemd[1]: Started systemd-ask-password-console.path - Dispatch Password Requests to Console Directory Watch.
[    1.291827] systemd[1]: Started systemd-ask-password-wall.path - Forward Password Requests to Wall Directory Watch.
[    1.292784] systemd[1]: Set up automount proc-sys-fs-binfmt_misc.automount - Arbitrary Executable File Formats File System Automount Point.
[    1.293850] systemd[1]: Expecting device dev-ttyS0.device - /dev/ttyS0...
[    1.294566] systemd[1]: Reached target cryptsetup.target - Local Encrypted Volumes.
[    1.295199] systemd[1]: Reached target integritysetup.target - Local Integrity Protected Volumes.
[    1.295869] systemd[1]: Reached target network-online.target - Network is Online.
[    1.296715] systemd[1]: Reached target paths.target - Path Units.
[    1.297440] systemd[1]: Reached target remote-fs.target - Remote File Systems.
[    1.298222] systemd[1]: Reached target slices.target - Slice Units.
[    1.298740] systemd[1]: Reached target swap.target - Swaps.
[    1.299217] systemd[1]: Reached target veritysetup.target - Local Verity Protected Volumes.
[    1.299927] systemd[1]: Listening on systemd-initctl.socket - initctl Compatibility Named Pipe.
[    1.301245] systemd[1]: Listening on systemd-journald-audit.socket - Journal Audit Socket.
[    1.302079] systemd[1]: Listening on systemd-journald-dev-log.socket - Journal Socket (/dev/log).
[    1.303013] systemd[1]: Listening on systemd-journald.socket - Journal Socket.
[    1.303906] systemd[1]: Listening on systemd-udevd-control.socket - udev Control Socket.
[    1.304680] systemd[1]: Listening on systemd-udevd-kernel.socket - udev Kernel Socket.
[    1.306129] systemd[1]: Mounting dev-hugepages.mount - Huge Pages File System...
[    1.307472] systemd[1]: Mounting dev-mqueue.mount - POSIX Message Queue File System...
[    1.308726] systemd[1]: Mounting sys-kernel-debug.mount - Kernel Debug File System...
[    1.309945] systemd[1]: Mounting sys-kernel-tracing.mount - Kernel Trace File System...
[    1.310627] systemd[1]: kmod-static-nodes.service - Create List of Static Device Nodes was skipped because of an unmet condition check (ConditionFileNotEmpty=/lib/modules/6.12.8+/modules.devname).
[    1.311922] systemd[1]: Starting modprobe@configfs.service - Load Kernel Module configfs...
[    1.313181] systemd[1]: Starting modprobe@dm_mod.service - Load Kernel Module dm_mod...
[    1.314764] systemd[1]: Starting modprobe@drm.service - Load Kernel Module drm...
[    1.316125] systemd[1]: Starting modprobe@efi_pstore.service - Load Kernel Module efi_pstore...
[    1.317401] systemd[1]: Starting modprobe@fuse.service - Load Kernel Module fuse...
[    1.318749] systemd[1]: Starting modprobe@loop.service - Load Kernel Module loop...
[    1.320637] systemd[1]: Starting systemd-journald.service - Journal Service...
[    1.322919] systemd[1]: Starting systemd-modules-load.service - Load Kernel Modules...
[    1.324439] systemd[1]: Starting systemd-remount-fs.service - Remount Root and Kernel File Systems...
[    1.326409] systemd[1]: Starting systemd-udev-trigger.service - Coldplug All udev Devices...
[    1.328372] systemd[1]: Mounted dev-hugepages.mount - Huge Pages File System.
[    1.329074] systemd[1]: Mounted dev-mqueue.mount - POSIX Message Queue File System.
[    1.329710] systemd[1]: Mounted sys-kernel-debug.mount - Kernel Debug File System.
[    1.330359] systemd[1]: Mounted sys-kernel-tracing.mount - Kernel Trace File System.
[    1.331112] systemd[1]: modprobe@configfs.service: Deactivated successfully.
[    1.331499] systemd[1]: Finished modprobe@configfs.service - Load Kernel Module configfs.
[    1.332384] systemd[1]: modprobe@dm_mod.service: Deactivated successfully.
[    1.332737] systemd[1]: Finished modprobe@dm_mod.service - Load Kernel Module dm_mod.
[    1.333533] systemd[1]: modprobe@drm.service: Deactivated successfully.
[    1.333831] systemd[1]: Finished modprobe@drm.service - Load Kernel Module drm.
[    1.334533] systemd[1]: modprobe@efi_pstore.service: Deactivated successfully.
[    1.334859] systemd[1]: Finished modprobe@efi_pstore.service - Load Kernel Module efi_pstore.
[    1.335568] systemd[1]: modprobe@fuse.service: Deactivated successfully.
[    1.335894] systemd[1]: Finished modprobe@fuse.service - Load Kernel Module fuse.
[    1.336553] systemd[1]: Started systemd-journald.service - Journal Service.
[    1.346974] systemd-journald[672]: Received client request to flush runtime journal.
[ 1234.861040] random: crng reseeded due to virtual machine fork
[ 1234.966149] systemd[1]: systemd-journald.service: Main process exited, code=killed, status=6/ABRT
[ 1234.966640] systemd[1]: systemd-journald.service: Failed with result 'watchdog'.
[ 1234.976318] systemd[1]: systemd-journald.service: Scheduled restart job, restart counter is at 1.
[ 1234.976818] systemd[1]: Stopped systemd-journald.service - Journal Service.
[ 1235.009213] systemd[1]: Starting systemd-journald.service - Journal Service...
[ 1235.009909] systemd[1]: systemd-tmpfiles-clean.service: Deactivated successfully.
[ 1235.010440] systemd[1]: Finished systemd-tmpfiles-clean.service - Cleanup of Temporary Directories.
[ 1235.016762] systemd[1]: run-credentials-systemd\x2dtmpfiles\x2dclean.service.mount: Deactivated successfully.
[ 1235.041088] systemd-journald[1576]: File /var/log/journal/6e36bc5dc1e547beae093c26891eed0f/system.journal corrupted or uncleanly shut down, renaming and replacing.
[ 1235.112967] systemd[1]: Started systemd-journald.service - Journal Service.
[ 1237.560356] overlayfs: upperdir is in-use as upperdir/workdir of another mount, accessing files from both mounts will result in undefined behavior.
[ 1237.560872] overlayfs: workdir is in-use as upperdir/workdir of another mount, accessing files from both mounts will result in undefined behavior.
[ 1237.757659] oom_control is deprecated and will be removed. Please report your usecase to linux-mm-@kvack.org if you depend on this functionality.
[ 1644.538189] random: crng reseeded due to virtual machine fork
[ 1644.625202] systemd[1]: systemd-timesyncd.service: Watchdog timeout (limit 3min)!
[ 1644.625930] systemd[1]: systemd-timesyncd.service: Killing process 1212 (systemd-timesyn) with signal SIGABRT.
[ 1644.682233] systemd[1]: systemd-logind.service: Main process exited, code=killed, status=6/ABRT
[ 1644.682785] systemd[1]: systemd-logind.service: Failed with result 'watchdog'.
[ 1644.721624] systemd[1]: systemd-journald.service: Main process exited, code=killed, status=6/ABRT
[ 1644.724326] systemd[1]: systemd-journald.service: Failed with result 'watchdog'.
[ 1644.743507] systemd[1]: systemd-timesyncd.service: Main process exited, code=killed, status=6/ABRT
[ 1644.743923] systemd[1]: systemd-timesyncd.service: Failed with result 'watchdog'.
[ 1644.769771] systemd[1]: systemd-logind.service: Scheduled restart job, restart counter is at 1.
[ 1644.770581] systemd[1]: systemd-journald.service: Scheduled restart job, restart counter is at 2.
[ 1644.771357] systemd[1]: systemd-timesyncd.service: Scheduled restart job, restart counter is at 1.
[ 1644.772126] systemd[1]: Stopped systemd-journald.service - Journal Service.
[ 1644.798456] systemd[1]: Starting systemd-journald.service - Journal Service...
[ 1644.798946] systemd[1]: Stopped systemd-logind.service - User Login Management.
[ 1644.806000] systemd[1]: Starting modprobe@drm.service - Load Kernel Module drm...
[ 1644.806470] systemd[1]: Stopped systemd-timesyncd.service - Network Time Synchronization.
[ 1644.833988] systemd-journald[2357]: File /var/log/journal/6e36bc5dc1e547beae093c26891eed0f/system.journal corrupted or uncleanly shut down, renaming and replacing.
[ 1644.843268] systemd[1]: Starting systemd-timesyncd.service - Network Time Synchronization...
[ 1644.844141] systemd[1]: modprobe@drm.service: Deactivated successfully.
[ 1644.844579] systemd[1]: Finished modprobe@drm.service - Load Kernel Module drm.
[ 1644.857378] systemd[1]: Starting systemd-logind.service - User Login Management...
[ 1644.899410] systemd[1]: Started systemd-journald.service - Journal Service.
[ 1987.295181] docker0: port 1(veth1e2c41c) entered blocking state
[ 1987.295502] docker0: port 1(veth1e2c41c) entered disabled state
[ 1987.295760] veth1e2c41c: entered allmulticast mode
[ 1987.296041] veth1e2c41c: entered promiscuous mode
[ 1987.306759] eth0: renamed from veth7ec8728
[ 1987.307538] docker0: port 1(veth1e2c41c) entered blocking state
[ 1987.307808] docker0: port 1(veth1e2c41c) entered forwarding state
[ 1989.723313] docker0: port 1(veth1e2c41c) entered disabled state
[ 1989.723655] veth7ec8728: renamed from eth0
[ 1989.757103] docker0: port 1(veth1e2c41c) entered disabled state
[ 1989.757982] veth1e2c41c (unregistering): left allmulticast mode
[ 1989.758232] veth1e2c41c (unregistering): left promiscuous mode
[ 1989.758452] docker0: port 1(veth1e2c41c) entered disabled state
[ 1990.904210] docker0: port 1(veth9bd3965) entered blocking state
[ 1990.904454] docker0: port 1(veth9bd3965) entered disabled state
[ 1990.904677] veth9bd3965: entered allmulticast mode
[ 1990.904883] veth9bd3965: entered promiscuous mode
[ 1990.915845] eth0: renamed from veth6b56ce9
[ 1990.916621] docker0: port 1(veth9bd3965) entered blocking state
[ 1990.916895] docker0: port 1(veth9bd3965) entered forwarding state
[ 1991.090629] docker0: port 2(vethca9cfe3) entered blocking state
[ 1991.090899] docker0: port 2(vethca9cfe3) entered disabled state
[ 1991.091113] vethca9cfe3: entered allmulticast mode
[ 1991.091321] vethca9cfe3: entered promiscuous mode
[ 1991.100368] eth0: renamed from veth4c53243
[ 1991.100894] docker0: port 2(vethca9cfe3) entered blocking state
[ 1991.101171] docker0: port 2(vethca9cfe3) entered forwarding state
[ 2012.157485] docker0: port 2(vethca9cfe3) entered disabled state
[ 2012.157925] veth4c53243: renamed from eth0
[ 2012.188109] docker0: port 2(vethca9cfe3) entered disabled state
[ 2012.188805] vethca9cfe3 (unregistering): left allmulticast mode
[ 2012.189066] vethca9cfe3 (unregistering): left promiscuous mode
[ 2012.189292] docker0: port 2(vethca9cfe3) entered disabled state
```

### 关键信息摘要：
- **内核版本**: Linux 6.12.8+ (编译于 2025年7月6日)
- **虚拟化环境**: KVM 虚拟机
- **处理器**: Intel Xeon 2.4GHz, 4核心
- **内存**: 约16GB RAM
- **文件系统**: EXT4 根文件系统
- **网络配置**: IP 172.30.0.2/24，网关 172.30.0.1
- **系统初始化**: systemd 252.38-1

---

## 2. `uname -a` 命令输出

显示系统基本信息：

```
Linux cursor 6.12.8+ #11 SMP PREEMPT_DYNAMIC Sun Jul  6 04:56:39 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux
```

### 信息解析：
- **操作系统**: Linux
- **主机名**: cursor
- **内核版本**: 6.12.8+
- **编译信息**: #11 SMP PREEMPT_DYNAMIC
- **编译时间**: Sun Jul 6 04:56:39 UTC 2025
- **架构**: x86_64

---

## 3. `cat /proc/self/status` 命令输出

显示当前进程状态信息：

```
Name:   cat
Umask:  0022
State:  R (running)
Tgid:   4532
Ngid:   0
Pid:    4532
PPid:   2228
TracerPid:      0
Uid:    1000    1000    1000    1000
Gid:    1000    1000    1000    1000
FDSize: 256
Groups:  
NStgid: 4532
NSpid:  4532
NSpgid: 4532
NSsid:  2228
Kthread:        0
VmPeak:     6036 kB
VmSize:     6036 kB
VmLck:         0 kB
VmPin:         0 kB
VmHWM:      1932 kB
VmRSS:      1932 kB
RssAnon:               0 kB
RssFile:            1932 kB
RssShmem:              0 kB
VmData:      488 kB
VmStk:       132 kB
VmExe:        24 kB
VmLib:      1816 kB
VmPTE:        56 kB
VmSwap:        0 kB
HugetlbPages:          0 kB
CoreDumping:    0
THP_enabled:    1
untag_mask:     0xffffffffffffffff
Threads:        1
SigQ:   0/63978
SigPnd: 0000000000000000
ShdPnd: 0000000000000000
SigBlk: 0000000000000000
SigIgn: 0000000000000000
SigCgt: 0000000000000000
CapInh: 0000000000000000
CapPrm: 0000000000000000
CapEff: 0000000000000000
CapBnd: 000001ffffffffff
CapAmb: 0000000000000000
NoNewPrivs:     0
Seccomp:        0
Seccomp_filters:        0
Speculation_Store_Bypass:       thread vulnerable
SpeculationIndirectBranch:      conditional enabled
Cpus_allowed:   f
Cpus_allowed_list:      0-3
Mems_allowed:   00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000000,00000001
Mems_allowed_list:      0
voluntary_ctxt_switches:        1
nonvoluntary_ctxt_switches:     0
```

### 关键信息：
- **进程名**: cat
- **进程ID**: 4532
- **父进程ID**: 2228
- **用户ID**: 1000
- **内存使用**: 虚拟内存 6036 kB，物理内存 1932 kB
- **CPU权限**: 允许使用 CPU 0-3（4个核心）
- **安全特性**: 启用了 THP（Transparent Huge Pages）

---

## 4. `cat /proc/mounts` 命令输出

显示当前挂载的文件系统：

```
overlay / overlay rw,relatime,lowerdir=/var/lib/docker/overlay2/l/IBZWBNXJ5UIEWHCPFEHNH4EFSP:/var/lib/docker/overlay2/l/X5U6HTWQCL3JEKDQVH64USXGO6:/var/lib/docker/overlay2/l/LHQEYTVDJ3OT7BXIEJYJBAWBNK:/var/lib/docker/overlay2/l/QHGRCDQCZW7Y5Q54QMPOEAT6LX:/var/lib/docker/overlay2/l/W5BFO7SUETAVNBWU2RYWWXLLN4:/var/lib/docker/overlay2/l/DOP4ILYBMBTZNAV35BUZ5F4N3J:/var/lib/docker/overlay2/l/PS2P4LAJJ57DEEPMTWA3XAWTNL:/var/lib/docker/overlay2/l/E6ESI2XEIHBWKRVDLUBLJINW2M:/var/lib/docker/overlay2/l/ZOA2CTUPAIRDH6EC5ERV2A4JFF:/var/lib/docker/overlay2/l/5AK7I2DOY2NNDFOEHNOJVEKW3B:/var/lib/docker/overlay2/l/XJ6MQS5FJUJMK6VYNRBON3NTPN:/var/lib/docker/overlay2/l/L5ZEPE5E4U77TGIFCBBA2R3JWR:/var/lib/docker/overlay2/l/OSZTKWSVNAMBJZ4DBP5DN2IGBG:/var/lib/docker/overlay2/l/IMNZRWXO3XF2VHSN25E6RPEN3N:/var/lib/docker/overlay2/l/IKJB6BVX6MS2PQWZXRSRYHI3SZ,upperdir=/var/lib/docker/overlay2/7093c53b11795e8558123c7ca4f1364c590b4b8bc21e14b503077f5021fe211b/diff,workdir=/var/lib/docker/overlay2/7093c53b11795e8558123c7ca4f1364c590b4b8bc21e14b503077f5021fe211b/work 0 0
proc /proc proc rw,nosuid,nodev,noexec,relatime 0 0
tmpfs /dev tmpfs rw,nosuid,size=65536k,mode=755 0 0
devpts /dev/pts devpts rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=666 0 0
sysfs /sys sysfs rw,nosuid,nodev,noexec,relatime 0 0
tmpfs /sys/fs/cgroup tmpfs rw,nosuid,nodev,noexec,relatime,mode=755 0 0
cgroup /sys/fs/cgroup/systemd cgroup rw,nosuid,nodev,noexec,relatime,xattr,name=systemd 0 0
cgroup /sys/fs/cgroup/perf_event cgroup rw,nosuid,nodev,noexec,relatime,perf_event 0 0
cgroup /sys/fs/cgroup/cpu,cpuacct cgroup rw,nosuid,nodev,noexec,relatime,cpu,cpuacct 0 0
cgroup /sys/fs/cgroup/blkio cgroup rw,nosuid,nodev,noexec,relatime,blkio 0 0
cgroup /sys/fs/cgroup/cpuset cgroup rw,nosuid,nodev,noexec,relatime,cpuset 0 0
cgroup /sys/fs/cgroup/devices cgroup rw,nosuid,nodev,noexec,relatime,devices 0 0
cgroup /sys/fs/cgroup/pids cgroup rw,nosuid,nodev,noexec,relatime,pids 0 0
cgroup /sys/fs/cgroup/hugetlb cgroup rw,nosuid,nodev,noexec,relatime,hugetlb 0 0
cgroup /sys/fs/cgroup/net_cls,net_prio cgroup rw,nosuid,nodev,noexec,relatime,net_cls,net_prio 0 0
cgroup /sys/fs/cgroup/memory cgroup rw,nosuid,nodev,noexec,relatime,memory 0 0
cgroup /sys/fs/cgroup/freezer cgroup rw,nosuid,nodev,noexec,relatime,freezer 0 0
mqueue /dev/mqueue mqueue rw,nosuid,nodev,noexec,relatime 0 0
shm /dev/shm tmpfs rw,nosuid,nodev,noexec,relatime,size=65536k 0 0
/dev/root /etc/resolv.conf ext4 rw,relatime 0 0
/dev/root /etc/hostname ext4 rw,relatime 0 0
/dev/root /etc/hosts ext4 rw,relatime 0 0
```

### 文件系统分析：
- **根文件系统**: overlay（Docker 容器特征）
- **标准挂载点**: proc, tmpfs, devpts, sysfs
- **cgroup 子系统**: systemd, perf_event, cpu, cpuacct, blkio, cpuset, devices, pids, hugetlb, net_cls, net_prio, memory, freezer
- **特殊挂载**: mqueue（消息队列）, shm（共享内存）
- **配置文件绑定挂载**: /etc/resolv.conf, /etc/hostname, /etc/hosts

---

## 总结

从这些命令的输出可以看出：

1. **运行环境**: 这是一个运行在 KVM 虚拟机中的 Docker 容器
2. **系统配置**: 4核 CPU，16GB 内存，使用 Linux 6.12.8+ 内核
3. **文件系统**: 使用 Docker 的 overlay 文件系统
4. **网络配置**: 静态 IP 172.30.0.2/24
5. **容器化特征**: 明显的 Docker overlay2 存储驱动和 cgroup 配置