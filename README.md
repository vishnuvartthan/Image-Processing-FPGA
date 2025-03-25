# Image-Processing-FPGA
#Project Title: Real-Time Image Filtering on FPGA

#Names of Teammates: Rithani priyanga coimbatore, Vishnuvartthan Govindaraj  

# Overview of Project

The goal of this project is to apply computationally heavy digital filters to a given image in real time using an FPGA. Due to the computational complexity of digital image processing, an FPGA is used to accelerate this process. We aim to implement and evaluate multiple image filtering techniques, including:

- Box Filter

- Gaussian Filter

- Moving Average Filter

- Grayscale Conversion

By accelerating these filters in hardware, we can enable real-time processing for applications such as live video processing, preprocessing for computer vision applications, and edge computing tasks.

# Motivation

Digital image processing is an essential component of modern computer vision and artificial intelligence applications. Many of these applications require real-time processing of high-resolution images, which can be computationally expensive. By implementing image filters on an FPGA, we can achieve significant speedups compared to software-based solutions. This project explores how FPGA acceleration can make image filtering more efficient for real-time applications.

# Outline of Project

## Image Filtering Techniques to be Implemented:

### Box Filter:

A simple averaging filter that replaces each pixel value with the average of the surrounding pixels.

Used for basic image smoothing.

### Gaussian Filter:

A weighted averaging filter that smooths images while preserving edges better than a standard box filter.

Useful for reducing image noise and detail.

### Moving Average Filter:

Computes the average of a subset of pixels over a moving window.

Can be used to remove high-frequency noise in images.

### Grayscale Conversion:

Converts an RGB image to grayscale by computing a weighted sum of the R, G, and B channels.

Used as a preprocessing step in many computer vision tasks.

### FPGA Implementation Strategy:

Image data will be captured from a camera or loaded from memory.

A dedicated image processing module will be implemented in Verilog.

A pipeline architecture will be used to apply the filters efficiently.

Filter selection will be controlled via switches or user input.

The processed image will be displayed on a monitor via VGA output.


# Expected Milestones and Outcomes

## Phase 1 (Week 1-2):

- Finalize project proposal and team roles.

- Review literature on FPGA-based image filtering.

## Phase 2 (Week 3-4):

- Develop individual Verilog modules for each filter.

- Implement testbenches to verify functionality.

## Phase 3 (Week 5-6):

- Integrate all modules into a single pipeline.

- Implement user controls for selecting filters.

## Phase 4 (Week 7-8):

- Test the design on FPGA hardware.

- Optimize for performance and resource usage.

## Final Phase:

- Document results and performance analysis.

- Prepare a final report and demonstration.

## Expected Challenges

Memory Bandwidth: Efficiently accessing and storing image data in SDRAM may require careful optimization.

Pipeline Implementation: Ensuring smooth data flow through multiple filter stages without bottlenecks.

Hardware Constraints: Managing FPGA resources efficiently to accommodate all filters within available logic elements.

Real-Time Processing: Achieving low-latency performance for live video applications.

By successfully implementing this project, we aim to demonstrate the power of FPGA acceleration for real-time image processing and gain hands-on experience with digital design methodologies.
