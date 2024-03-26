# Task Participant Metadata

### Team Name: 

RETUYT-INCO

### Participants:

1. Leandro Alfonso, Universidad de la República, Uruguay
2. Luis Chiruzzo, Universidad de la República, Uruguay
3. Facundo Fleitas, Universidad de la República, Uruguay
4. Federico Gil, Universidad de la República, Uruguay
5. Santiago Góngora, Universidad de la República, Uruguay
6. Andrés Lucas, Universidad de la República, Uruguay
7. Aiala Rosá, Universidad de la República, Uruguay
8. Ignacio Sastre, Universidad de la República, Uruguay
9. Tomás Sportuno, Universidad de la República, Uruguay

### Language Survey

Please indicate which of the following languages you are able to provide human evaluation for. You should be proficient in a language to provide judgments in it.

 - [ ] Catalan
 - [X] English
 - [ ] Filipino
 - [ ] French
 - [ ] German
 - [ ] Italian
 - [ ] Japanese
 - [ ] Portuguese
 - [ ] Sinhala
 - [X] Spanish

### Files submitted (mark with an X):

| FILE        | LCP  | LS  |
| ------------|:----:|----:|
| All         |   X  |  X  |
| Catalan     |   X  |     |
| English     |   X  |  X  |
| Filipino    |      |     |
| French      |      |     |
| German      |      |     |
| Italian     |      |     |
| Japanese    |      |     |
| Portuguese  |   X  |  X  |
| Sinhala     |      |     |
| Spanish     |   X  |  X  |

### System Description

We tried several methods ranging from simple embeddings and frequency baselines, feed forward with BERT features, to more complex fine-tuning of LLMs with synthetic examples.
The submitted results include the following methods:
* Embeddings and frequency baselines for Spanish, English and Portuguese (LS)
* Feed forward with BERT-based embeddings for Spanish and English (LCP)
* Fine-tuning Mistral-7B for English (LCP) and with synthetic data and self-consistency for English, Spanish, Catalan and Portuguese (LCP and LS)
* Prompting using models available in the Groq API for Spanish (LS)

### Agreement

- [X] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [X] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [X] I agree to participate in the human evaluation round and provide up to 300 judgments.
