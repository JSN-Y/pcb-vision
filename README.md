# PCB Component Vision Terminal 🔬

A purely client-side web application designed to automatically detect, annotate, and catalog Integrated Circuits (ICs) on Printed Circuit Boards (PCBs).

<h4>🧠 Why Not YOLO?<h4>

Initially, the goal was to train a custom YOLO (You Only Look Once) object detection model to find and read chip part numbers. However, training a highly accurate YOLO model requires a massive, curated dataset of thousands of annotated PCB images, which simply was not available.
Instead, this project pivots to a Zero-Shot Vision-Language Model (VLM) architecture. By leveraging the spatial reasoning and world-knowledge of the Gemini 3.5 Flash engine, the system can instantly identify ICs, read micro-laser etchings, and deduce commercial part numbers without requiring any custom dataset training.

<h4>🚀 Features<h4>

* Zero-Setup Execution: Runs entirely in the browser using static HTML/JS. No backend server required.
* Auto-Scaling Coordinates: Automatically standardizes coordinate matrices from the VLM to perfectly overlay bounding boxes directly onto the image.
* Network Resiliency: Built-in 4-stage exponential backoff retry loop to handle API rate limits gracefully.
* High-Res Canvas Compiler: Generates downloadable, flattened images with bounding boxes and an embedded inventory legend.
* Built-in Sample Gallery: Contains 8 pre-loaded test images for quick execution. (I have also included 2 photos of a test run in the repository so you can see the output firsthand).

<h4>🛠 Usage<h4>

1. Open the web interface.
2. Generate and input your own Gemini API key into the configuration field.
3. Click a "Quick Test Sample" or drag-and-drop your own PCB image.
4. Click Execute Scan and watch the AI plot the components.

Note: You must use your own Google Gemini API key to operate this tool. Because this is a static frontend application, your API key is used strictly client-side and is never stored or routed through an external backend.
