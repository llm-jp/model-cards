# mdx 1.7b

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|24|
|Number of embedding units(hidden size)|2048|
|Number of FFN hidden units(intermediate size)|7168|
|Number of attention heads|16|
|GQA|✅|
|Number of key value heads|8|
|Vocabulary size|99,487|
|Maximum sequence length|4096|
|Positional embedding|RoPE|

# Dataset specs
|Spec name|Value|
|:---|:---|
|Dataset|LLM-jp v3|
|Number of tokens|2.1T|

# Training specs

|Spec name|Value|
|:---|:---|
|Implementation|[Megatron-LM](https://github.com/llm-jp/Megatron-LM/tree/0cc02dff7943fddc53da42d8893dafe28ec3cf8e)|
|Optimizer|AdamW|
|Initial learning rate|3e-4|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-5|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|1,009,579|
|Total training steps|1,009,579|
|Global batch size|512|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash Attention|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|mdx|
|Number of Nodes|8|
|Processor|Intel Xeon Platinum 8368 Processor (38core, 2.4GHz)|
|Number of processors per instance|2|
|RAM|448 GiB|
|Accelerators|NVIDIA Tesla A100 40GiB|
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|

# Comments

`1009579 * 512 * 4096 = 2,117,240,619,008`
trainデータを1epoch見るようにスケジューリングをしています。

学習データはGENIAC 172Bモデルと同様であるため、GENIAモデルのモデルサイズ縮小版としての性格をもちます。