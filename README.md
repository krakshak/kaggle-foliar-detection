# kaggle-foliar-detection
Kaggle hosted a competiton in 2020 to detect diseases on apple leaves.<br> Competition Link: https://www.kaggle.com/c/plant-pathology-2020-fgvc7<br> Dataset Link: https://www.kaggle.com/c/plant-pathology-2020-fgvc7/data

**Problem Statement:**
The Objective is to train a model using images of training dataset to accurately classify a given image from testing dataset into different diseased category or a healthy leaf.

**Solution:**
Primarily this is a classification task, a vanilla CNN mdel would serve as an optimum solution for the problem statement and use case. The jupyter notbook in the repository would explain my solution in detail to fit a CNN model to identify and classify the images to their respective classes.

1) **Training data preparation:** We are reading the csv dataset which has the class label information. Once we add the label column as a numberical value to the train dataframe, we can create individual folders for each class.
2) **Data Preprocessing:**<ul><li>Reducing the size of images to (224,224) due to resource constraint(No GPU).</li><li>The above mentioned image dimensions will ensure to give the best results even though its reduced by a factor of 10x.</li><li>Spliting the data set into test and validations sets for model training.</li></ul>
3) **Model**: A seqeuntial CNN model is built and trained for 30 epochs.
4) **Accuracy & Loss:** The validation set accuracy is ~90%. This infers that the model has trained well but the class distribution of the training dataset is uneven. CNNs are known to perform well when the class distribution is even. Hence this result could have been better if the training sets had an even class distribution.
5) **Test cases using on Test Data:** <ul><li>In the 1st Test case, We are taking a train image to check the model's correctness.</li><li>In the 2nd test case, We are considering an actual test image for prediction to validate the prediction accuracy.</li></ul>
6) **Inferences:** <ul><li>In the 1st test case, We took a image that belongs to "Scab" class. The model was able to predict the image that it belongs to the Scab class which proves the model's correctness.</li><li>In the 2nd test case, the model was given a test input image. It was able to predict the image belongs to "Healthy" class which is evident from the test image.</li></ul>
