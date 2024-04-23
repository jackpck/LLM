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

### 2.2.1 Virtual environement:

### 2.2.2 Various techniques

[reference](https://huggingface.co/docs/transformers/en/llm_tutorial_optimization)

#### Mixed precision

#### Sharded model

## 3. Reference
[google cloud](https://cloud.google.com/vertex-ai/generative-ai/docs/model-garden/lora-qlora#:~:text=Tuning%20recommendations,-The%20following%20table&text=LoRA%20is%20about%2066%25%20faster,in%20terms%20of%20tuning%20speed.&text=While%20both%20methods%20are%20relatively,40%25%20less%20expensive%20than%20QLoRA.&text=Higher%20max%20sequence%20length%20increases,support%20higher%20max%20sequence%20lengths.)

# II. Milestone 5/31

## 1. Generative LLM
[generation config](https://huggingface.co/docs/transformers/generation_strategies)

## 2. Prompting/few-shot learning

[SetFit](https://huggingface.co/blog/setfit)

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