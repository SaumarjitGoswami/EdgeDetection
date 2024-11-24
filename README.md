PGA-Based Real-Time Image Processing
Project Overview:
This repository contains Verilog modules for a real-time image processing pipeline on FPGA. It processes 1920x1080 HD video streams, converting RGB to grayscale, buffering image data, and applying edge detection with a Sobel filter. Designed for AXI4-Stream interfaces, the modules support efficient, scalable, and modular implementation.

Key Modules:
dataReg.v: Synchronizes data using a latch for smooth pipelining.
pipeline.v: Implements cascading registers for pipelined data flow.
pixel.v: Handles single-pixel processing, forming the base unit of the pipeline.
line.v: Manages line buffering by calling pixel multiple times for up to 1920 pixels.
image.v: Combines multiple line buffers to process entire image frames.
rgb2grey.v: Converts 24-bit RGB data to 8-bit grayscale.
sobel.v: Detects edges using horizontal and vertical Sobel filters, with pipelined control signal synchronization.
