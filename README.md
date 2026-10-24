# Learning to optimize matrix multiplication on a 2018 ThinkPad (and then a GPU)

## Machine
- ThinkPad T480s, Intel Core i5-8350U, 4 cores / 8 threads
- Base 1.7 GHz, max turbo 3.6 GHz, all benchmarks run with turbo off
- AVX2 + FMA: 2 FMA units × 8 floats × 2 FLOPs = 32 FP32 FLOP/cycle/core
- Caches: L1d 32 KiB and L2 256 KiB per core; L3 6 MiB shared
- Memory: 8 GB DDR4-2400, single channel (19.2 GB/s theoretical)
- Ubuntu 26.04, GCC 15.2, OpenBLAS 0.3.32

## Peak (FP32, turbo off at 1.7 GHz)
- 1 core: 32 × 1.7 = 54.4 GFLOP/s
- 4 cores: 32 × 1.7 × 4 = 217.6 GFLOP/s
