# geniac-172b-exp2

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|num_hidden_layers|96|
|hidden_size|12288|
|intermediate size|38464|
|num_attention_heads|96|
|GQA|✅|
|num_key_value_heads|16|
|Vocabulary size|99,487|
|Tokenizer|[llm-jp-tokenizer-100k.ver3.0b1.model](https://github.com/llm-jp/llm-jp-tokenizer/blob/870a27ce6872e105e4b76cdf2e68c8b7ebfc6a37/models/ver3.0/llm-jp-tokenizer-100k.ver3.0b1.model)|
|max_position_embeddings|4096|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3.1|
|Number of tokens|**FIXME**|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation| **FIXME (link)** [Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/0cc02dff7943fddc53da42d8893dafe28ec3cf8e)|
|Optimizer|AdamW|
|Initial learning rate|8e-5|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-8|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate Decay steps|**FIXME**|
|Total training steps|**FIXME**|
|Global batch size|1728|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Google Cloud (asia-southeast1-c)|
|Number of Nodes|64|
|CPU|Intel(R) Xeon(R) Platinum 8481C CPU @ 2.70GHz|
|RAM|1.8TB|
|Accelerators|NVIDIA H100 80GB|
|Number of accelerators per instance|8|
|Intra Node Communication|NVLink|
|Inter Node Communication|GPU Direct TCPX-v7|

# Comments

**TBD**
