Benchmark Performance

For question answering through span prediction, we used a BERT model on which we added HTML tags as tokens in the tokenizer. 
Dues to the fact that many articles were large and surpassed the context limit, we cropped them in sequences like: [CLS] Question [SEP] Context.
We trained the model using one-hot encoding of the span start and end positions.
We based our predictions on a number of common sense mechanisms that analysed the probability distribution predicted by the model (for instance, the question in a crop cannot be part of an answer).
We used a large uncased configuration of BERT that outputs an embedding of 1024.


We implemented the notebook that trains without any pretrained data on kaggle, however, due to time constraints, the script was not able to run fully:

Kaggle trainig script without pretrained data: https://www.kaggle.com/code/smocgeorge/trainnotebook?scriptVersionId=159323956
Base training script on google colab: https://colab.research.google.com/drive/1DmIMb5vIHpQJykyfIJCEttlbcknc0cI9#scrollTo=dVwgtkdyixay