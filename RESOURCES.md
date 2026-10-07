# Ресурсы

Материалы по проекту «Исследование методов сжатия и ускорения малых языковых моделей (SLM)».

## Квантование и дообучение

- [QLoRA: Efficient Finetuning of Quantized LLMs (NeurIPS 2023)](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1feb87871436031bdc0f2beaa62a049b-Abstract.html) — 4-битная база (NF4) + LoRA-адаптеры, качество на уровне 16-битного дообучения.

## Прунинг и дистилляция

- [LLM Pruning and Distillation in Practice: The Minitron Approach (arXiv 2408.11796)](https://arxiv.org/html/2408.11796v3) — структурный прунинг (по глубине и ширине) с последующей дистилляцией.
- [NVIDIA: How to Prune and Distill Llama 3.1 8B to Minitron 4B](https://developer.nvidia.com/blog/how-to-prune-and-distill-llama-3-1-8b-to-an-nvidia-llama-3-1-minitron-4b-model) — практическое руководство; ускорение 2.7× (depth) и 1.8× (width) относительно 8B. Результаты получены на моделях 8B+, для 1–3B данных мало.

## Квантование и качество на коде и математике

- [Smaller = Weaker? Benchmarking Robustness of Quantized LLMs in Code Generation (arXiv 2506.22776)](https://arxiv.org/pdf/2506.22776)
- [Evaluating Quantized LLMs for Code Generation on Low-Resource Language Benchmarks (arXiv 2410.14766)](https://arxiv.org/pdf/2410.14766)
- [Precision or Peril: Python Code Quality from Quantized LLMs (arXiv 2411.10656)](https://arxiv.org/pdf/2411.10656)

## Инференс и методика замеров

- [llama.cpp vs vLLM](https://deploybase.ai/articles/llama.cpp-vs-vllm) — сравнение движков; llama.cpp лучше для одиночных запросов, vLLM для батчей.
- [bitsandbytes vs llama.cpp vs exllamav2](https://www.index.dev/skill-vs-skill/ai-bitsandbytes-vs-llamacpp-vs-exllamav2)

Заметка по методике (из найденных источников): batch 1, фиксированные длины промпта и генерации, 10 прогонов и медиана; метрики TTFT, inter-token latency, tokens/s, пиковая VRAM; prefill и decode считаются отдельно.

## Инструменты

Ссылки не проверялись поиском, названия приведены по общим знаниям.

- transformers, peft, trl, bitsandbytes
- AutoGPTQ, AutoAWQ
- llama.cpp (GGUF), vLLM
- lm-evaluation-harness, evalplus (HumanEval+/MBPP+)
- LLM-Pruner
