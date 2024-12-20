# Position-Based-Interaction-Using-InteractML-in-Unity

Introduction

In this project, we aim to create a position-based interaction system using Unity and
InteractML. Our goal is to train a machine learning model which classify and recognize
different movement data of the player based on specific positions in real-time and use
this data to adjust environmental parameters accordingly, such as changing light
intensity based on movement states. After recording several training examples we
trained the classification model using InteractML, where the trained model can
dynamically update environmental settings in Unity based on live position data.

Dataset

The dataset we used for this project consists of live position data recordings of an
avatar in a lab environment. We recorded different training examples and each
representing distinct states or behavior of the player. These recordings provided
integer-labeled data points correspond to each state.
Feature Extraction:
• The primary feature extraction was the avatar's position coordinates (e.g., x, y, z).
These features were mapped to the corresponding integer labels to enable
classification.

Model

We used InteractML’s Classification Model to recognize and classify avatar positions
based on the training data we collected. The classification model takes the position data
as input and outputs an integer that is the current state of the avatar. Several recording
examples are needed to train and run a robust classification model.
Key Model Components:
1. Input Features: Real-time position data of the avatar.
2. Output Labels: Integer values (0, 1, 2, 3).
3. Prediction Usage: The predicted integer value is used to dynamically control the
intensity of light in Unity.

![image alt](https://github.com/injamul-abeg/Position-Based-Interaction-Using-InteractML-in-Unity/blob/main/Light_Intensity_InteractML.png?raw=true)

Training and Evaluation

Training Process
• We manually recorded multiple training examples for each state by assigning
different integer values. Then we moved the avatar position differently after every
input. These recording examples were fed into the InteractML Classification
Model for training.
• The model learned to associate position coordinates with the corresponding
integer labels.
Evaluation
• After training, we tested the model that is able to classify position of the avatar
and control the intensity of the light based of avatar position. The model's
predictions were evaluated by observing the output integer and checking if it
matched the expected state.
Results
The model efficiently classified avatar positions and generated the correct integer
outputs for most cases. This classification allowed us to control the intensity of light
dynamically in Unity:
• Integer (0): Light intensity set to 0
• Integer (1): Light intensity set to 1
• Integer (2): Light intensity set to 2
The performance of the model was reliable when tested with new live position data,
where it is updating environmental parameters in real-time.

Conclusion

This project successfully implemented a position-based interaction system using Unity
and InteractML. By training a classification model with live position data, we are able to
control environmental settings such as light intensity based on avatar movement. The
performance of the system highlights the potential for using machine learning to
enhance interactive experiences in Unity-based applications.

References

1. InteractML Unity
 
