# t4-llama-2-70b

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
|max_position_embeddings|4096|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3|
|Number of tokens|2,100,002,291,712 (=2.1T)|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|[Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/0cc02dff7943fddc53da42d8893dafe28ec3cf8e)|
|Optimizer|AdamW|
|Initial learning rate|1e-4|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-5|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate Decay steps|268,442 (=1.9T Token)|
|Total training steps|296,699|
|Global batch size|1728|
|Dropout rate|0.0|
|Floating point precisions|BF16 -> BF16 + FP8|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Google Cloud (asia-southeast1-c)|
|Number of Nodes|64|
|CPU|Intel(R) Xeon(R) Platinum 8481C CPU @ 2.70GHz|
|RAM|1.8TB|
|Accelerators| NVIDIA H100 80GB |
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|
|Inter Node Communication|GPU Direct TCPX-v7|

# Comments

7,000 iteration 以降は TransformerEngine FP8 hybrid 機能を利用しています。
