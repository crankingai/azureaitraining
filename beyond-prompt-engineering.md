# Beyond Prompt Engineering

What are some options available to application developers to influence the responses from LLM systems?

| Execution Control  | Category | Control Methods |
|--------------------|----------|----------------|
| Application        | Model Selection | - LLMs (e.g., GPT, Claude, Llama) vs. SLMs (e.g., Phi-4)<br>- Domain-specific models (e.g., Stable Diffusion for images, Whisper for speech)<br>- Multi-modal models<br>- Open source vs. closed source models |
| Application        | Model Tuning | - Fine-tuning |
| Application        | Prompt Engineering | - Zero-shot prompting<br>- Few-shot prompting<br>- Chain of thought reasoning<br>- Template Prompting (for JSON or Markdown) |
| Application        | Prompt Execution Parameters | - Temperature (randomness)<br>- Top-p (nucleus sampling)<br>- Max tokens |
| Application        | Prompt Safety Engineering | - Meta-prompt to deflect attacks or avoid hallucinations (e.g., "if you don't know the answer, return 'I have insufficient data to answer that question'." or "for any topics outside the scope of open source software licenses, reply with 'I only know about software licenses'.") |
| Application or Agent (LLM) | Prompt Data Augmentation | - Retrieval Augmented Generation (RAG)<br>- Vector databases<br>- Context window optimization<br>- Document chunking strategies<br>- Semantic search integration<br>- Knowledge graph integration |
| Application or Agent (LLM) | Function Calling | - Function/Tool access (prompt and native)<br>- API integrations<br>- System time and date access<br>- File system operations<br>- Database queries<br>- External service calls |
| Application        | Pre-Model Prompt Filtering | - Content filtering<br>- Jailbreak & Prompt Injection prevention<br>- Content guidelines enforcement |
| Application        | Post-Model Response Filtering | - Content filtering<br>- Output sanitization<br>- Content guidelines enforcement (ethics, bias, others) |
| Application        | Evaluation & Monitoring | - Output quality metrics<br>- Response time monitoring<br>- Error rate tracking<br>- Cost tracking<br>- Usage analytics<br>- A/B testing frameworks |

## Latency, Cost, Quality, Privacy, Security

<!-- beam search -->
