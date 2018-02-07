# Content-Based-image-retriever-using-Denoising-Autoencoder

Content based image retrieval (CBIR) systems enable to find similar images to a query image among an image dataset. The most famous CBIR system is the search per image feature of Google search.This project is a CBIR made on the MNIST dataset based on the Deep Learning Framework.

Our CBIR will be based on convolutional denoising autoencoder.It is a class of unsupervised learning algorithms.Basically we first extract features from an image database and store it. Then we compute the features associated with a query image. Finally we retrieve images with the closest features.

![alt tag](https://cdn-images-1.medium.com/max/750/1*A8XGoiRfGusTxdfmglrKww.png)

## Feature Extraction

The key point about content based image retrieval is the feature extraction. The features correspond to the way we represent an image on a high level.The features we extract should also allow an efficient retrieval of the images. This is especially true if we have a big image database. 

One possibility to extract the feature maps is to use deep learning algorithms. In this research paper the authors demonstrate that convolutional neural networks (CNN) trained for classification purposes can be used to extract a ‘neural code’ for images. These neural codes are the features used to describe images. It also demonstrates that it performs as well as state of the art approaches on many datasets. The problem about this approach is that we first need labelled data to train the neural network. The labelling task can be costly and time consuming. Another way to generate these ‘neural codes’ for our image retrieval task is to use an unsupervised deep learning algorithm. This is where the denoising autoencoder comes.
 
## Denoising autoencoder

A denoising autoencoder is a feed forward neural network that learns to denoise images. By doing so the neural network learns interesting features on the images used to train it. Then it can be used to extract features from similar images to the training set.

![alt tag](https://blog.keras.io/img/ae/autoencoder_schema.jpg)

