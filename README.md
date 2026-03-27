# Low Mem Brain

![edge-ai](https://img.shields.io/badge/edge--ai-blue?style=flat-square) ![raspberry-pi](https://img.shields.io/badge/raspberry--pi-blue?style=flat-square) ![iot](https://img.shields.io/badge/iot-blue?style=flat-square)

An optimized inference engine for running small agent models on Raspberry Pi devices.

## Overview
Low Mem Brain is designed to bridge the gap between resource-constrained hardware and autonomous agent capabilities. By utilizing specialized quantization techniques and memory-efficient execution paths, it allows Raspberry Pi and other IoT devices to run local inference without relying on cloud APIs. This engine is specifically tuned for small-parameter models that power decision-making tasks at the edge.

## Features
*   **Memory-Optimized Execution:** Minimal RAM footprint designed to run comfortably on Raspberry Pi 4/5 and even Zero 2 W.
*   **Quantization Support:** Native support for 4-bit and 8-bit weights to reduce model size without significant logic loss.
*   **Agentic Framework:** Built-in hooks for tool-calling and sensory input processing in real-time environments.
*   **Low Latency:** Optimized C++ kernels with Python bindings for high-speed token generation on ARM architecture.

## Installation
Ensure you have Python 3.9+ installed on your device. Clone the repository and install the necessary dependencies:

```bash
git clone https://github.com/username/low-mem-brain.git
cd low-mem-brain
pip install -r requirements.txt
```

## Usage
To start the inference engine with a default agent model, run the following command:

```bash
python main.py --model ./models/tiny-agent-8b-q4.gguf --prompt "Check the temperature sensor and log the result."
```

You can also integrate it into your own scripts:

```python
from low_mem_brain import InferenceEngine

engine = InferenceEngine(model_path="models/tiny-agent.bin")
response = engine.generate("Scan local network for devices.")
print(response)
```

## Contributing
We welcome contributions to improve the efficiency and compatibility of Low Mem Brain. If you have ideas for optimizations or support for new hardware, please open an issue or submit a pull request following our standard coding guidelines.

## License
This project is licensed under the [MIT License](LICENSE).