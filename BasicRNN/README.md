# Comparison btw basic RNN and LSTM

> Basic RNN
* Small RNN is created as below. I add embedding layer then batch normalization before rnn layer. RNN layer is connected to output layer as well.  The structure is very basic.
  
![image](https://github.com/user-attachments/assets/0befce03-af4b-4abf-a2ec-4f7bd58e0035)

* According to training results, even though accuracy in train oscillates at same line and val_acc seems saturated a little bit, i would keep the training going on. Because the val loss keeps decending as you can see the graph. But you can see that there is a big unstablity in training and validating on the data.
  
![image](https://github.com/user-attachments/assets/a2452085-b7d6-4c69-a916-811955094afa)

> LSTM Model:
* I take the benefits from gloVE in embedding layer. Instead of putting the embedding array as random values like basic rnn, i could take the meaningful values for this array through glove that already trained and filled up. I am matching my vocab with glove. Now, embedding array is meaningful right now. Vocabulary sequence is more meaningful now from the start of training.
  
![image](https://github.com/user-attachments/assets/f65b8e9a-6b7f-48d9-94fd-1d8602927f0e)

* The result is more better than the rnn, right :)
  
![image](https://github.com/user-attachments/assets/ec10315b-3ba8-4b7a-b03b-c5ce7c0e45dc)

> Bidirectional LSTM Model:
* I see that overfitting was started. It might be because of the data size. In order to get fast result, i had cropped the data. 
![image](https://github.com/user-attachments/assets/1d2d6e6a-b649-445e-93ae-bf58d5aa6853)

# Comparison btw basic LSTM and Bidrectional LSTM:
The main difference is that lstm goes forward only. It focuses on what happened in the past. That's why hidden layer is moving towards the right. But Bidirectional version double the hidden layers seen below. Forward and backward hidden layers goes through.

![image](https://github.com/user-attachments/assets/c4fcf757-5fee-4d51-bba5-e401b6d71e06)

![image](https://github.com/user-attachments/assets/b8974671-5a4a-49d4-a774-d60b66d7a521)

The other difference is the time lapsed. Bidirectional takes more time. Lets see:
Bidirectional LSTM -> the execution took 3731.799 sec vs LSTM -> the execution took 1497.624 sec

**In these results, LSTM has better score and performance.**

# Let see what if my data is bigger/complexer:
somehow lstm model went exploding gradient. I will investigate deeply at different folder. go to -->https://github.com/cagricivici/NLP_Examples/tree/main/Basic%20LSTM%20with%20Glove




