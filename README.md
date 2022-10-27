# Neural-Network-SMS-Text-Classifier
Machine Learning

Take note that this problem's training duration is agonizingly slow!

You can use the following helpful lesson on RNN and TextVectorization to resolve this issue. But be careful to adhere to it strictly. By skipping these 2 lines, thinking that it is merely an optimization, I waste a lot of time. It isn't. The data sets are really reshaped by it. The model can't fit without it.

( train_dataset = train_dataset.shuffle(BUFFER_SIZE).batch(BATCH_SIZE).prefetch(tf.data.AUTOTUNE)
test_dataset = test_dataset.batch(BATCH_SIZE).prefetch(tf.data.AUTOTUNE) )

# Problem description
Copied and modified from this Google Colab

In this challenge, you need to create a machine learning model that will classify SMS messages as either "ham" or "spam". A "ham" message is a normal message sent by a friend. A "spam" message is an advertisement, or a message sent by a company.

You should create a function called predict_message that takes a message string as an argument and returns a list. The first element in the list should be a number between zero and one that indicates the likeliness of "ham" (0) or " spam" (1). The second element in the list should be the word "ham" or "spam", depending on which is most likely.

For this challenge, you will use the SMS Spam Collection dataset. The dataset has already been grouped into train data and test data.

The first two cells import the libraries and data. The final cell tests your model and function. Add your code in between these cells.
