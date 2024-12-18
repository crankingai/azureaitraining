# Beyond Prompt Engineering

What are some options available to application developers that influence the value of responses coming back from LLM systems?

| Execution Control  | Category | Control Methods |
|--------------------|----------|----------------|
| Application        | Model Selection (cost, latency, quality, privacy, complexity) | - LLMs (e.g., GPT, Claude, Llama) vs. SLMs (e.g., Phi-4)<br>- Multi-modal models (e.g., GPT o1) vs. Domain-specific models (e.g., Stable Diffusion for images, Whisper for speech, models focused on code generation)<br>- Open source vs. closed source models<br>- Hosted vs. Self-hosted |
| Application        | Prompt Execution Knobs | - Temperature (randomness - probability of choosing less likely tokens)<br>- Top-p (nucleus sampling - which tokens to include when sampling)<br>- Max tokens (token budget) |
| Application        | Prompt Engineering| - Zero-shot prompting<br>- Few-shot prompting<br>- Chain of thought reasoning (note also GPT o1)<br>- Template Prompting (e.g., JSON, Markdown, or THIS EXACT JSON)<br>- Meta-prompt may be used for context ("you are a playful assistant who uses fun emojis in your responses") |
| Application or Agent (LLM) | Prompt Data Augmentation | - Retrieval Augmented Generation (RAG) (grounding data, contextual data)<br>- RAG data may or may not be retrieved via semantic search from vector database or knowledge graph<br>- RAG data may or may not be the result of "chunked" documents
| Application or Agent (LLM) | Function Calling | - Local prompt function<br>- Local native function<br>- Remote API (e.g., OpenAPI)<br>- For native and remote consider "anything behind an API" possible |
| Application        | Prompt Engineering for Safety | - Meta-prompt to deflect attacks ("for any topics outside the scope of open source software licenses, reply with 'I only know about software licenses'")<br>- Meta-prompt to minimize hallucinations (e.g., "if you don't know the answer, return 'I have insufficient data to answer that question'") |
| Application        | Pre-Model Prompt Filtering | - Content filtering<br>- Jailbreak & Prompt Injection prevention<br>- Content guidelines enforcement (ethics, bias, others) |
| Application        | Post-Model Response Filtering | - Content filtering<br>- Output sanitization<br>- Content guidelines enforcement (ethics, bias, others) |
| Application        | Model Tuning | - Fine-tuning |

<!-- Add beam search? -->

<!-- Bill Wilder, https://github.com/crankingai/azureaitraining/blob/main/beyond-prompt-engineering.md -->
