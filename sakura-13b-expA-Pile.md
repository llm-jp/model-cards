# (model name)

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|40|
|Number of embedding units|5120|
|Number of FFN hidden units|13824|
|Number of attention heads|40|
|Vocabulary size|101047 (+73 dummy 101120)|
|Maximum sequence length|2048|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3 (all languages except english) & LLM-jp v1.0.1 English-Pile|
|Number of tokens|250B (4096*62776350)|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|https://github.com/llm-jp/Megatron-LM/commits/402e6ff1|
|Optimizer|Adam|
|Initial learning rate|1e-4|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-8|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|*100,000*|
|Total training steps|61000|
|Global batch size|1024|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash attention|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Sakura (ishikari)|
|Number of instances|8|
|Processor|Intel(R) Xeon(R) Platinum 8480+|
|Number of processors per instance|1|
|RAM|2014 GiB|
|Accelerators|NVIDIA H100 * 64|
|Number of accelerators per instance|8|
|high-speed connection|NVLink|

# Comments

Describe other details of this model.
