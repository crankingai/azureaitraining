# Microsoft AI Services Hierarchy

> AI AUTHORSHIP: Human owner Bill Wilder, guided AI generation by AI Claude 3.7 Sonnet, human modified AI response, human did not fact check

## Overview

This table provides a hierarchical view of Microsoft's AI services, 
showing the evolution from specialized ML models to more generalized large language models. 
Services are organized by category with umbrella services expanded to show their complete offerings.

## Key Transition Points

1. **2018-2021**: Primarily traditional ML methods, statistical models, and neural networks
2. **2021-2023**: Transition to GPT-based models and integration of OpenAI technology
3. **2023-Present**: Unified approach with Azure AI, consolidating many services under OpenAI-based technologies

## Azure OpenAI Service

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **[Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/ai-services/openai/)** | Active | GPT-3.5, GPT-4, other OpenAI models | Consumption-based | Enterprise LLM integration, RAG applications, AI assistants | Direct access to OpenAI's models via Azure with added security and compliance features |

## [Azure AI Language Services](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)

Natural language processing (NLP) services. 

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **[Conversational Language Understanding (CLU)](https://learn.microsoft.com/en-us/azure/ai-services/language-service/conversational-language-understanding/overview)** | Active | GPT-based models | Free tier (limited), then consumption | Intent recognition, entity extraction | Successor to LUIS, uses modern LLM technology |
| **[Custom Question Answering](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/overview)** | Active | GPT-based models | Free tier (limited), then consumption | FAQ bots, knowledge base creation | Successor to QnA Maker |
| **Text Analytics** | Active | ML models with GPT enhancement options | Consumption-based | Content analysis, sentiment detection | Includes sentiment analysis, key phrase extraction |
| **Named Entity Recognition** | Active | ML models | Consumption-based | Document processing, content tagging | Identifies entities like people, places, organizations |
| **Sentiment Analysis** | Active | ML models | Consumption-based | Customer feedback analysis, social media monitoring | Determines positive, negative, or neutral sentiment |
| **Language Detection** | Active | ML models | Consumption-based | Content filtering, routing | Identifies the language of input text |
| **Summarization** | Active | GPT-based models | Consumption-based | Document processing, news aggregation | Creates concise summaries of longer texts |
| **Entity Linking** | Active | ML models | Consumption-based | Content enrichment, knowledge graphs | Links entities to known references |
| **PII Detection** | Active | ML models | Consumption-based | Compliance, data protection | Identifies personally identifiable information |
| **Healthcare Text Analytics** | Active | Specialized ML models | Consumption-based | Medical record processing, clinical research | Domain-specific text analysis for healthcare |
| **LUIS** (Language Understanding) | Deprecated | Custom ML models, not LLMs | Legacy pricing | Legacy applications | Being deprecated in favor of CLU |
| **QnA Maker** | Deprecated | Information Retrieval + ML (not LLM-based) | Legacy pricing | Legacy applications | Being deprecated in favor of Custom Question Answering |

## [Azure AI Speech Services](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/)

Speech services for voice-enabled applications + accessibility features.

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **Speech to Text** | Active | Neural networks | Consumption-based | Transcription, voice commands | Real-time and batch transcription options |
| **Text to Speech** | Active | Neural networks | Consumption-based | Audiobooks, voice assistants | Supports [Speech Synthesis Markup Language (SSML)](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/speech-synthesis-markup) |
| **Speech Translation** | Active | Neural networks | Consumption-based | International communication, global content | Real-time translation between multiple languages |
| **Speaker Recognition** | Active | Neural networks | Consumption-based | Security, personalization | Voice authentication and identification |
| **Custom Speech** | Active | Neural networks | Consumption-based | Domain-specific applications | Customized speech recognition for specific vocabularies |
| **Custom Voice** | Active | Neural networks | Consumption-based | Brand-specific voice applications | Create custom voice fonts for your applications |
| **Speech Containers** | Active | Neural networks | Container pricing | Edge computing, offline scenarios | Deploy speech services in containers |

## [Azure AI Vision Services](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/)

Image analysis and image understanding for content moderation and other applications.

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **Image Analysis** | Active | CNN | Consumption-based | Content tagging, moderation | Extracts information from images |
| **Spatial Analysis** | Active | Specialized vision models | Consumption-based | Retail analytics, space optimization | Analyzes movement of people in physical spaces |
| **Face API** | Active (with restrictions) | Specialized ML models | Consumption-based | Limited identity verification use cases | Subject to Responsible AI restrictions |
| **Azure AI Video Indexer** | Active | ML models + speech models | Consumption-based | Video content analysis, searchable video | Extracts insights from video content |

## [Azure AI Document Intelligence](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/)

Document processing.

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **Prebuilt Models** | Active | ML models | Consumption-based | Invoice processing, receipt scanning | Domain-specific document understanding |
| **Custom Models** | Active | ML models | Consumption-based | Industry-specific documents | Train on your own document types |
| **Layout Analysis** | Active | ML models | Consumption-based | Document structure understanding | Extract text, tables, and structure |

## Other Azure AI Services

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **[Azure AI Translator](https://learn.microsoft.com/en-us/azure/ai-services/translator/)** | Active | Neural networks, newer versions use LLMs | Consumption-based | Content localization, international support | Text translation across 100+ languages |
| **Azure AI Anomaly Detector** | Active | Time-series ML models | Consumption-based | IoT monitoring, business metrics | Identifies unusual patterns in data |
| **Azure AI Content Safety** (formerly Content Moderator) | Active | ML models | Consumption-based | User-generated content screening | Detects offensive or inappropriate content |
| **Azure AI Immersive Reader** | Active | ML models | Consumption-based | Education, accessibility | Improves reading comprehension |
| **Azure AI Metrics Advisor** | Active | Time-series ML models | Consumption-based | Business intelligence, monitoring | Monitors metrics and diagnoses issues |
| **Azure AI Health Bot** | Active | Healthcare-specific ML models + LLM integration | Consumption-based | Healthcare scenarios, patient engagement | Healthcare-specific virtual assistant |
| **[Azure AI Search](https://learn.microsoft.com/en-us/azure/search/)** (formerly Cognitive Search) | Active | Information Retrieval + LLM integration | Consumption + reserved capacity | Enterprise search, knowledge mining | Can be integrated with LLMs for RAG patterns |

## Microsoft Copilot Family

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **Bing Chat / Microsoft Copilot** | Active | GPT-4 with customizations | Free (basic), Premium subscription | Consumer web search, creative assistance | Consumer-facing service using advanced LLMs |
| **Microsoft Copilot for Microsoft 365** | Active | GPT-4 with customizations | Subscription-based | Enterprise productivity | Integration with Office apps for content generation |
| **[Microsoft Copilot Studio](https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio)** (formerly Power Virtual Agents) | Active | GPT models + integration capabilities | Consumption + license | Enterprise chatbots, workflow automation | Low-code/no-code bot building platform |
| **GitHub Copilot** | Active | OpenAI Codex | Subscription-based | Code generation, developer productivity | AI pair programming assistant |

## Development and Deployment Platforms

| Service/Feature | Status | Underlying Model Technology | Pricing Tier | Use Cases | Notes |
|-----------------|--------|------------------------------|--------------|-----------|-------|
| **[Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/)** | Active | Various ML frameworks | Consumption + compute | ML model training, deployment, management | Complete ML lifecycle management |
| **Azure Cognitive Services for Containers** | Active | Varies by service | Container pricing | Edge deployment, offline scenarios, compliance | Deploy AI services in containers |
| **Azure AI Studio** | Active | Various, with focus on LLMs | Varies by usage | End-to-end AI development | Unified development environment for AI |

## Migration Paths

* LUIS → CLU (Conversational Language Understanding)
* QnA Maker → Custom Question Answering
* Form Recognizer → Azure AI Document Intelligence
* Computer Vision → Azure AI Vision
* Content Moderator → Azure AI Content Safety
* Multiple cognitive services → Azure AI Language or Azure OpenAI Service
