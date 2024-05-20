# geniac-13b-exp2

# Model specs

|Spec name|Value|
|:---|:---|
|Base model structure|Llama-2|
|Number of layers|40|
|Number of embedding units(hidden size)|5120|
|Number of FFN hidden units(intermediate size)|13824|
|Number of attention heads|40|
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
|Implementation|[Megatron-LM](https://github.com/Taishi-N324/Megatron-LM/tree/61447ffbc2cf60035428cea9c112565cfe32e33a)|
|Optimizer|Adam|
|Initial learning rate|2e-4|
|Beta1|0.9|
|Beta2|0.95|
|Epsilon|1e-8|
|Warmup strategy|Linear|
|Warmup steps|2000|
|Learning rate scheduling strategy|Cosine|
|Learning rate scheduling steps|452,995|
|Total training steps|452,995|
|Global batch size|1,024|
|Dropout rate|0.0|
|Floating point precisions|BF16|
|Additional randomness/approximation|Flash Attention|
|Z loss|1e-4|
|Embedding scale|✅|

# Environmental specs

|Spec name|Value|
|:---|:---|
|Data center|Google Cloud (asia-southeast1-c)|
|Number of Nodes|8|
|Processor|Intel(R) Xeon(R) Platinum 8481C CPU @ 2.70GHz|
|Number of CPUs per instance|2|
|RAM|1.8TiB|
|Accelerators|NVIDIA H100 80GB|
|Number of accelerators per instance|8|
|Intra Node Communication |NVLink|

# Comments

Loss spikeの対策に、Z loss、Embedding scale、BF16の使用に加え、LRを2e-4にしています。

学習データはGENIAC 172Bモデルと同様であるため、GENIAモデルのモデルサイズ縮小版としての性格をもちます。