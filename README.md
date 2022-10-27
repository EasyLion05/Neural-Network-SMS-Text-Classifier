# Neural-Network-SMS-Text-Classifier
Machine Learning

Take note that this problem's training duration is agonizingly slow!

You can use the following helpful lesson on RNN and TextVectorization to resolve this issue. But be careful to adhere to it strictly. By skipping these 2 lines, thinking that it is merely an optimization, I waste a lot of time. It isn't. The data sets are really reshaped by it. The model can't fit without it.

( train_dataset = train_dataset.shuffle(BUFFER_SIZE).batch(BATCH_SIZE).prefetch(tf.data.AUTOTUNE)
test_dataset = test_dataset.batch(BATCH_SIZE).prefetch(tf.data.AUTOTUNE) )
