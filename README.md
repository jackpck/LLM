# 0. Setup

This repo was first created using python ```3.7.4```, which is too old for the newer 
version of ```transformers``` library such as version ```4.35.2```, which is needed to
install some of the newer LLM such as Mistral 7b or falcon 7b. The virtual environment
based on python ```3.7.4``` is saved in ```requirements.txt```.

To get around this, a new virtual environment is created under python ```3.8.0```. This
includes newer version of ```torch``` (compatible with whatever CUDA version your local computer
is running) and newer version of ```transformers```. This venv is saved in 
```requirements_py38.txt```.

To ```pip install -r requirements_py38.txt```, make sure you are using python ```3.8.0```. Create
ipykernel to increase flexibility in case you are working with different python versions.

# I. Milestone 4/30

## 1. Theory

### 1.1 Backpropagation
[reference (autodiff)](https://www.cs.toronto.edu/~rgrosse/courses/csc421_2019/readings/L04%20Backpropagation.pdf)

### 1.2 Fine-tuning

#### Full/partial fine tuning

#### Bias-only fine tuning

#### Prefix-layer fine tuning

#### Adapter

#### LoRA, QLoRA
[reference (comparison and best practices)](https://cloud.google.com/vertex-ai/generative-ai/docs/model-garden/lora-qlora#:~:text=Tuning%20recommendations,-The%20following%20table&text=LoRA%20is%20about%2066%25%20faster,in%20terms%20of%20tuning%20speed.&text=While%20both%20methods%20are%20relatively,40%25%20less%20expensive%20than%20QLoRA.&text=Higher%20max%20sequence%20length%20increases,support%20higher%20max%20sequence%20lengths.)

#### Instruction fine tuning
[reference: FLAN](https://research.google/blog/introducing-flan-more-generalizable-language-models-with-instruction-fine-tuning/)
[reference](https://arxiv.org/pdf/2210.11416)

### 1.3 Optimizier
[reference: p13, section IV (GD)](https://arxiv.org/pdf/1803.08823.pdf)

[reference (Normalization)](https://www.cs.toronto.edu/~rgrosse/courses/csc2541_2021/readings/L05_normalization.pdf)

[reference (SGD)](https://www.cs.toronto.edu/~rgrosse/courses/csc2541_2021/slides/lec07.pdf)

[HF troubleshooting guide](https://huggingface.co/docs/transformers/v4.18.0/en/troubleshooting)

### Gradient descent (first-order, second-order)

### Learning rate, scheduler

### Batch size

### Regularization

### Weight decay

# 2. Engineering

## 2.1 Hardware

### 2.1.1 Data/model storage

### 2.1.2 Computation (cpu, gpu, tpu)
[reference (GPU calculation)](https://www.substratus.ai/blog/calculating-gpu-memory-for-llm:w
)

## 2.2 Software

### 2.2.1 Virtual environment:

### 2.2.2 Various techniques

[reference](https://huggingface.co/docs/transformers/en/llm_tutorial_optimization)

#### Mixed precision/ Quantization
[GPU inference with mixed precision best practices](https://huggingface.co/docs/transformers/en/perf_infer_gpu_one)


#### Sharded model

#### Gradient accumulation

[reference](https://lightning.ai/blog/gradient-accumulation/)

## 3. Reference
[google cloud](https://cloud.google.com/vertex-ai/generative-ai/docs/model-garden/lora-qlora#:~:text=Tuning%20recommendations,-The%20following%20table&text=LoRA%20is%20about%2066%25%20faster,in%20terms%20of%20tuning%20speed.&text=While%20both%20methods%20are%20relatively,40%25%20less%20expensive%20than%20QLoRA.&text=Higher%20max%20sequence%20length%20increases,support%20higher%20max%20sequence%20lengths.)

# II. Milestone 5/31

## 1. Generative LLM
[generation config](https://huggingface.co/docs/transformers/generation_strategies)

## 2. Prompting/few-shot learning

[SetFit (not really prompting. It's few-shot fine tuning)](https://huggingface.co/blog/setfit)


## 3. Sampling/ decoding strategies
[decoding strategies](https://huggingface.co/blog/how-to-generate)
- Multinomial sampling
- beam-search multinomial sampling
- Top-K sampling 
- Top-p sampling

# III. Milestone 6/30

## RAG

# IV. Milestone 7/31

## RLHF

# Misc

[falcon](https://huggingface.co/blog/falcon)
[useful information](https://huggingface.co/docs/transformers/en/glossary)