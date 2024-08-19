# RAG note from [Huggingface](https://huggingface.co/learn/cookbook/en/advanced_rag)

## 1. Chunking
- Text splitter
  - Recursive text splitter
  - semantic chunking
- Hyperparameters
    - chunk size
    - chunk overlap
    
- Make sure chunk size is calculated on number of tokens, not number of characters
- Make sure chunk size is less than the max sequence length of the embedding model

## 2. [Sentence embedding](https://osanseviero.github.io/hackerllama/blog/posts/sentence_embeddings/)

## 3. Retrieval

### 3.1 Vector database
- Nearest neighbor search algorithm
  - FAISS (for indexing)
  - Note on choice of different metrics (cosine similarity, dot product, Euclidean distance)
  
### 3.2 Knowledge graph
  
### 3.3 Reranker
Maximize **retrieval recall** by retrieving more documents than you want and then maximize **LLM recall** by minimizing 
the number of documents that make it to the LLM. This is achieved by building a reranking model, or **cross-encoder**.

Cross-encoder is much slower, but more accurate than embedding model.

Example of cross-encoder: Colbertv2
  
## 4. Reader

### 4.1 Aggregation

- Step 1: The content of the retrieved documents is aggregated together into the 'context', with many processing options like *prompt compression*
- Step 2: The context and the user query are aggregated into a prompt to an LLM to generate answer

- Use reader model with longer max sequence length to fit in aggregation of multiple retrieved chunks
- Look out for the *Lost-in-the-middle phenomenon* when doing context window stuffing (pass long retrieved prompt into the reader LLM)

## 5. [Evaluation](https://docs.llamaindex.ai/en/stable/module_guides/evaluating)
- **Correctness**: response vs ground truth (require label)
- **Semantic similarity**: response vs ground truth, semantically (require label)
- **Faithfulness**: response vs retrieved context (check for hallucination)
- **Context relevancy**: retrieved context vs query
- **Answer relevancy**: response vs query
- **Guideline adherence**: response vs specific guidelines

For usage pattern, see [reference](https://docs.llamaindex.ai/en/stable/module_guides/evaluating/usage_pattern/)

[Evaluation of RAG - A Survey](https://arxiv.org/pdf/2405.07437)

## N. Miscellaneous

### N.1 Query expansion

### N.2 Dimension reduction
- t-SNE
- UMAP
- PaCMAP

### N.3 Technology

- Langchain text splitter
- unstructured.io
- Microsoft LLMLingua Prompt Compression
- Vector database
- Knowledge Graph
