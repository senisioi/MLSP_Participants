# Task Participant Metadata

### Team Name: 

TMU-HIT

### Participants:

1. Taisei Enomoto, Tokyo Metropolitan University
2. Hwichan Kim, Tokyo Metropolitan University
3. Tosho Hirasawa, Tokyo Metropolitan University
4. Yoshinari Nagai, Tokyo Metropolitan University
5. Ayako Sato, Tokyo Metropolitan University
6. Kyotaro Nakajima, Tokyo Metropolitan University
7. Mamoru Komachi, Hitotsubashi University

### Language Survey

Please indicate which of the following languages you are able to provide human evaluation for. You should be proficient in a language to provide judgments in it.

 - [ ] Catalan
 - [ ] English
 - [ ] Filipino
 - [ ] French
 - [ ] German
 - [ ] Italian
 - [X] Japanese
 - [ ] Portuguese
 - [ ] Sinhala
 - [ ] Spanish

### Files submitted (mark with an X):

| FILE        | LCP  | LS  |
| ------------|:----:|----:|
| All         |   X  |  X  |
| Catalan     |      |     |
| English     |   X  |  X  |
| Filipino    |      |     |
| French      |      |     |
| German      |      |     |
| Italian     |      |     |
| Japanese    |   X  |  X  |
| Portuguese  |      |     |
| Sinhala     |      |     |
| Spanish     |      |     |

### System Description
We basically used GPT-4 based approach in the both tasks.
The details are follows:

#### LS
In System 1, we used GPT-4 to generate 10 alternative words for the target word in zero-shot.
In the case of Japanese, rather than solely generating alternative words, we directed GPT-4 to generate sentences wherein the target words were substituted with each alternative word. This approach was necessary to ensure that the “Katsuyou” (inflection) appropriately suited the context in Japanese.
In System 2, we directed GPT-4 to re-rank the top three alternatives in System 1 based on the “Ease of word” and the “Semantic similarity of word to the target word.
In System 3, we re-ranked the top three alternatives in System 1 using [XGLM] (https://huggingface.co/facebook/xglm-7.5B), which we fine-tuned using the Trial data.

#### LCP
For LCP, we assessed the complexities of target words according to [G-EVAL](https://arxiv.org/abs/2303.16634).
First, we employed GPT-4 to generate an instruction in English utilizing AutoCoT, subsequently assigning complexity scores to target words across all languages based on the English instruction.
Additionally, we conducted an analysis of the efficacy of the initial instruction for each language, refining the instruction to enhance the accuracy of complexity scoring.
This refinement included incorporating instructions specifying the language of the target word or emphasizing the scoring of complexities by individuals lacking specialized knowledge or expertise in a particular domain, into the initial instruction.
We evaluated each refined instruction using trial data and selected the instruction that achieved the lowest MSE score for each language.
The results, namely *_1.tsv and *_2.tsv, correspond to the zero- and three-shot settings, respectively.

### Agreement

- [X] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [X] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [X] I agree to participate in the human evaluation round and provide up to 300 judgments.

