# Japanese LLM Benchmark Suite

A lightweight benchmarking suite for Japanese-language large-scale models.  
Focus: **inference speed, memory efficiency, and generation quality** across multiple deployment methods.

## Objectives

- Compare performance of Japanese-specific models (`rinna`, `cl-tohoku`, etc.)
- Evaluate quantized variants (QLoRA, GPTQ)
- Analyze tradeoffs: speed vs accuracy vs memory
- Build a reproducible benchmark on minimal hardware (MacBook M1+)

## Models Covered

| Model                        | Type           | Tokenizer         |
|-----------------------------|----------------|-------------------|
| rinna/japanese-gpt2-medium  | GPT-style      | SentencePiece     |
| cl-tohoku/bert-base-japanese-v2 | BERT      | WordPiece         |
| distil-japanese-BERT        | Distilled BERT | WordPiece         |

## ⛮ Inference Backends

- Transformers (CPU/GPU)
- ONNX Runtime
- GGUF / llama.cpp (planned)

## Benchmark Metrics

- Tokens/sec (inference throughput)
- Memory usage (resident size, max alloc)
- Quality scores (BLEU, ROUGE, JL-BERTScore)

## Dataset Sources

- 青空文庫 (Aozora Bunko)
- livedoorニュースコーパス
- 日本語 Wikipedia 抜粋

## Results Preview

Coming soon — benchmark tables for:
- QLoRA vs GPTQ performance on `rinna` models
- SentencePiece vs WordPiece tokenization drift
- ONNX vs Transformers latency on CPU

## Blog + Results

- [Blog 1: 「LLM推論をMacで始める方法」 (予定)](link)
- [Blog 2: 「日本語LLMの量子化比較：QLoRA vs GPTQ」 (予定)](link)

## 📄 License

MIT. See `LICENSE.md`.
