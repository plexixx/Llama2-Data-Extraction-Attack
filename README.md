# Llama2-Data-Extraction-Attack

This project investigates the vulnerability of large language models (LLMs) to training data extraction attacks, following the methodology proposed by "Extracting Training Data from Large Language Models" ([Carlini et al., 2020](https://arxiv.org/abs/2012.07805)). The study evaluates whether newer models (specifically Llama2-7B) exhibit similar tendencies to memorize and leak sensitive data as earlier models like GPT-2.

## Key Features
- **Top-n Sampling:** Generates diverse outputs by selecting from the top $n$ most probable tokens for each step, balancing creativity and coherence.
- **Decaying Temperature Sampling:** Introduces diversity by starting with a high temperature and gradually reducing it, enabling exploratory generation followed by deterministic output.
- **Perplexity-Based Filtering:** Evaluates model outputs to identify highly confident predictions that may indicate memorized content.
- **Quantized Model Usage:** Utilizes quantized versions of Llama2-7B using [llama-cpp-python](https://github.com/abetlen/llama-cpp-python) for efficient computation and evaluation.
