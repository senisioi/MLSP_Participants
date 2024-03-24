# Task Participant Metadata

### Team Name:

CocoNut

### Participants:

1. Keren Tan, School of Data Science \& Engineering, East China Normal University, Shanghai, China
2. Yunshi Lan, School of Data Science \& Engineering, East China Normal University, Shanghai, China

### Language Survey

Please indicate which of the following languages you are able to provide human evaluation for. You should be proficient
in a language to provide judgments in it.

- [ ] Catalan
- [X] English
- [ ] Filipino
- [ ] French
- [ ] German
- [ ] Italian
- [ ] Japanese
- [ ] Portuguese
- [ ] Sinhala
- [ ] Spanish

### Files submitted (mark with an X):

| FILE       | LCP | LS |
|------------|:---:|---:|
| All        |     |    |
| Catalan    |     |    |
| English    |  X  |  X |
| Filipino   |     |    |
| French     |     |    |
| German     |     |    |
| Italian    |     |    |
| Japanese   |     |    |
| Portuguese |     |    |
| Sinhala    |     |    |
| Spanish    |     |    |

### System Description

We present our approach for the English (LCP & LS) task, utilizing our **LAE-LS** model [1].

Technical details of our methodology are outlined below:

**LAE-LS** introduces a novel method for LS that is trained without the use of parallel corpora or
any external linguistic resources, comprising two key modules: Adversarial Editing and Difficulty-aware Filling.
Concretely, we employ an Adversarial Editing System with guidance from a confusion loss and an invariance loss to
predict lexical edits in the original sentences.
Particularly, an LLM-enhanced loss is tailored to distill high-quality knowledge from LLMs into our Edit Predictor.
From that, complex words within sentences are masked and a Difficulty-aware Filling module is crafted to replace masked
positions with simpler words.

- For LCP, we utilize the probability of a word being masked by the Edit Predictor as the complexity value of
  the word in context.

- For LS, we mask complex words and utilize the Difficulty-aware Filling module to predict substitute words,
  selecting the top 10 predicted words as the final substitutes list.

[1] Tan K, Luo K, Lan Y, et al. An LLM-Enhanced Adversarial Editing System for Lexical Simplification[J]. arXiv preprint
arXiv:2402.14704, 2024.

### Agreement

- [X] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [X] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [X] I agree to participate in the human evaluation round and provide up to 300 judgments.

