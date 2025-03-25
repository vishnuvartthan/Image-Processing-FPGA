# Image-Processing-FPGA
## Project Title: Image Processing on FPGA

### Names of Teammates:
- Rithani Priyanga Coimbatore Kannan (hwu6hc)
- Vishnuvartthan Govindaraj (fpp6vt) 

# Overview of Project

The goal of this project is to implement computationally intensive digital image filters on an FPGA platform to achieve real-time image processing. Digital image processing plays a crucial role in a wide range of applications, from video streaming to computer vision and augmented reality. Processing images in real-time can be computationally expensive, especially when applying complex filters to high-resolution images. Software-based solutions struggle with the latency and processing time required for live image analysis, making hardware acceleration through FPGAs more effective.

By accelerating the image filtering process on FPGA hardware, we aim to significantly improve processing time, enabling real-time applications such as video stream processing, edge detection for vision systems, and preprocessing stages for AI-based systems. The FPGA's parallel processing capability will allow for faster data manipulation than general-purpose processors, making it suitable for high-speed image processing tasks. We aim to implement and evaluate multiple image filtering techniques, including:

- Gaussian Filter

- Box Filter

- Moving Average Convolution

- Grayscale Conversion, and many others

By accelerating these filters in hardware, we can enable real-time processing for applications such as live video processing, preprocessing for computer vision applications, and edge computing tasks.

# Motivation

The main motivation behind this project stems from the increasing demand for real-time image processing in modern technologies, such as autonomous vehicles, robotics, and surveillance systems. These systems rely on quick and accurate image manipulation, which can be computationally heavy, particularly when using complex filters to process large volumes of image data. For instance, Gaussian blurs, edge detection filters, and noise reduction techniques require considerable computational power, making them challenging to implement in real time using traditional processors.

FPGAs (Field-Programmable Gate Arrays) provide a solution to this challenge by offering parallel computing resources that can handle multiple operations simultaneously, unlike traditional CPUs, which are designed for sequential processing. This project will explore the potential of FPGAs to accelerate four critical image filtering techniques—Box Filter, Gaussian Filter, Moving Average Filter, and Grayscale Conversion—by implementing them in hardware.

By utilizing FPGAs, we can achieve a substantial speedup in image processing, enabling real-time applications such as live video processing and computer vision tasks. The ability to handle complex image processing algorithms in parallel also makes FPGAs an ideal platform for edge computing, where power efficiency and real-time processing are essential.

# Outline of Project

The project will be divided into several phases, with the core task being the design and implementation of multiple image filters on an FPGA. The following sections outline the primary techniques we will implement and their intended benefits.

## Image Filtering Techniques to be Implemented:
### Box Filter:

* The Box Filter is a simple image smoothing filter that replaces each pixel in an image with the average of the pixels in a surrounding window.

* This filter is widely used for basic noise reduction and image smoothing.

* Although computationally simple, it serves as a foundation for more advanced filters.

### Gaussian Filter:

* The Gaussian filter smooths the image while preserving edges better than the Box Filter by applying a weighted average.

* It uses a Gaussian kernel, which gives higher weights to the central pixels and lower weights to the surrounding ones, effectively blurring the image with minimal edge distortion.

* It is widely used in preprocessing stages to reduce noise while maintaining important features.

### Moving Average Filter:

* This filter calculates the average of a group of surrounding pixels, typically within a sliding window, and is used to remove high-frequency noise in images.

* It’s useful in reducing the sharp fluctuations in pixel intensity that occur in noisy or less than ideal conditions.

### Grayscale Conversion:

* Grayscale conversion involves converting a colored RGB image to shades of gray by computing a weighted sum of the red, green, and blue pixel values.

* This step simplifies image analysis and is commonly used in various computer vision algorithms for edge detection, feature extraction, and pattern recognition.



### FPGA Implementation Strategy:

* We will design and implement each of the filters in hardware using Verilog on an FPGA, ensuring that they operate efficiently and in parallel. The implementation will follow a pipeline architecture, where each filter acts as a stage in the pipeline. The image data will flow through each filter in the sequence and be processed at each stage.

Each of the filters will be designed to work on a 3x3 neighborhood of pixels to ensure that the processed image maintains the necessary level of detail. The filters will operate on RGB data, with each channel being processed separately and then combined to form the output pixel. For example, in the Gaussian filter, each of the RGB channels will be convolved with a Gaussian kernel before being combined back into a single pixel.

The implementation will be divided into the following steps:

* Develop Verilog modules for each filter.

* Integrate the filters into a pipeline with control logic to select which filter to apply.

* Interface the FPGA with a camera module to capture images in real time.

* Display the processed images on an output device, such as a monitor or HDMI screen.



# Expected Milestones and Outcomes :
## Phase 1 :

- Finalize project proposal and team roles.

- Review literature on FPGA-based image filtering.

## Phase 2 :

- Develop individual Verilog modules for each filter.

- Implement testbenches to verify functionality.

## Phase 3 :

- Integrate all modules into a single pipeline.

- Implement user controls for selecting filters.

## Phase 4 :

- Test the design on FPGA hardware.

- Optimize for performance and resource usage.

## Final Phase:

- Document results and performance analysis.

- Prepare a final report and demonstration.

# Expected Challenges

- Memory Bandwidth: Efficiently accessing and storing image data in SDRAM may require careful optimization.

- Pipeline Implementation: Ensuring smooth data flow through multiple filter stages without bottlenecks.

- Hardware Constraints: Managing FPGA resources efficiently to accommodate all filters within available logic elements.

- Real-Time Processing: Achieving low-latency performance for live video applications.

# Conclusion
In this project, we aim to demonstrate the power of FPGA hardware in accelerating image filtering tasks for real-time processing. By designing and implementing multiple filters such as the Box Filter, Gaussian Filter, Moving Average Filter, and Grayscale Conversion, we will showcase the potential of FPGA acceleration for edge computing and computer vision tasks. The successful completion of this project will not only improve our understanding of FPGA development but also contribute valuable insights into the efficiency and effectiveness of hardware-accelerated image processing.
