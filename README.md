# CachyOS Performance Checklist for True PerformanceHeads

<img src="swoletux.png" width="512">

## General
- x86_64-v4 repository if CPU supports it, otherwise x86_64-v3
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
	- BORE+EEVDF
	- ECHO **(NEW ⭐)**
	- LAVD **(NEW ⭐)** (already included in `scx-scheds`)

## Filesystem

- XFS for regular desktop

## CPU

- Disable security mitigations (`mitigations=off`) depending on your CPU [^1] [^2] [^3]

### AMD

- `amd_pstate=active` if >= Zen2
- RAM timings (EXPO)
- Undervolting

## Programs

- Discord -> [OpenAsar](https://openasar.dev/)
- Firefox -> Cachy Browser

## Gaming

- [Proton GE](https://github.com/GloriousEggroll/proton-ge-custom)
- Use X11 instead of Wayland for now because of performance regressions yet to be resolved (TIMESTAMP: 2024-04-22) [^4]

# Footnotes

[^1]: https://www.phoronix.com/news/AMD-Zen-4-Mitigations-Off
[^2]: https://www.phoronix.com/review/amd-inception-benchmarks
[^3]: https://www.phoronix.com/review/retbleed-benchmark
[^4]: https://www.youtube.com/watch?v=Xr3bLN3tZjU