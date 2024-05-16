# (model name)

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|12|
|Number of embedding units|1024|
|Number of FFN hidden units|4096|
|Number of attention heads|16|
|Vocabulary size|65536|
|Maximum sequence length|2048|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3 (link)|
|Number of tokens|2.1T|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|Megatron-LM (link to commit)|
|Optimizer|AdamW|
|Initial learning rate|1e-4|
|Beta1|0.9|
|Beta2|0.999|
|Epsilon|1e-4|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|100,000|
|Total training steps|120,000|
|Global batch size|1536|
|Dropout rate|0.2|
|Floating point precisions|BF16 for parameters, FP32 for optimizer|
|Additional randomness/approximation|Flash attention, ...|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Google Cloud (asia-southeast1-c)|
|Number of instances|64|
|Processor|Intel Xeon xxxx|
|Number of processors per instance|1|
|RAM|512GiB|
|Accelerators|NVIDIA H100 * 64|
|Number of accelerators per instance|8|
|high-speed connection|NVLink|

# Comments

Describe other details of this model.


