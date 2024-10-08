# LLM-jp v3 70B experiment 1

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|80|
|Number of embedding units(hidden size)|8192|
|Number of FFN hidden units(intermediate size)|28672|
|Number of attention heads|64|
|GQA|✅|
|Number of key value heads|8|
|Vocabulary size|99,487|
|Tokenizer|[llm-jp-tokenizer-100k.ver3.0b1.model](https://github.com/llm-jp/llm-jp-tokenizer/blob/870a27ce6872e105e4b76cdf2e68c8b7ebfc6a37/models/ver3.0/llm-jp-tokenizer-100k.ver3.0b1.model)|
|Maximum sequence length|4096|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3|
|Number of tokens|2,117,241,409,943 Token|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|[Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/7b45c6ca5793ab3c7eba7c53863930dd538b83bf)|
|Optimizer|AdamW|
|Initial learning rate|1e-4|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-5|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|512,696|
|Total training steps|512,696|
|Global batch size|1000|
|Dropout rate|0.0|
|Floating point precisions 1~21,500 iter|
BF16|
|Floating point precisions 21,501 iter~|fp8-hybrid|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|
|Tensor parallel size|4|
|Pipeline parallel size|4|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|TSUBAME 4.0|
|Number of Nodes|40|
|CPU|AMD EPYC 9654|
|Number of CPUs per instance|2|
|RAM|768 GiB|
|Accelerators| NVIDIA H100 SXM5 94GB HBM2e |
|Number of accelerators per instance|4|
|Intra Node Communication |NVLink|

# Comments

2024年 夏 に学習予定の8x70B MoEモデルの元になる予定です。
学習データはGENIAC 172Bモデルと同様であるため、GENIAモデルのモデルサイズ縮小版としての性格をもちます。

速度向上のため、21,501 iterからfp8-hybridに変更