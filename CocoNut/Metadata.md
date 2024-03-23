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

LAE-LS introduces a novel method for lexical simplification (LS) that is trained without the use
of parallel corpora or any external linguistic resources.
This method comprises two key modules: Adversarial Editing and Difficulty-aware Filling.

Concretely, we employ an Adversarial Editing module to train an Edit Predictor for predicting lexical edits, which can
be used to identify complex words within sentences.
To balance the preservation of semantics and the level of simplification, we introduce a confusion loss and an
invariance loss to confuse the discriminator and preserve the semantics of the original sentence, respectively.
Particularly, an LLM-enhanced loss is tailored to extract supervision signals from Large Language Models.
With this loss, high-quality knowledge from LLMs can be distilled into our Edit Predictor.
Eventually, the Difficulty-aware Filling module is crafted to fill in the masked positions with alternative simple
words.

- For the LCP method, we utilize the probability of a word being masked by the Edit Predictor as the complexity value of
the word in context.

- For the LS method, we mask difficult words and utilize the Difficulty-aware Filling module to predict substitute words
for these positions. The top 10 predicted words are selected as the final list of substitute words.

[1] Tan K, Luo K, Lan Y, et al. An LLM-Enhanced Adversarial Editing System for Lexical Simplification[J]. arXiv preprint
arXiv:2402.14704, 2024.

### Agreement

- [X] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [X] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [X] I agree to participate in the human evaluation round and provide up to 300 judgments.

