# Task Participant Metadata

### Team Name: 

SCaLAR

### Participants:

1. Anand Kumar, National Institute of Technology Karnataka,
2. Abhin B, National Institute of Technology Karnataka,
3. Renukasakshi V Patil,National Institute of Technology Karnataka,
4. Sidhaarth Sredharan Murali, National Institute of Technology Karnataka

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
 - [ ] Spanish

### Files submitted (mark with an X):

| FILE        | LCP  | LS  |
| ------------|:----:|----:|
| All         |   X  |    |
| Catalan     |      |     |
| English     |      |  X   |
| Filipino    |      |     |
| French      |      |     |
| German      |      |     |
| Italian     |      |     |
| Japanese    |      |     |
| Portuguese  |      |     |
| Sinhala     |      |     |
| Spanish     |      |     |

### System Description

For LS we used Mistral-7B with few shot learning and applied cleaning with more post-processing because of repition of the prompt itself and got similarity scores using Google word2vec and chose the top 10 similar words for each complex word if present or all the words predicted to be simliar if present in number less than 10.

For LCP, we used 
- Roberta Regressor with Multisample Dropout and MLPs: Employs Roberta regressor with multisample dropout and ReLU activations, followed by MLPs with varying depths (1, 3, and 5 layers) and ReLU activations, each with distinct parameters.
- MPNet Hidden State to Image Regression with EfficientNet: Transforms MPNet hidden states into image format and employs EfficientNet for image regression, bridging text data to convolutional neural networks.
- XGBoost Regressor with TF-IDF and Zipf Frequency Features: Utilizes XGBoost regressor with features derived from TF-IDF and Zipf frequency, incorporating text features effectively.
- Final Model with Weighted Sum: Combines outputs of stages 2 and 3 using a weighted sum as complexity scores, optimizing regression performance through an ensemble approach.

### Agreement

- [X] I agree for my submission to be evaluated as part of the MLSP Shared Task
- [X] I agree for my system outputs to be made public and the ranking of my system to be made public for future research
- [X] I agree to participate in the human evaluation round and provide up to 300 judgments.
