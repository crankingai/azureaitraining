# Beyond Prompt Engineering

What are some options available to application developers that influence the value of responses coming back from LLM systems?

| Execution Flow  | Category | Control Methods |
|--------------------|----------|----------------|
| Application addresses a specific model via API | Model Selection (cost, latency, quality, privacy, complexity) | - LLMs (e.g., GPT, Claude, Llama) vs. SLMs (e.g., Phi-4)<br>- Multi-modal models (e.g., GPT o1) vs. Domain-specific models (e.g., Stable Diffusion for images, Whisper for speech, models focused on code generation)<br>- Open source vs. closed source models<br>- Hosted vs. Self-hosted |
| Application sends with prompt | Prompt Execution Knobs | - Temperature (randomness - probability of choosing less likely tokens)<br>- Top-p (nucleus sampling - which tokens to include when sampling)<br>- Max tokens (token budget) |
| Application sends this prompt | Prompt Engineering | - Zero-shot prompting<br>- Few-shot prompting<br>- Chain of thought reasoning (note also GPT o1)<br>- Template Prompting (e.g., JSON, Markdown, or THIS EXACT JSON)<br>- Meta-prompt may be used for context ("you are a playful assistant who uses fun emojis in your responses") |
| Application sends prompt that includes this data | Prompt Data Augmentation | - Retrieval Augmented Generation (RAG) (grounding data, contextual data)<br>- RAG data may or may not be retrieved via semantic search from vector database or knowledge graph<br>- RAG data may or may not be the result of "chunked" documents<br>- RAG being applied within the prompt
| Application registers available functions and LLM executes inline | Function Calling | - Local prompt function<br>- Local native function<br>- Remote API (e.g., OpenAPI)<br>- For native and remote consider "anything behind an API" possible<br>- Example zero-shot prompt that uses a simple function: "Today is {{getCurrentDate}}. What are some significant events that happened on this day in history?" |
| Application registers available functions and LLM<br>(in **Agent mode**) decides which ones to invoke | Function Calling | - Local prompt function<br>- Local native function<br>- Remote API (e.g., OpenAPI)<br>- For native and remote consider "anything behind an API" possible<br>- RAG, date/time, weather, location, customer orders database, etc.<br>- If RAG available via Function, then its use it determined by the LLM |
| Application sends this prompt| Prompt Engineering for Safety | - Meta-prompt to deflect attacks ("for any topics outside the scope of open source software licenses, reply with 'I only know about software licenses'")<br>- Meta-prompt to minimize hallucinations (e.g., "if you don't know the answer, return 'I have insufficient data to answer that question'") |
| Application (or delegated, such as to Azure AI Foundry [`Prompt Shields`](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/jailbreak-detection) service) | Pre-Model Prompt Filtering | - Content filtering<br>- Jailbreak & Prompt Injection prevention<br>- Content guidelines enforcement (ethics, bias, others) |
| Application (or delegated, such as to Azure AI Foundry [`Prompt Shields`](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/jailbreak-detection) service) | Post-Model Response Filtering | - Content filtering<br>- Output sanitization<br>- Content guidelines enforcement (ethics, bias, others) |
| LLM        | Model Tuning | - Fine-tuning applied to offline model<br>- Fine-tuning effects are then apparent in the LLM output |

<!-- Add beam search? -->

<!-- Bill Wilder, https://github.com/crankingai/azureaitraining/blob/main/beyond-prompt-engineering.md -->
