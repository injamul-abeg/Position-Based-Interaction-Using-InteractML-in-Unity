# Position-Based-Interaction-Using-InteractML-in-Unity
Introduction
In this project, we aim to create a position-based interaction system using Unity and
InteractML. Our goal is to train a machine learning model which classify and recognize
different movement states of the player based on specific positions in real-time and use
this data to adjust environmental parameters accordingly, such as changing the color of
environment light based on movement states. After recording several training examples
we trained the classification model using InteractML, where the trained model can
dynamically update environmental settings in Unity based on live position data.
Dataset
The dataset we used for this project consists of live position data recordings of an
avatar in a clean lab environment. We recorded different training examples and each
representing distinct states or behavior of the player. These recordings provided
integer-labeled data points correspond to each state.
Feature Extraction:
• The primary feature extraction was the avatar's position coordinates (e.g., x, y, z).
These features were mapped to the corresponding integer labels 0 or 1 to enable
classification.
Model
We used InteractML’s Classification Model which is K-Nearest Neighbors (KNN)
algorithm that classify avatar positions based on the training data we collected. The
classification model takes the position data as input and outputs either 0 or 1 based on
current state of the avatar. Several recording examples are needed to train and run a
robust classification model.
Key Model Components:
1. Input Features: Real-time position data of the avatar.
2. Output Labels: Integer values 0 or 1.

![image alt](https://github.com/injamul-abeg/Position-Based-Interaction-Using-InteractML-in-Unity/blob/main/Model.png)

Training and Evaluation
Training Process
• We manually recorded multiple training examples for each state by labeling as 0
for wrong path and 1 for the right path direction. Then we moved the avatar
position differently after every input.
• These recording examples were fed into the InteractML Classification Model for
training which performs a binary classification. The model learned to associate
position coordinates with the corresponding integer labels.

![image alt](https://github.com/injamul-abeg/Position-Based-Interaction-Using-InteractML-in-Unity/blob/main/Data%20Recording.jpg)

Evaluation
• After training, we tested the model that is able to classify position of the avatar
and control the light based on avatar´s current state. We evaluated the
performance of the model using a confusion matrix.
Results
The model efficiently classified avatar positions based on the input label. This
classification allowed us to control the environment light dynamically in Unity where the
color of the light turn red and green for the predicted integer value 0 and 1 respectively.
As we evaluated the accuracy of the model’s classification using confusion matrix, here
is the key metrics output value from the confusion matrix:
• Accuracy: 0.90, where the model correctly classified 90% of all cases.
• Precision: 0.92, when the model predicts positive, it is correct 92% of the time.
• Recall: 0.98, the model almost correctly identifies actual positives.
• F1-Score: 0.95, suggest a good balance between precision and recall.
The performance of the model was reliable when tested with new live position data,
where it is updating environmental parameters in real-time.

References

1. InteractML Unity
 
