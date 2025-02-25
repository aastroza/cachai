![](/logo.PNG)

# cachai: the multimodal LLM about which there's nothing to say [WIP]

Welcome to the LLM that brings Chile's vibrant linguistic landscape to the forefront of technology. We're not just translating words; we're capturing the culture, humor, and distinctive Chilean spirit.

The future of AI is speaking Chilean, cachai?

## Motivation

Generative AI is revolutionizing global communication, with the potential to mediate all our interactions in the near future. However, [current models predominantly excel in standard English](https://blog.modernmt.com/making-generative-ai-multilingual-at-scale/), leaving less-represented languages and dialects at a significant disadvantage. This disparity is particularly evident in the case of **Chilean Spanish**, a dialect so unique that it challenges the very notion of what constitutes Spanish.

The Spanish spoken in Chile [stands out as one of the most linguistically disruptive variants worldwide](https://www.elmundo.es/cultura/2021/11/30/61a4a36321efa013518b4571.html). Its distinctiveness is unmistakable to both native speakers and language experts, although it is difficult to quantify. The Chilean dialect is characterized by:

- Rapid evolution of spoken and written language
- Frequent invention and adoption of new words
- Flexible and often unconventional pronunciation
- Constant modification and reinterpretation of linguistic rules

These factors combine to create a language environment where *"speaking Chilean"* diverges significantly from standard Spanish, posing unique challenges for LLMs.

The legendary filmmaker [Raúl Ruiz](https://www.ojoentinta.com/chile-segun-raul-ruiz/) eloquently captures the complexity of Chilean Spanish:

>What I like about Chile is that special way Chileans have of speaking. Chileans are sometimes capable of speaking without using either verb or subject, or they use verbs and the subject displaced, which makes them talk for hours and you don't know what about. Every Chilean speaks exclusively in quotation marks. It's someone who puts rhetoric before reality. Chile manufactures a very curious form of artificial language in which intonation is almost as important as the words that are uttered. More than the accent, it's the strange syntax. One starts a sentence and ends with ellipsis, starts another and another, and what happens is that people are speaking with three parallel discourses.

| ![tigres.jpg](images/tigres.jpg) | 
|:--:| 
| *"Tres tristes tigres", a masterpiece by Raúl Ruiz* |

Adapting models to this Chilean dialect requires more than simple translation. It demands a deep understanding of the cultural context, linguistic nuances, and the ever-evolving nature of the language. To achieve this, we need to curate a reliable written record that captures the essence of Chilean Spanish, reflecting its evolution while ensuring quality and representativeness.

Developing a model specialized in Chilean Spanish is not just about preserving linguistic diversity. It's about ensuring that as AI-mediated communication becomes ubiquitous, Chilean voices are not left behind. This project aims to bridge the gap between global advancements and local linguistic realities. The goal is to create a LLM that can authentically understand and interact with Chilean Spanish speakers, reflecting their unique expressions and cultural context.

## Exploration

### Traditional Voice AI

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

#### Listen Stage

- **Voice Activity Detection:** Identifies when speech is present in the audio input.
- **Automatic Speech Recognition:** Converts the detected speech into text.

#### Think Stage

- **Large Language Model:** Processes the text input and generates an appropriate response.

#### Speak Stage

- **Text-to-Speech:** Converts the generated text response into spoken audio output.

The entire process typically takes 3 to 5 seconds from input to output.

### Multimodal Voice AI

Example: [Moshi](/references/kuytai/moshi.md), developed by Kyutai, is a real-time voice-enabled AI that incorporates advanced multimodal processing, enabling more natural and spontaneous conversations with AI systems.

| ![moshi.jpg](images/moshi.jpg) | 
|:--:| 
| *Kyutai rolls out first voice-enabled AI chatbot ‘Moshi’. Image from [GBN](https://www.gccbusinessnews.com/kyutai-rolls-out-ai-chatbot-moshi/)* |

#### Key Features
- Real-time voice interaction: Achieves a latency of approximately 200-240ms.
- Multimodal processing: Simultaneously processes audio and text.
- Multi-stream audio: Capable of listening and speaking at the same time.
- Support for diverse emotions and speaking styles: Recognizes and expresses over 70 different emotions and styles.
- On-device capability: Functions effectively on standard laptops without requiring constant internet connectivity.

### Comparison with Traditional AI Voice Systems

#### Traditional Systems
- Pipeline approach: Sequential stages of Voice Activity Detection, ASR (Automatic Speech Recognition), LLM (Large Language Model), and TTS (Text-to-Speech).
- High latency: Typically ranges from 3-5 seconds.
- Loss of non-textual information: Struggles to capture tone, emotion, and context.
- Rigid turn-taking: Limited to back-and-forth interactions without overlapping dialogue.
- Limited contextual understanding: Fails to adapt dynamically to ongoing conversations.

#### Multimodal
- Unified model approach: Utilizes a single deep neural network.
- Drastically reduced latency: Achieves real-time interactions with 200-240ms delay.
- Preservation of non-textual information: Captures tone, emotion, and context effectively.
- Multi-stream processing: Allows for natural, overlapping dialogue.
- Multimodal understanding: Integrates audio and text for more comprehensive comprehension.
- Real-time adaptation: Adjusts dynamically to the user's tone and style.
- Advanced audio compression: Uses Mimi codec for efficient audio processing.
- Contextual consistency: Maintains coherent and contextually relevant interactions.

## Datasets

### Text

| Name | Author | Link |
| ---|---| ---|
| Chilean Humor | cachai | [Github](https://github.com/aastroza/chilean-humor) |
| Chilean Spanish Corpus | [Jorge Ortiz Fuentes](https://github.com/jorgeortizfuentes) | [Huggin Face](https://huggingface.co/datasets/jorgeortizfuentes/chilean-spanish-corpus) |
| Universal Chilean Spanish Corpus | [Jorge Ortiz Fuentes](https://github.com/jorgeortizfuentes) | [Huggin Face](https://huggingface.co/datasets/jorgeortizfuentes/universal_spanish_chilean_corpus) |

#### Chilean Humor

| ![avello.jpg](images/avello.jpg) | 
|:--:| 
| *Felipe Avello in the Viña del Mar Festival. SA Producciones, [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0), via Wikimedia Commons* |

An unexpected but rich source for this linguistic data lies in Chile's vibrant comedy scene. The [Viña del Mar Festival](https://en.wikipedia.org/wiki/Vi%C3%B1a_del_Mar_International_Song_Festival), showcases the country's top comedians and offers a treasure trove of uniquely Chilean expressions, wordplay, and cultural references. Held annually since 1960, the festival presents Chilean humor, known for its eccentricity – from talking puppets to trampoline-jumping comedians. This humor often features dialogues that are incomprehensible to non-Chilean Spanish speakers, making it an ideal dataset for training LLMs in the intricacies of Chilean Spanish.

### Text to Speech (TTS)

| Name | Author | Link |
| ---|---| ---|
| Google Chilean Spanish | [Yoach Lacombe](https://github.com/ylacombe) | [Huggin Face](https://huggingface.co/datasets/ylacombe/google-chilean-spanish) |
| Crowdsourced high-quality Chilean Spanish speech dataset | Guevera-Rokuz et al | [Open SLR](https://www.openslr.org/71/) |

### Automatic Speech Recognition (ASR)

| Name | Author | Link |
| ---|---| ---|
|  Common Voice Corpus 13.0 | [Mozilla Common Voice](https://commonvoice.mozilla.org/en/datasets) | [Huggin Face](https://huggingface.co/datasets/mozilla-foundation/common_voice_13_0) |
|  Common Voice Corpus 13.0 - Chilean Accent | [Mozilla Common Voice](https://commonvoice.mozilla.org/en/datasets) | [Huggin Face](https://huggingface.co/datasets/mozilla-foundation/common_voice_13_0/viewer/es/train?f[accent][value]=%27Chileno:%20Chile,%20Cuyo%27) |

## Existing Models

| Name | Type | Author | Link |
| ---|---|---| ---|
| BETO | Text | [dccuchile](https://github.com/dccuchile/beto) | [Huggin Face](https://huggingface.co/dccuchile/bert-base-spanish-wwm-uncased) |
| Tulio | Text | [Jorge Ortiz Fuentes](https://github.com/jorgeortizfuentes) | [Huggin Face](https://huggingface.co/dccuchile/tulio-chilean-spanish-bert) |
| Patana | Text | [Jorge Ortiz Fuentes](https://github.com/jorgeortizfuentes) | [Huggin Face](https://huggingface.co/dccuchile/patana-chilean-spanish-bert) |

## Fine-tuning

### TTS

- [Finetune VITS and MMS using HuggingFace's tools](https://github.com/ylacombe/finetune-hf-vits)
- [Parler-TTS](https://github.com/huggingface/parler-tts)
- [MeloTTS Training](https://github.com/myshell-ai/MeloTTS/blob/main/docs/training.md)
- [MetaVoice-1B Finetuning](https://github.com/metavoiceio/metavoice-src?tab=readme-ov-file#finetuning)
- [Coqui XTTS training](https://docs.coqui.ai/en/latest/models/xtts.html#training)

### ASR

- [Choosing a dataset](https://huggingface.co/learn/audio-course/en/chapter5/choosing_dataset)
- [Fine-tuning the ASR model](https://huggingface.co/learn/audio-course/en/chapter5/fine-tuning)

## Tools

- [DataSpeech](https://github.com/huggingface/dataspeech)

