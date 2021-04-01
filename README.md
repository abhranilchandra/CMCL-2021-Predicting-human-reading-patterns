# ChiSquareX at CMCL 2021 Shared task: Leveraging recent advances in Pre-Trained Language Models for Eye-Tracking Prediction

This is our attempt of the shared task on **Eye-Tracking Data Prediction: Predicting human reading patterns** at the [CMCL 2021 workshop](https://cmclorg.github.io/), part of the [NAACL 2021](https://2021.naacl.org/) conference.  

## Authors: Varun Madhavan, Aditya Girish Pawate, Abhranil Chandra, Shraman Pal

The workshop provides a venue for work in computational psycholinguistics, including computational and mathematical modeling of linguistic representations, development and processing. CMCL promotes the synergy between the field of Cognitive Modelling and Natural Language Processing applying methods from computational linguistics to problems in the cognitive modeling of any and all natural language abilities by the use of Cognitively inspired human-derived behavioral data, which reflect the semantic representations in the human brain to augment the neural nets to solve a range of tasks spanning syntax and semantics with the aim of teaching machines about language processing mechanisms.

Official information, data, and task details can be found [here](https://competitions.codalab.org/competitions/28176).

## Sections
1. [System description paper](#system-description-paper)
2. [Results](#results)
3. [Acknowledgements](#acknowledgements)

## System Description Paper  
Our paper can be found [here](https://drive.google.com/file/d/18HnVPbO0_EiQMvCRYgxGDPeBxURwWuPf/view?usp=sharing).  

## Results  
Results of different models on the dataset can be found here:
The results have been in terms of the **R^2** (coefficient of determination) scores.  

### Compiled results of all the top performing models:  

|  Model         |Feature Norm| Extra Features|   nFix  |   FFD   |   GPT   |   TRT   | fixProp |
|----------------|------------|---------------|---------|---------|---------|---------|---------|
|    Roberta     |  Std Scl   |      STT      | 0.8842  | 0.9246  | 0.7343  | 0.8823  | 0.9509  | 
|    Roberta     |  Min Max   |      All      | 0.8835  | 0.9132  | 0.7383  | 0.8542  | 0.9461  |
|    Roberta     |  Min Max   |      STT      | 0.8417  | 0.9090  | 0.6456  | 0.8152  | 0.9492  | 
|      Bert      |  Min Max   |      All      | 0.7433  | 0.8528  | 0.4574  | 0.6925  | 0.9173  | 
|BiLSTM Minibatch|  Min Max   |   All+GloVe   | 0.6595  | 0.7275  | 0.6281  | 0.5988  | 0.7583  |
|BiLSTM Minibatch|  Min Max   |All+Numberbatch| 0.6379  | 0.7203  | 0.5992  | 0.5388  | 0.7592  |
| Roberta Token  |  Std Scl   |      All      | 0.7038  | 0.6512  | 0.4697  | 0.6877  | 0.7146  | 
|   Bert Token   |  Std Scl   |      All      | 0.7231  | 0.7107  | 0.3440  | 0.6376  | 0.7635  | 
|      Bert      |  Std Scl   |      All      | 0.6497  | 0.6456  | 0.5409  | 0.6088  | 0.7171  | 
|BiLSTM Minibatch|  Std Scl   |   All+GloVe   | 0.6850  | 0.5976  | 0.5267  | 0.5940  | 0.7158  | 

Our Final Leaderboard Test MAE(Mean Absolute Error): **4.6764**  

## Acknowledgements  
A huge thanks to the organizers Emmanuele Chersoni, Nora Hollenstein, Cassandra Jacobs, Yohei Oseki, Laurent Prévot, and Enrico Santus for creating this wonderful task.  

Additionally, we would like to extend a big thanks to the makers and maintainers of the excellent [HuggingFace](https://github.com/huggingface/transformers) repository, without which most of our research would have been impossible.
