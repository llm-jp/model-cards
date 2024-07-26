# mdx-1.7b-exp2

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|24|
|Number of embedding units(hidden size)|2048|
|Number of FFN hidden units(intermediate size)|7168|
|Number of attention heads|16|
|Vocabulary size|99,487|
|Tokenizer|[llm-jp-tokenizer-100k.ver3.0b1.model](https://github.com/llm-jp/llm-jp-tokenizer/blob/870a27ce6872e105e4b76cdf2e68c8b7ebfc6a37/models/ver3.0/llm-jp-tokenizer-100k.ver3.0b1.model)|
|Maximum sequence length|4096|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3.1|
|Number of tokens|2,072,488,058,295|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|**FIXME** [Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/******)|
|Optimizer|AdamW|
|Initial learning rate|3e-4|
|Final learning rate|3e-5|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-8|
|Weight decay factor|0.1|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|986,240|
|Total training steps|988,240|
|Global batch size|512|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|
|Embedding scale|❌|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|mdx|
|Number of Nodes|16|
|Processor|Intel Xeon Platinum 8368 Processor (38core, 2.4GHz)|
|Number of processors per instance|2|
|RAM|448 GiB|
|Accelerators|NVIDIA Tesla A100 40GiB|
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|

# Comments
