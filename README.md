# Automated_image_captioning

I have made a basic Image Captioning Pipeline using deep learning Methods.

Approach :
1) **Data Collection** : I downloaded dataset from Kaggle [Link](https://www.kaggle.com/adityajn105/flickr8k)
2) **Data Cleaning** : I performed some basic cleaning like lower-casing all the words (otherwise“hello” and “Hello” will be regarded as two separate words), removing special tokens (like ‘%’, ‘$’, ‘#’, etc.), eliminating words which contain numbers (like ‘hey199’, etc.)
3) **Vocabulary creation** : Created a set of all unique words which occurs at least 10 times
4) **Load Training Set Captions** : added token 'startseq' and 'endseq' in each captions
5) **Feature Extraction using Transfer Learning** : Created a feature vector for each image using ResNet50
6) **Data Preprocessing** : Created two dictionary viz. word_to_idx and idx_to_word which helps to maps word in their index and vice-versa.
7) **Data Preparation using Generator Function** : This methods is used to reduce space taken by our model on main memory. 
8) **Word Embeddings** : Used Glove Vectors(glove 6B50d.txt) to create embedding_matrix. Embeddings were requirements for any RNN based architecture.
9) **Model Architecture** : 
![1_rfYN2EELhLvp2Van3Jo-Yw](https://user-images.githubusercontent.com/84574907/130343351-7ec1da2f-1c20-414b-a836-bf4657162df3.jpeg)
10) **Training** : Trained model for 20 epochs and batchsize = 3
11) **Prediction on random images**
