Introduction: In this project, we utilized the MNIST dataset to explore noise reduction using a KNN (K-Nearest Neighbors) Classifier. Our objective was to train the classifier to predict the original, non-noisy images from their noisy counterparts.

Importing the Libraries: We started by importing essential libraries: Numpy, Pandas, Matplotlib, and gzip.

Defining a Function to Show Images: A custom function, showImage(), was defined to help visualize images within the dataset.

Loading the Data: We loaded the MNIST dataset, split it into training and testing sets, and stored these in respective variables. The dataset comprises four files: training features and labels, and testing features and labels, each read and stored appropriately.

Exploring the Data: We printed the shape of our data variables, confirming that each image is represented by 784 features (28x28 pixels). The training set included 60,000 rows, while the test set had 10,000. We used showImage() to display some of the images along with their labels.

Shuffling the Data: To ensure reproducibility, we set a random seed and shuffled the training data using Numpy’s random.permutation().

Adding Noise to the Data: Noise was introduced using Numpy’s randint() function. The generated noise was added to both the training and testing sets, resulting in new variables: X_train_mod and X_test_mod. The labels for these noisy images were set as the original, non-noisy images.

Viewing the Noisy Data: Using showImage(), we visualized the noisy images alongside their original, non-noisy counterparts.

Training a KNN Classifier: We trained a KNN Classifier using Scikit-learn’s KNeighborsClassifier on the noisy images. The model’s task was to predict the original images from the noisy versions.

Predicting Noisy Images: Finally, we tested the model by feeding it a noisy image from X_test_mod and comparing its prediction with the corresponding original image from y_test_mod. The KNN Classifier successfully predicted the non-noisy images, demonstrating its capability in noise reduction.
