# Task Participant Metadata

### Team Name: 

Archaeology

### Participants:

1. Petru Theodor Cristea, University of Bucharest
2. Sergiu Nisioi, University of Bucharest

### Language Survey

Please indicate which of the following languages you are able to provide human evaluation for. You should be proficient in a language to provide judgments in it.

 - [] Catalan
 - [x] English
 - [] Filipino
 - [] French
 - [] German
 - [] Italian
 - [] Japanese
 - [] Portuguese
 - [] Sinhala
 - [] Spanish

### Files submitted (mark with an X):

| FILE        | LCP  | LS  |
| ------------|:----:|----:|
| All         |      |     |
| Catalan     |   x   |  x   |
| English     |   x   |  x   |
| Filipino    |   x   |  x   |
| French      |   x   |  x   |
| German      |   x   |  x   |
| Italian     |   x   |  x   |
| Japanese    |   x   |  x   |
| Portuguese  |   x   |  x   |
| Sinhala     |   x   |  x   |
| Spanish     |   x   |  x   |

## System Description

### LCP system
The LCP system is trained on all the trial data and the data from [LCP2021 Shared Task](https://sites.google.com/view/lcpsharedtask2021). The model is an [xgb.Regressor](https://xgboost.readthedocs.io/en/stable/parameter.html) and the features values are defined below. The features are dependent on English language resources (Dale-Chall's list, MRC psycholinguistic feature, wordnet, etc) and for non-English languages the model is trained mostly on features derived from spaCy and the shallow structure of the word.


#### 1. Shallow word structure features:

- `zipf_frequency` from wordfreq library (except `sin` language)
- character length of word
- is title (irrelevant for non-Latin glyphs)
- number of vowels (irrelevant for non-Latin glyphs)
- number of syllables from pyphen library (irrelevant for non-Latin glyphs)


#### 2. Syntactic features (spaCy medium-sized models, except for `sin` and `fi`)

- is entity
- is sentence start
- is sentence end
- number of immediate children in syntactic dependency parse

#### 3. Wordnet feature (English only):

- synsets
- hypernyms
- hyponyms

#### 4. [MRC Psycholinguistic Database](https://websites.psychology.uwa.edu.au/school/MRCDatabase/uwa_mrc.htm) (English only)

- aoa - Age of acquisition rating (100-700)
- conc - Concreteness rating (100-700)
- fam - Familiarity rating (100-700)
- imag - Imagability rating (100-700)
- nlet - Number of letters
- meanc - Meaningfulness; Colorado Norms (100-700)
- meanp - Meaningfulness; Paivio Norms (100-700)
- brown_freq - Brown verbal frequency
- kf_ncats - Kucera-Francis number of categories
- kf_nsamp - Kucera-Francis number of samples
- kf_freq - Kucera-Francis written frequency (>0)
- tl_freq - Thorndike-Lorge written frequency (0-3000000)

#### 5. External Dataset (English only)
- is word in the Dale-Chall list
- frequency in [the dataset of non-native speakers from the European Parliament](https://aclanthology.org/L16-1664/)

### LS System
For lexical simplification we use `openhermes-2.5-mistral-7b.Q4_K_M.gguf` a locally run (on CPU) quantized LLM with llama-cpp-python and langchain and we prompt it to generate altenative candidates for the target word.
We test two pipelines:

#### 1. Machine Translation (MT) pipeline
We use propietary MT systems (Google Translate for `fi`, `sin`, `ca`, and DeepL for all the others) to translate all the data into English. We then apply the LCP and LS systems on the English data and back-translate the simplified data to the original language. It is often the case that single words are translated as expressions. Candidates are translated out of context which makes them innapropriate for search-and-replace substitutions.
The submissions with this approache are suffixed with `*_1.tsv`.

#### 2. Direct pipeline
We apply the LCP and LS systems directly on the original data, thus we prompt the model to generate alternative candidates for the target word in the original language. The submissions with this approache are suffixed with `*_2.tsv`.
The model is not capable of handling multilingual data and often hallucinates.


### Agreement

- [x] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [x] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [x] I agree to participate in the human evaluation round and provide up to 300 judgments.

