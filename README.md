# cachai: el LLM multimodal del que no hay nada que decir

## Traditional Voice AI

The process is divided into three main stages: Listen, Think, and Speak. Each stage involves specific AI technologies to process and generate speech.

```mermaid
graph LR
    subgraph Listen
    A[Voice Activity Detection] --> B[Automatic Speech Recognition]
    end
    subgraph Think
    C[Large Language Model]
    end
    subgraph Speak
    D[Text-to-Speech]
    end
    
    B --> C
    C --> D
    
    style Listen fill:#f0fff0,stroke:#333,stroke-width:2px
    style Think fill:#f0f8ff,stroke:#333,stroke-width:2px
    style Speak fill:#fff0f5,stroke:#333,stroke-width:2px
```

## Listen Stage

- **Voice Activity Detection:** Identifies when speech is present in the audio input.
- **Automatic Speech Recognition:** Converts the detected speech into text.

## Think Stage

- **Large Language Model:** Processes the text input and generates an appropriate response.

## Speak Stage

- **Text-to-Speech:** Converts the generated text response into spoken audio output.

The entire process typically takes 3 to 5 seconds from input to output.