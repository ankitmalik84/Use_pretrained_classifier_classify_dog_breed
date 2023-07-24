# Use Pretrained Classifier To Classify Dog Breed

## Project Overview
Welcome to the "Use_pretrained_classifier_classify_dog_breed" project! The objective of this project is to implement a pre-trained image classifier that can accurately identify dog breeds from pet images.

## Objectives
1. Correctly identify which pet images are of dogs (even if the breed is misclassified) and which pet images aren't of dogs.
2. Correctly classify the breed of the dog for the images that are of dogs.
3. Determine the best CNN model architecture among ResNet, AlexNet, and VGG16 that achieves objectives 1 and 2 effectively.
4. Consider the time resources required to achieve objectives 1 and 2, and explore alternative solutions to achieve good results within reasonable time constraints.

## Getting Started
To run the project, make sure you have Python 3 and PyTorch installed. If you haven't installed PyTorch, you can follow the instructions provided [here](https://medium.com/analytics-vidhya/4-steps-to-install-anaconda-and-pytorch-onwindows-10-5c9cb0c80dfe).

## How to Use
1. Clone this repository to your local machine.
2. Run the script `run_models_batch.sh` to visualize the results.
3. The results will be stored in `resnet_pet-images.txt`, `alexnet_pet-images.txt`, and `vgg_pet-images.txt`.

## Project Results
After running the project, you should see a results table similar to the one shown below:

![Results Table](results.png)

## Additional Questions Addressed
1. Did the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed?
   - Yes, all three models reported the same classification, although the image is of a dogo argentino, visually similar to a pit bull terrier but not in the dictionary.

2. Did each of the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed of dog as that model architecture classified Dog_02.jpg?
   - ResNet and VGG consistently misidentified the dogo argentino and the flipped image of the dogo argentino as american staffordshire terrier, staffordshire terrier, american pit bull terrier, pit bull terrier. AlexNet inconsistently classified the flipped image as a weimaraner.

3. Did the three model architectures correctly classify Animal_Name_01.jpg and Object_Name_01.jpg to not be dogs?
   - Yes, all are correctly classified.

4. Based on the answers for the previous questions, which model architecture performed the best at classifying the uploaded images?
   - ResNet and VGG16 both consistently misidentified the dogo argentino and the flipped image, whereas AlexNet showed some inconsistencies. However, ResNet misclassified the non-animal image (coffee) as mortar, while VGG16 and AlexNet provided more reasonable classifications (bucket/pail and flower pot/pot, respectively). Hence, considering overall performance, VGG16 appears to be the optimal model architecture for the uploaded images.

## Conclusion
In conclusion, the "Use_pretrained_classifier_classify_dog_breed" project successfully implemented a pre-trained image classifier to identify dog breeds from pet images. The thorough analysis of different model architectures, along with considering time resources, ensures a robust and efficient solution to the problem. The project's creator has done an excellent job in achieving the objectives and providing valuable insights into the model's performance. Great work!
