
# Local Model Inference & Hardware Profiler

## Overview
This project evaluates the inference performance and GPU memory
usage of a locally loaded 7B instruction-tuned language model.

## Model
- Model: Qwen/Qwen2.5-7B-Instruct
- Quantization: 4-bit NF4
- Runtime: Hugging Face Transformers and PyTorch

## Hardware and Environment
- Execution environment: Google Colab
- GPU: NVIDIA Tesla T4
- GPU memory: approximately 15 GB
- Python and library versions: see notebook

## Experimental Method
- Input context lengths: 1024, 2048, 4096, 8192 tokens
- Maximum generated tokens: 32
- Repetitions per context length: 2
- Warm-up run excluded from measurements

## Metrics
- Time to First Token (TTFT)
- Mean inter-token latency
- Generation throughput (tokens/second)
- Peak allocated and reserved GPU memory

## Results
See profiling_results.csv, profiling_summary.csv,
and the generated plots.

## Limitations
Results depend on the model configuration, quantization,
hardware, runtime, and experimental conditions.
Cloud GPU availability and session limits may affect reproducibility.

## How to Run
Open the notebook in Google Colab, select a compatible GPU,
install the listed dependencies, and run the cells in order.
