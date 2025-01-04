# Prompt + Response <= Context Window

LLMs have assorted limitations on how much data they can process in one shot. One such limitation is known as the _context window_
which is the overall number of tokens available for a single inference request.

The number of tokens consumed by the prompt is implied - you don't specify it separately, 
but rather you send in the prompt and that prompt is innately made up of a certain number of tokens.

You get to specify a cap on the number of tokens consumed in the response - this is MaxTokens, a value typically
transmitted alongside the prompt, temperature, and other response-impacting values.
The response is not going to be exactly this number of tokens, but will not exceed it.

The context window is also measured in tokens. The number of tokens used by the prompt PLUS 
the number of tokens used by the response CANNOT EXCEED
the number of tokens allowed in the context window.

## Consequences

Chat history: unmanaged accumulated chat history can consume a lot of your context window, eventually overflowing it. There are patterns for compressing this.

Cost: if you are paying by the token, token use and spend are correlated.

Latency: does an LLM take longer to process a larger context window?

Accuracy: does a larger context window equally account for all of its content?

## Examples: Context Window = 32,000 tokens

```mermaid
flowchart TD
    Title[/"**Context Window: 32,000 tokens**"/]
    Title --> ValidCase
    Title --> ErrorCase
    
    subgraph ValidCase["**Success Example**"]
        direction TB
        Input1["Input Prompt:<br>2,000 tokens"]
        Max1["MaxTokens:<br>4,000 tokens"]
        Total1["Total Attempted Usage:<br>6,000 tokens<br>✅ 26,000 under limit"]
        
        Input1 & Max1 --> Total1
        
        style Input1 fill:#e6ffe6,stroke:#4CAF50
        style Max1 fill:#e6ffe6,stroke:#4CAF50
        style Total1 fill:#E8F5E9,stroke:#4CAF50
    end
    
    subgraph ErrorCase["**Failure Example**"]
        direction TB
        Input2["Input Prompt:<br>2,000 tokens"]
        Max2["MaxTokens:<br>31,000 tokens"]
        Total2["Total Attempted Usage:<br>33,000 tokens<br>❌ 1,000 over limit"]
        
        Input2 & Max2 --> Total2
        
        style Input2 fill:#e6ffe6,stroke:#4CAF50
        style Max2 fill:#e6ffe6,stroke:#4CAF50
        style Total2 fill:#FFEBEE,stroke:#FF5252
    end

    style Title fill:#333,stroke:none,color:#fff
    style ValidCase fill:#fff,stroke:#ddd
    style ErrorCase fill:#fff,stroke:#ddd
```
