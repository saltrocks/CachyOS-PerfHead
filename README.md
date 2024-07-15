# CachyOS Performance Checklist for True PerformanceHeads

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
- Custom scheduler
	- BORE+EEVDF
	- ECHO **(NEW ⭐)**
	- LAVD **(NEW ⭐)**

## CPU

- Disable security mitigations (`mitigations=off`) depending on your CPU [^1] [^2] [^3]

### AMD

- `amd_pstate=active` if >= Zen2

# Footnotes

[^1]: https://www.phoronix.com/news/AMD-Zen-4-Mitigations-Off
[^2]: https://www.phoronix.com/review/amd-inception-benchmarks
[^3]: https://www.phoronix.com/review/retbleed-benchmark