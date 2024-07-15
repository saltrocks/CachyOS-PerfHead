# CachyOS Performance Checklist for True PerformanceHeads

<img src="swoletux.png" width="512">

## General

- Package repository for your specific generic architecture (x86_64-v3, x86_64-v4, znver4, etc)
- Performance CPU governor

## Kernel

- Full tickless
- 1000HZ running tick rate
- Full preempt
- Native AMD/Intel compiler optimizations
- O3 level compiler optimizations
- Full LTO
- Transparent Hugepages
- Custom schedulers
	- BORE+EEVDF 👑 (current best performer, especially under stress)
	- scx_lavd (topology unaware, works with most Intel CPUs, accordingly won't work well with CPUs that have 2 CCX such as the 7950X)
	- scx_bpfland (best for non-gaming related workloads, unparalleled responsiveness under stress)

## Graphics

- Replace `mesa` package with `mesa-git` \[[Source-1](https://flightlesssomething.duckdns.org/benchmark/54)\]

## Filesystem

- BTRFS \[[Source-1](https://discuss.cachyos.org/t/cachyos-performance-checklist-for-true-performanceheads/123/2)\]

## CPU

- Disable security mitigations (`mitigations=off`) depending on your CPU \[[Source-1](https://www.phoronix.com/news/AMD-Zen-4-Mitigations-Off) [Source-2](https://www.phoronix.com/review/amd-inception-benchmarks) [Source-3](https://www.phoronix.com/review/retbleed-benchmark)\]

### AMD

- `amd_pstate=active` if >= Zen2
- RAM timings (EXPO)
- Undervolting

## Programs

- Discord -> [OpenAsar](https://openasar.dev/), [Vesktop](https://github.com/Vencord/Vesktop)
- Firefox -> Cachy Browser

## Gaming

- [Proton GE](https://github.com/GloriousEggroll/proton-ge-custom)
- ~Use X11 instead of Wayland for now because of performance regressions yet to be resolved (TIMESTAMP: 2024-04-22) \[[Source-1](https://www.youtube.com/watch?v=Xr3bLN3tZjU)\]~ Fixed for the most part, with some caveats.