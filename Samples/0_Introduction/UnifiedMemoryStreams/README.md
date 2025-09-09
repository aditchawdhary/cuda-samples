# UnifiedMemoryStreams - Unified Memory Streams

## Description

This sample demonstrates the use of OpenMP and streams with Unified Memory on a single GPU.

## Key Concepts

CUDA Systems Integration, OpenMP, CUBLAS, Multithreading, Unified Memory, CUDA Streams and Events

## Supported SM Architectures

## Supported OSes

Linux, Windows

## Supported CPU Architecture

x86_64, armv7l

## CUDA APIs involved

### [CUDA Runtime API](http://docs.nvidia.com/cuda/cuda-runtime-api/index.html)
cudaStreamDestroy, cudaFree, cudaMallocManaged, cudaStreamAttachMemAsync, cudaSetDevice, cudaDeviceSynchronize, cudaStreamSynchronize, cudaStreamCreate, cudaGetDeviceProperties

## Dependencies needed to build/run
[OpenMP](../../../README.md#openmp), [UVM](../../../README.md#uvm), [CUBLAS](../../../README.md#cublas)

## Prerequisites

Download and install the [CUDA Toolkit](https://developer.nvidia.com/cuda-downloads) for your corresponding platform.
Make sure the dependencies mentioned in [Dependencies]() section above are installed.

## References (for more details)

## Output
```
(main) root@C.25691976:/workspace/cuda-samples/0_Introduction/UnifiedMemoryStreams$ nvcc -I ../../Common UnifiedMemoryStreams.cu -o UnifiedMemoryStreams -l
cublas -Xcompiler -fopenmp
(main) root@C.25691976:/workspace/cuda-samples/0_Introduction/UnifiedMemoryStreams$ ls
CMakeFiles  UnifiedMemoryStreams  UnifiedMemoryStreams.cu
(main) root@C.25691976:/workspace/cuda-samples/0_Introduction/UnifiedMemoryStreams$ ./UnifiedMemoryStreams 
GPU Device 0: "Pascal" with compute capability 6.0

Executing tasks on host / device
Task [0], thread [0] executing on device (543)
Task [2], thread [2] executing on device (831)
Task [3], thread [3] executing on device (483)
Task [1], thread [1] executing on device (355)
Task [4], thread [0] executing on device (320)
Task [5], thread [2] executing on device (106)
Task [6], thread [3] executing on device (903)
Task [7], thread [1] executing on device (896)
Task [8], thread [0] executing on host (64)
Task [9], thread [2] executing on device (912)
Task [10], thread [1] executing on device (697)
Task [11], thread [1] executing on device (388)
Task [12], thread [2] executing on host (64)
Task [13], thread [1] executing on device (603)
Task [14], thread [2] executing on device (735)
Task [15], thread [0] executing on device (722)
Task [16], thread [3] executing on device (307)
Task [17], thread [0] executing on device (123)
Task [18], thread [3] executing on device (513)
Task [19], thread [0] executing on device (856)
Task [20], thread [3] executing on device (761)
Task [21], thread [0] executing on device (227)
Task [22], thread [1] executing on device (791)
Task [23], thread [2] executing on device (464)
Task [24], thread [3] executing on device (912)
Task [25], thread [0] executing on device (916)
Task [26], thread [2] executing on device (872)
Task [27], thread [1] executing on device (117)
Task [28], thread [0] executing on device (819)
Task [29], thread [3] executing on device (316)
Task [30], thread [0] executing on device (583)
Task [31], thread [1] executing on device (284)
Task [32], thread [2] executing on device (941)
Task [33], thread [3] executing on device (804)
Task [34], thread [2] executing on host (98)
Task [35], thread [1] executing on device (283)
Task [36], thread [0] executing on host (66)
Task [37], thread [0] executing on device (645)
Task [38], thread [3] executing on device (264)
Task [39], thread [2] executing on device (664)
All Done!
```
