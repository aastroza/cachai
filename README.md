# cachai: el LLM multimodal del que no hay nada que decir

## IA de Voz Tradicional

El proceso se divide en tres etapas principales: Escuchar, Pensar y Hablar. Cada etapa involucra tecnologías específicas de IA para procesar y generar voz.

```mermaid
graph LR
    subgraph Escuchar
    A[Detección de Actividad de Voz] --> B[Reconocimiento Automático del Habla]
    end
    subgraph Pensar
    C[LLM]
    end
    subgraph Hablar
    D[Texto a Voz]
    end
    
    B --> C
    C --> D
    
    style Escuchar fill:#f0fff0,stroke:#333,stroke-width:2px
    style Pensar fill:#f0f8ff,stroke:#333,stroke-width:2px
    style Hablar fill:#fff0f5,stroke:#333,stroke-width:2px
```

### Etapa de Escuchar

- **Detección de Actividad de Voz:** Identifica cuándo hay habla presente en la entrada de audio.
- **Reconocimiento Automático del Habla:** Convierte el habla detectada en texto.

### Etapa de Pensar

- **LLM:** Procesa la entrada de texto y genera una respuesta apropiada.

### Etapa de Hablar

- **Texto a Voz:** Convierte la respuesta de texto generada en salida de audio hablada.

Todo el proceso típicamente toma de 3 a 5 segundos desde la entrada hasta la salida.