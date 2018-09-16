Training a convolutional neural network for handwritten digits on the famous MNIST dataset.


## Dependencies
This code is written in python. To use it you will need:
* python  2.7
* Keras  2.2.2
* numpy  1.15.1
* Tensorflow  1.10.0


## Loading Data

    from mnist_loader import load_dataset
    train_x, train_y, test_x, test_y = load_dataset()


## Training
    cnn = CNN()
    cnn.train(train_x, train_y, epochs=10, batch_size=32)

## Evaluation
    score = cnn.evaluate(test_x, test_y)
    print('Accuracy is : ', score)
    
## Classify a new instance
    new_class = cnn.classify(np.array([test_x[0]]))

## Save and Load the trained model
    cnn.save_model('saved_model')
	  cnn.load_model('saved_model')
    
