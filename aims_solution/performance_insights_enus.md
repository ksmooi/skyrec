# Performance Insights: AI Video and Image Analysis with GPUs

## Introduction

This document provides an in-depth look at the performance benchmarks for AI-based video and image analysis systems using a variety of GPU configurations. These benchmarks evaluate recording functions, data retention capabilities, and specific analysis functionalities for both face recognition and person & vehicle recognition. By analyzing different GPU setups, this document highlights the strengths and limitations of each configuration, offering critical insights into how these systems can be optimized for different deployment scenarios, including edge devices, workstations, and data centers. This information is essential for professionals looking to enhance the efficiency and effectiveness of AI-driven video analysis systems.

## 40 Cameras Recording

[![40 cameras recording](https://img.youtube.com/vi/X3ISQpXO0XU/0.jpg)](https://www.youtube.com/watch?v=X3ISQpXO0XU)

### Recording Functions and Data Rate

The tables below outline the recording functions, data rates, and storage arrangements for a system utilizing 40 cameras per server. The first table details the recording capabilities, showing that all 40 cameras can record video at a rate of 2 Mbps per camera and generate thumbnails at a rate of 8 images per minute per camera. However, due to GPU limitations, only 16 cameras can utilize the AI channel for analysis at 15 FPS per camera.

| Recording Function | 40 cameras / Server         | Data Rate               |
|--------------------|-----------------------------|-------------------------|
| Video              | All                         | 2 Mbps / Camera         |
| Thumbnail          | All                         | 8 image / min / Camera  |
| AI channel         | 16 (due to GPU limitation)  | 15 FPS / Camera         |

### Storage Arrangement

The table provides the storage arrangement options, indicating how different HDD capacities affect the number of cameras per disk and the data retention period. For instance, a 6TB HDD can handle 4 cameras with a data retention period of 30 days, while a 10TB HDD can accommodate 3 cameras but with a longer retention period of 90 days. This information is essential for planning and optimizing storage solutions to meet specific recording and retention needs.

| HDD Capacity | Camera per Disk  | Data Retention |
|--------------|------------------|----------------|
| 6TB          | 4                | 30 days        |
| 8TB          | 3                | 60 days        |
| 12TB         | 4                | 60 days        |
| 10TB         | 3                | 90 days        |

**Notes**
- 40 cameras recording with 8 HDDs on SATA ports

## 24 Cameras Recording

[![24 cameras recording](https://img.youtube.com/vi/94v7AY0tyrA/0.jpg)](https://www.youtube.com/watch?v=94v7AY0tyrA)

### Recording Functions and Data Rate

The tables below describe the recording functions, data rates, and storage arrangements for a system using 24 cameras per server. The first table details the recording capabilities, showing that all 24 cameras can record video at a rate of 2 Mbps per camera and generate thumbnails at a rate of 8 images per minute per camera. Due to GPU limitations, the AI channel can only be used by 16 cameras, processing at 15 FPS per camera.

| Recording Function | 24 cameras / Server              | Data Rate               |
|--------------------|----------------------------------|-------------------------|
| Video              | All                              | 2 Mbps / Camera         |
| Thumbnail          | All                              | 8 image / min / Camera  |
| AI channel         | 16 (due to GPU limitation)       | 15 FPS / Camera         |

### Storage Arrangement

The table provides various storage arrangement options, detailing how different HDD configurations affect the number of cameras per disk and the data retention period. For example, a configuration with 4TB x 5 + 2TB x 1 HDDs can support 3 cameras per disk with a data retention period of 30 days, while a setup with 12TB x 5 + 6TB x 1 HDDs also supports 3 cameras per disk but extends the retention period to 90 days. This information helps in planning and optimizing storage solutions based on specific recording and retention requirements.

| HDD Capacity        | Camera per Disk  | Data Retention |
|---------------------|------------------|----------------|
| 4TB x 5 + 2TB x 1   | 3 (recommended)  | 30 days        |
| 6TB x 4             | 4                | 30 days        |
| 8TB x 5 + 4TB x 1   | 3 (recommended)  | 60 days        |
| 12TB x 4            | 4                | 60 days        |
| 12TB x 5 + 6TB x 1  | 3                | 90 days        |

**Notes**
- 24 cameras recording with 6 HDDs on SATA ports

## Performance Benchmark on Single GPU

[![Performance Benchmark on Single GPU](https://img.youtube.com/vi/J13jzoFAXto/0.jpg)](https://www.youtube.com/watch?v=J13jzoFAXto)

The following tables provide a comprehensive performance benchmark for single GPU configurations used in Face Analysis and Person & Vehicle Analysis. The tables present key metrics including deployment environment, AI channels, analysis frame rates (FPS), NVDEC units, memory capacity, CUDA cores, and Tensor cores for various NVIDIA GPUs. These benchmarks highlight the performance capabilities of different GPU models across various deployment scenarios such as edge devices, workstations, and data centers. The data demonstrates how each GPU configuration handles high-resolution video streams and complex AI processing tasks, providing critical insights for optimizing AI-driven video analysis systems.

### Face Analysis on Single GPU

| Single GPU         | Deployment   | AI Channel | Analyze FPS | NVDEC | Memory | CUDA Cores | Tensor Cores |
|--------------------|--------------|------------|-------------|-------|--------|------------|--------------|
| 1 x NVIDIA RTX 3060| Edge Device  | 18         | 270         | 1     | 12 GB  | 3,584      | 112          |
| 1 x NVIDIA A5000   | Workstation  | 36         | 540         | 2     | 24 GB  | 8,192      | 256          |
| 1 x NVIDIA A30     | Data Center  | 40         | 600         | 4     | 24 GB  | 3,584      | 224          |
| 1 x NVIDIA A100    | Data Center  | 60         | 900         | 5     | 40 GB  | 6,912      | 432          |

### Person & Vehicle Analysis on Single GPU

| Single GPU         | Deployment   | AI Channel | Analyze FPS | NVDEC | Memory | CUDA Cores | Tensor Cores |
|--------------------|--------------|------------|-------------|-------|--------|------------|--------------|
| 1 x NVIDIA RTX 3060| Edge Device  | 18         | 270         | 1     | 12 GB  | 3,584      | 112          |
| 1 x NVIDIA A5000   | Workstation  | 36         | 540         | 2     | 24 GB  | 8,192      | 256          |
| 1 x NVIDIA A30     | Data Center  | 40         | 600         | 4     | 24 GB  | 3,584      | 224          |
| 1 x NVIDIA A100    | Data Center  | 60         | 900         | 5     | 40 GB  | 6,912      | 432          |

**Notes**
- HEVC video streaming (1920 x 1080, 15 FPS, 2 Mbps)
- H.264 video streaming (1920 x 1080, 15 FPS, 2 Mbps)

### Face Analysis

A comprehensive Face AI Analysis provides the following functionalities:
- HEVC/H264 Decoder
- Face Detection
- Face Mask Classification
- Face Gender Classification
- Face Age Classification
- Face Race Classification
- Face Recognition

### Person & Vehicle AI Analysis

A comprehensive Person & Vehicle AI Analysis provides the following functionalities:
- HEVC/H264 Decoder
- Person Detection
- Person Gender Classification
- Person Upper Clothes Style Classification
- Person Lower Clothes Style Classification
- Person Upper Clothes Color Classification
- Person Lower Clothes Color Classification
- Person Recognition (ReID)
- Vehicle Category Classification
- Vehicle Color Classification
- Vehicle Recognition

## Performance Benchmark on Dual GPU

[![Performance Benchmark on Dual GPU](https://img.youtube.com/vi/sjCYWvHJ65c/0.jpg)](https://www.youtube.com/watch?v=sjCYWvHJ65c)

The following tables provide a detailed performance benchmark for dual GPU setups used in Face Analysis and Person & Vehicle Analysis. Each table highlights the deployment environment, AI channels, analysis frame rates (FPS), NVDEC units, memory capacity, CUDA cores, and Tensor cores for various NVIDIA GPU configurations. The data illustrates the significant performance improvements achieved with dual GPU configurations across different deployment scenarios such as edge devices, workstations, and data centers. These benchmarks are critical for understanding the capabilities of AI-driven video analysis systems in processing and analyzing high-resolution video streams efficiently.

### Face Analysis on Dual GPU

| Dual GPU           | Deployment   | AI Channel | Analyze FPS | NVDEC   | Memory        | CUDA Cores       | Tensor Cores    |
|--------------------|--------------|------------|-------------|---------|---------------|------------------|-----------------|
| 2 x NVIDIA RTX 3060| Edge Device  | 36         | 540         | 2 x 1   | 2 x 12 GB     | 2 x 3,584        | 2 x 112         |
| 2 x NVIDIA A5000   | Workstation  | 72         | 1,080       | 2 x 2   | 2 x 24 GB     | 2 x 8,192        | 2 x 256         |
| 2 x NVIDIA A30     | Data Center  | 80         | 1,200       | 2 x 4   | 2 x 24 GB     | 2 x 3,584        | 2 x 224         |
| 2 x NVIDIA A100    | Data Center  | 128        | 1,920       | 2 x 5   | 2 x 40 GB     | 2 x 6,912        | 2 x 432         |

### Person & Vehicle Analysis on Dual GPU

| Dual GPU           | Deployment   | AI Channel | Analyze FPS | NVDEC   | Memory        | CUDA Cores       | Tensor Cores    |
|--------------------|--------------|------------|-------------|---------|---------------|------------------|-----------------|
| 2 x NVIDIA RTX 3060| Edge Device  | 36         | 540         | 2 x 1   | 2 x 12 GB     | 2 x 3,584        | 2 x 112         |
| 2 x NVIDIA A5000   | Workstation  | 72         | 1,080       | 2 x 2   | 2 x 24 GB     | 2 x 8,192        | 2 x 256         |
| 2 x NVIDIA A30     | Data Center  | 80         | 1,200       | 2 x 4   | 2 x 24 GB     | 2 x 3,584        | 2 x 224         |
| 2 x NVIDIA A100    | Data Center  | 128        | 1,920       | 2 x 5   | 2 x 40 GB     | 2 x 6,912        | 2 x 432         |

**Notes**
- HEVC video streaming (1920 x 1080, 15 FPS, 2 Mbps)
- H.264 video streaming (1920 x 1080, 15 FPS, 2 Mbps)

