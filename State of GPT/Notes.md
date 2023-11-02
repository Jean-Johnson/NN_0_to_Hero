# State of GPT
_Talk by andrewj at Microsoft Build 2023 event_

## GPT assistant training pipline
- ### Pretraining
  - Trained on raw internet data without any lables etc
  - Next token prediction training is done by feeding data into transformer arch (Unsupervised learning)
  - need 1000s of GPU and months to train
  - Can use promt engineer on base model to complete a task
  - Trick base model using Few-shot promt
  - GPT, LLaMA, PaLM
- ### Supervised fine tuning (SFT)
  - use high quality dataset -> promt and response dataset
  - next token prediction
  - 1-100 GPUs and takes weeks
  - Vulcan - 13B
- ### Reward Modeling
  - use people to rank the document
  - consider for one prompt 3 responses are given and the contracter annotate it with reward
  - Train the model to predict reward
  - 1-100 GPUs and take days of training
  - These RM model can only be used to predict rewards.
- ### Reinforcement Learning
  - use SFT model to create the outputs for a prompt
  - Then use reward model to predict the reward
  - The ouput with best reward is used in the training of the model, means the propability of the ouput  is increased

- ## seperate Notes
  - Base model have high entropy because of that it can be used to create diverse outputs