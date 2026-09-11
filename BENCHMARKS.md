# LocalAgentStack Empirical Hardware & VRAM Benchmarks

Comprehensive hardware benchmarks, memory footprints, and token throughput for local LLM inference engines.

⚡ **Interactive Calculators & Guides:** [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/)

## 1. Dual RTX 3090 vs RTX 4090 Throughput Matrix

| Model | Quantization | Context | Dual RTX 3090 (48GB) | Single RTX 4090 (24GB) | Apple M4 Max (128GB) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| DeepSeek-R1 70B | IQ4_XS | 16k | 20.4 tok/s | Offload bottleneck (4.2 tok/s) | 14.8 tok/s |
| Llama-3.3 70B | Q4_K_M | 8k | 18.2 tok/s | Offload bottleneck (3.8 tok/s) | 15.6 tok/s |
| Qwen-2.5 32B | Q8_0 | 32k | 28.5 tok/s | 34.2 tok/s | 26.1 tok/s |
| Llama-3.1 8B | FP16 | 64k | 82.0 tok/s | 114.5 tok/s | 68.0 tok/s |

## 2. VRAM Formula
$$\text{VRAM}_{\text{Total}} = \text{Weights}_{\text{GB}} + \text{KV\_Cache}_{\text{GB}} + \text{CUDA\_Overhead}_{\text{GB}}$$
- For 70B @ 4-bit with 16k context: $38.5\text{GB} + 3.2\text{GB} + 1.2\text{GB} = 42.9\text{GB}$ VRAM required.

---
Empirical benchmark suite provided by [LocalAgentStack](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/).

## 📚 In-Depth Technical Implementation Guides

| Target Engineering Query | Production Reference & Guide URL |
| :--- | :--- |
| **Ollama Vs Vllm Benchmark 2026** | [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/inference/ollama-vs-vllm-benchmark/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/inference/ollama-vs-vllm-benchmark/) |
| **Deepseek R1 Local Setup Ollama** | [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/models/deepseek-r1-local-setup-ollama/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/models/deepseek-r1-local-setup-ollama/) |
| **Vram Requirements Calculator 70B** | [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/hardware/vram-requirements-calculator-70b/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/hardware/vram-requirements-calculator-70b/) |
| **Llama.Cpp Vs Vllm Memory Overhead 4-Bit** | [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/hardware/llamacpp-vs-vllm-4bit-memory-overhead/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/hardware/llamacpp-vs-vllm-4bit-memory-overhead/) |
| **Deepseek R1 32B Vs 70B Coding Benchmark** | [https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/models/deepseek-r1-32b-vs-70b-coding/](https://jibranpcccc.github.io/digitalcreatoravi-seo-engine/models/deepseek-r1-32b-vs-70b-coding/) |

