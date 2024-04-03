# Task Participant Metadata

### Team Name: 

ANU

### Participants:

1. Sandaru Seneviratne Australian National University
2. Hanna Suominen Australian National University


### Language Survey

Please indicate which of the following languages you are able to provide human evaluation for. You should be proficient in a language to provide judgments in it.

 - [ ] Catalan
 - [x] English
 - [ ] Filipino
 - [ ] French
 - [ ] German
 - [ ] Italian
 - [ ] Japanese
 - [ ] Portuguese
 - [x] Sinhala
 - [ ] Spanish

### Files submitted (mark with an X):

| FILE        | LCP | LS |
| ------------|:---:|---:|
| All         |     |    |
| Catalan     |     |    |
| English     |  x  |  x |
| Filipino    |     |    |
| French      |     |    |
| German      |     |    |
| Italian     |     |    |
| Japanese    |     |    |
| Portuguese  |     |    |
| Sinhala     |  x  |  x |
| Spanish     |     |    |

### System Description
LCP:
For LCP, we relied on the gpt3.5-turrbo model to generate lexical complexity of the given words based on zero-shot, one-shot, and few-shot prompting. This was done for both English and Sinhla tasks. The three files correspond to the three types of prompting.

LS:
Similar to our approach in LCP, for LS, we used the GPT-3.5-turbo model to generate alternative words that are similar or simpler using prompt engineering techniques. These techniques include zero-shot, one-shot, and few-shot methods. 
After obtaining alternative words through prompt engineering, each prediction is scored based on the order in which it was suggested. Subsequently, all predicted words are combined. In cases where the same word is suggested across all three prompt engineering methods, its score is increased. Furthermore, duplicates are removed to get the final set of predictions. The results are in '_1' file. '_2' and '_3' files include the predictions based on one-shot and few-shot.
For Sinhala, only one result file is provided ('_1'') which contains the combined predictions.  
### Agreement

- [x] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [x] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [x] I agree to participate in the human evaluation round and provide up to 300 judgments.

