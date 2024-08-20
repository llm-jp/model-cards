# geniac-13b-exp4

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|40|
|Number of embedding units(hidden size)|5120|
|Number of FFN hidden units(intermediate size)|13824|
|Number of attention heads|40|
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
|Implementation|[Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/9c8d91d6667a12e97bb84f103dbbe16f08dddcbb)|
|Optimizer|AdamW|
|Initial learning rate|2e-4|
|Final learning rate|2e-5|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-8|
|Weight decay factor|0.1|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|492120|
|Total training steps|494120|
|Global batch size|1,024|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|
|Embedding scale|❌|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Google Cloud (asia-southeast1-c)|
|Number of Nodes|32|
|Processor|Intel(R) Xeon(R) Platinum 8481C CPU @ 2.70GHz|
|Number of CPUs per instance|2|
|RAM|1.8TiB|
|Accelerators|NVIDIA H100 80GB|
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|

|Spec name|Value|
|:---|:---|
|Name|Sakura Internet|
|Number of Nodes|32|
|Processor|Intel Xeon Platinum 8480|
|Number of CPUs per instance|2|
|RAM|2.0TB|
|Accelerators|NVIDIA H100 80GB|
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|

# Comments

Run on Sakura Internet after iteration 15000
