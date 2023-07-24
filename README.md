# Pretrained_dog_classifier
My nanodegree project implementing a pre-trained image classifier to identify dog breeds.

# Objectives
1. Correctly identify which pet images are of dogs (even if breed is misclassified) and which pet images aren't of dogs.
2. Correctly classify the breed of dog, for the images that are of dogs.
3. Determine which CNN model architecture (ResNet, AlexNet, or VGG16), "best" achieve the objectives 1 and 2.
4. Consider the time resources required to best achieve objectives 1 and 2, and determine if an alternative solution would have given a "good enough" result, given the amount of time each of the algorithms take to run.

# This project meets the following specifications:
* calls the time functions before the start of main code and after the main logic has been finished.
* adds command line argument for '--dir': uses default ='pet_images/'
* adds command line argument for '--arch': default='vgg'
* adds command line argument for '--dogfile': default='dognames.txt'
* makes sure files starting with '.' are ignored: checks for '.' using a conditional statement.
* dictionary key and label are in the correct format and retrieves 40 key-value pairs.
e.g:- {'Poodle_07956.jpg': ['poodle'], 'fox_squirrel_01.jpg': ['fox squirrel'] ... }
* 'in_arg.dir' is passed as an argument inside check_images.py while calling the get_pet_labels function.
* appends images_dir to each value before making the function call.
* classifier(images_dir+users_key, model)
* convert the output to lower case and strip any whitespaces
* appends 1 to correct label, and 0 to falsely classified values, classifying Labels as dogs
* check the displayed output and see if all matches are appropriately displayed.
* check the displayed output and see if all non matches are appropriately displayed
Results
* all three models score as expected
  
## Setup
Install Python3  
Install PyTorch Using https://medium.com/@debarko/how-to-install-pytorch-on-a-mac-os-x-97a79e28c70

Run ``bash run_models_batch.sh`` to visualize results

View results in resnet_pet-images.txt, alexnet_pet-images.txt and vgg_pet-images.txt

Your Results Should Look Like This 
![Results Table](results.png)

# Additional questions addressed:
1. Did the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed? If not, report the differences in the classifications.
* Yes, all three models reported the same classification (american staffordshire terrier, staffordshire terrier, american pit bull terrier, pit bull terrier), though the image is of a dogo argentino (visually similar to pit bull terrier but not in the dictionary.)
2. Did each of the three model architectures classify the breed of dog in Dog_01.jpg to be the same breed of dog as that model architecture classified Dog_02.jpg? If not, report the differences in the classifications.
* ResNet and VGG both consistently misidentified the dogo argentino and the flipped image of the dogo argentino as american staffordshire terrier, staffordshire terrier, american pit bull terrier, pit bull terrier, whereas AlexNet inconsistently classified the flipped image as a weimaraner.
3. Did the three model architectures correctly classify Animal_Name_01.jpg and Object_Name_01.jpg to not be dogs? If not, report the misclassifications.
* Yes, all are correctly classified.
4. Based upon your answers for questions 1. - 3. above, select the model architecture that you feel did the best at classifying the four uploaded images. Describe why you selected that model architecture as the best on uploaded image classification.
* ResNet and VGG16 both consistently misidentified the dogo argentino and the flipped image of the dogo argentino as american staffordshire terrier, staffordshire terrier, american pit bull terrier, pit bull terrier, whereas AlexNet inconsistently classified the flipped image as a weimaraner. So ResNet and Vgg appear to be superior at identifying dog breeds. However, they differed in the classification of the non-animal picture (coffee) - VGG16 and AlexNet are the closest because they identified it as a bucket/pail or flower pot/pot, respectively, whereas ResNet thought it was mortar.
* Therefore, VGG16 is the optimal model architecture for the uploaded images.
