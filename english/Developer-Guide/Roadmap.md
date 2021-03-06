### Planned features and improvements

* CPU
 * [x] x86-32-only mode
 * [x] BIOS boot
 * [ ] x86-64-only mode (**dropping x86-32**)
 * [ ] Multicore HAL and scheduler (only for x64)
 * [ ] UEFI boot
 * [ ] USB fixes
* GPU
 * [x] Software OpenGL
 * [x] Virtualized OpenGL
 * [ ] Hardware OpenGL
 * [ ] Hardware Vulkan
 * [x] D3D over OpenGL
 * [ ] D3D over Vulkan
 * [ ] Native D3D
* Kernel
 * [x] Basic stubs: memory manager, FAT filesystem, simple scheduler
 * [ ] Stable memory manager
 * [ ] GUI for OS installer instead of DOS terminal session
 * [ ] Moving from FAT to EXT4 filesystem (NTFS ok for external drives, but not for root, BTRFS is very linux specific)
 * [ ] Stable networking
 * [x] Initial NT 5.1 support (Windows XP)
 * [ ] Full NT 5.1 support (Windows XP)
 * [x] Initial NT 5.2 support (Windows Server 2003)
 * [ ] Full NT 5.2 support (Windows Server 2003)
 * [ ] Initial NT 6.1 support (jump directly to Windows 7, compatibility mode)
 * [ ] Full NT 6.1 support (Windows 7)
 * [ ] Linux subsystem (only software)
 * [ ] Android subsystem (based on linux's, only software)
 * [ ] Easy system updates
* Visuals
 * [x] New default theming and visuals (Windows XP compatible)
 * [ ] Fix theming engine (Windows XP compatible)
 * [ ] GreenShell theme and toolkit for GreenStep
 * [ ] Overhaul of theming engine (shadows, blurs, effects)
* Shell and UI
 * [x] Initial implementations of shell, tray, explorer, start button and others
 * [ ] GreenStep widgets and gui elements
 * [ ] Stabilization of shell, tray, explorer, start button and others
 * [ ] Shell overhaul to add modern features and look
 * [ ] GreenLibs modules for GreenStep
 * [ ] Stable and finished user space software

---

### Not planned features

This project started as a controversy to undefined future (and past) of existing operating systems.
Our team decided to define precise list of *the most useful* features to the wide audiences.
Features, like ARM support, aren't really useful in any real manner *right now*, as already showed by Windows RT.
Features, like LPT printing, has so small applicability (LPT ports in 2016 anyone?),
so can't be considered in any manner real target for Greentea OS team and use case for our users.
Also, multiply that by a *enormous* number of bugs, hacks and workarounds, which we should fix now,
to at least make NT kernel non-academic project! And then improve the NT and WinAPI implementations, **the real things**.
Otherwise it is a waste of time.

---

### Feature timings

Features are highly dependent of Kernel API version.
Also, the Windows exosystem defines it's own distribution rules.
For example: while it *is* possible to run Vulkan API over Windows XP,
no hardware or middleware (LunarG) distributors actually did it.
Some features also, like native Wi-Fi or BLE support, were non-existent on old versions of NT.
So we need to declare timings and dependencies for each feature.

| NT Versions |
|:-:|
| Kernel NT < 5 |
| Kernel NT 5.0 (2000) |
| Kernel NT 5.1 (XP) |
| Kernel NT 5.2 (2003) |
| Kernel NT 6.0 (Vista) |
| Kernel NT 6.1 (7) |
| Kernel NT 6.2 (8) |
| Kernel NT 6.3 (8.1) |
| Kernel NT 10.0 (10) |
