<h1>Covid-19 Detection</h1>
<h3>The Proposed Framework</h3>
<p>As we have limited amount of data i.e we have some constraint over the data sizes we have taken the help of transfer learning to fine tune on our <b><i>COVID-Xray 5-K dataset.</i></b></p>
<p align="centre">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/Sample-images-from-COVID-Xray-5k-dataset-The-images-in-the-first-row-show-4-COVID-19.png" width="450" title="COVID-Xray 5-K dataset",alt="Lung Radiograms">
</p>
<h4>Transfer Learning Approach</h4>
<p>There are mainly two approaches in which the pre-trained networks can be used:-</p>
<p><i>1. <b>Feature Extractor</b> and then the classifier is trained to do the classification</i> .</p>
<p><i>2. <b>Subset of the classifier</b> to get finetuned on the new tasks.</i><p>
<p align="right">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/Untitled%20presentation.jpg" title="Types of use of Transfer Learning",alt="Lung Radiograms">
</p>
<h4>Transfer Learning Approach role in our Model Architecture</h4>
<p>As mentioned earlier the number of images in the dataset is  a matter of concern , we will here adapt to train the last layer of the classifier (mainly the CNN) and essentially here it has been used as the feature extractor in our model. </p>
<h4>Covid-19 Detection Using Residual ConvNet - ResNet18 </h4>
<p>Here mainly we have used the ResNet18 model trained on the ImageNet Dataset.ResNet is one of the most popular CNN architecture, which provides easier gradient flow for more efficient training of the CNN architecture. The core idea of ResNet is introducing a so-called <b><i>identity shortcut connection </b></i> that skips one or more layers. This would help the network to provide a direct path to the very early layers in the network, making the gradient up-dates for those layers much easier.  </p>
<p align="centre">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/ResNet-18.png" title="ResNet18 Model Architecture",alt="ResNet18">
</p>
<h3>The Training</h3>
<p>Here we have mainly used the Cross-Entropy Loss function which here mainly tries to minimize the distance between the predicted probability scores and the ground truth probabilities and is defined as :- </p>
<p align="centre">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/CrossEntopy.png" title="ResNet18 Model Architecture",alt="ResNet18">
</p>
<p>where p i and q i denote the ground-truth, and predicted probabilities for each image, respectively.</p>
<h3>Evaluation Metrics</h3>
<p>There are different metrics which can be used for evaluating the performance of classification models, such as classification accuracy, sensitivity, specificity, precision, and F1-score. Since the current test dataset is highly imbalanced (100 COVID-19 images, 3000 Non-COVID image), sensitivity and specificity are two proper metrics which can be used for reporting the model performance:</p>
<p align="centre">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/Eval.png" title="Evaluation Metrics",alt="ResNet18">
</p>
<p>This is the evaluation results which our model architecture has received:-</p>
<p align="centre">
  <img src="https://github.com/Nilotpal1998/Computer-Vision/blob/main/Covid_19_Detection/images/eval_result.png" title="Evaluation on ResNet18",alt="ResNet18">
</p>
<p>We have almost reached an accuracy of almost <b>97.5 % accuracy </b> . This project is under development and we are also trying to incorporate other transfer learning techniques for better results. Thank You. </p>
