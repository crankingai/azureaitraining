# Microsoft's AI Service Offerings (old, new)

> AI AUTHORSHIP: Human owner Bill Wilder, guided AI generation by AI Claude 3.7 Sonnet, human modified AI response, human did not fact check

## Summary from Claude:

Older Microsoft AI cognitive services like LUIS and QnA Maker did not use the same underlying LLMs as newer Microsoft AI Language services. The older services were primarily built on traditional machine learning techniques, statistical models, and specialized neural networks, whereas newer services leverage large language models (primarily GPT-based models from their partnership with OpenAI).

In the table below are different Microsoft AI services and the technologies that power them. You'll notice a clear evolution from specialized ML models to more generalized large language models over time.

Microsoft has been gradually deprecating older services like LUIS and QnA Maker in favor of their newer counterparts that utilize LLM technology. They've created migration paths to help customers transition from the older services to the newer, more capable offerings.

### Microsoft AI Services and Their Underlying Models

| Service/Feature | Generation | Underlying Model Technology | Notes |
|-----------------|------------|------------------------------|-------|
| **LUIS** (Language Understanding) | Older (Cognitive Services) | Custom ML models, not LLMs | Being deprecated in favor of CLU |
| **QnA Maker** | Older (Cognitive Services) | Information Retrieval + ML (not LLM-based) | Being deprecated in favor of Language Studio features |
| **CLU** (Conversational Language Understanding) | Newer (Azure AI Language) | GPT-based models | Successor to LUIS, uses modern LLM technology |
| **Custom Question Answering** | Newer (Azure AI Language) | GPT-based models | Successor to QnA Maker |
| **Azure OpenAI Service** | Newest | GPT-3.5, GPT-4, other OpenAI models | Direct access to OpenAI's models via Azure |
| **Bing Chat** | Newest | GPT-4 with customizations | Consumer-facing service using advanced LLMs |
| **Microsoft Copilot for Microsoft 365** | Newest | GPT-4 with customizations | Enterprise productivity offering |
| **Azure AI Search** (formerly Cognitive Search) | Evolved | Information Retrieval + LLM integration options | Can be integrated with LLMs for RAG patterns |
| **[Azure AI Language Services](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)** | Evolved | ML models with GPT enhancement options | Original features used ML, newer ones leverage LLMs. Encompasses Text Analytics alongside other natural language processing (NLP) capabilities, replacing older standalone services like LUIS and QnA Maker68. |
| **[Azure AI Speech Services](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/)** | Evolved | Neural networks (not LLM-based) with newer LLM options | Original features used neural networks, newer ones may leverage LLMs. Speech Synthesis services support [Speech Synthesis Markup Language (SSML)](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-synthesis-markup), though it
is not required. |

## Key Transition Points

1. **2018-2021**: Primarily traditional ML methods, statistical models, and neural networks
2. **2021-2023**: Transition to GPT-based models and integration of OpenAI technology
3. **2023-Present**: Unified approach with Azure AI, consolidating many services under OpenAI-based technologies

## Migration Paths

* LUIS → CLU (Conversational Language Understanding)
* QnA Maker → Custom Question Answering
* Multiple cognitive services → Azure AI Language or Azure OpenAI Service
