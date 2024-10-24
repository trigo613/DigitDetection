# Digit Detection 

This project focuses on detecting digits in images. The following steps outline the project's strategy, with visual a illustration for each step.

## Our goal

![final_boxes2](https://github.com/user-attachments/assets/421221a0-fda9-415a-9a23-aa8b2fc8c5ed)

## Table of Contents
- [Step 1: Load the Digit Data](#step-1-load-the-digit-data)
- [Step 2: Create Function to Draw a Box Around a Digit](#step-2-create-function-to-draw-a-box-around-a-digit)
- [Step 3: Load Images from Google Maps](#step-3-load-images-from-google-maps)
- [Step 4: Randomly Place the Digits in a Cropped Image](#step-4-randomly-place-the-digits-in-a-cropped-image)
- [Step 5: Draw a Bounding Box on the Digit](#step-5-draw-a-bounding-box-on-the-digit)
- [Step 6: Train the Model](#step-6-train-the-model)
- [Step 7: Sliding Windows](#step-7-sliding-windows)
- [Step 8: Non-Max Suppression](#step-8-non-max-suppression)
- [Future Improvements](#future-improvements)
- [Acknowledgments](#acknowledgments)

## Step 1: Load the Digit Data
In this step, we load the digit dataset that contains images of digits along with their labels.

![plain_digits](https://github.com/user-attachments/assets/1800ef48-db67-4fb8-a69f-7ff5d818f3f9)

## Step 2: Create Function to Draw a Box Around a Digit
We implement a function that can draw a bounding box around digits in the images.

![bounded_digits](https://github.com/user-attachments/assets/7ef99d69-851d-459e-8226-66c37aa687b0)

## Step 3: Load Images from Google Maps
Images are obtained from Google Maps, which will serve as the background for our digit placement.

![google_images](https://github.com/user-attachments/assets/b505c6b1-cc6a-4b96-8b48-da1252a264f1)


## Step 4: Randomly Place the Digits in a Cropped Image
This step involves randomly placing the digit images onto a cropped version of the Google Maps images.

![randomly_placed_digits](https://github.com/user-attachments/assets/c362cb3f-1aba-4dbc-9b24-f919501bbfd0)

## Step 5: Draw a Bounding Box on the Digit
We then draw bounding boxes around the digits that have been randomly placed in the images.

![randomly_placed_digits_bounded](https://github.com/user-attachments/assets/7e3ba732-744d-4d87-b172-cd6ca1b238e3)

## Step 6: Train the Model
The model is trained using the dataset we created and it's objective is to detect if there is a digit in the image, if yes then draw a bounding box around it and predict the digit inside. The following is the output of the model on some random sample data after 8 epochs

![digit_detection_performance](https://github.com/user-attachments/assets/8dbab641-5ab9-43ab-9483-cbe7a0c39498)


## Step 7: Sliding Windows
In this step, we implement a sliding window technique to detect digits in various parts of the images.


https://github.com/user-attachments/assets/e53a261d-933b-4161-8b04-a877171f6070


## Step 8: Non-Max Suppression
Finally, we apply non-max suppression to filter out overlapping bounding boxes, ensuring we retain only the most accurate detections.

![final_boxes2](https://github.com/user-attachments/assets/421221a0-fda9-415a-9a23-aa8b2fc8c5ed)

## Future Improvements

1. **Extended Training Duration**
   - Current model was trained for only 8 epochs
   - Increasing the number of training epochs is expected to significantly improve model accuracy and detection performance
   - The model is currently good at detecting in which window there is a digit and which digit it is, but it is bad at drawing the bounding boxes, training the model for longer will probably help improve this.

2. **Data Augmentation**
   - Implement additional data augmentation techniques
   - Add rotation, scaling, and noise to training images

3. **Model Architecture**
   - Experiment with different and bigger CNN architectures

4. **Performance**
   - Optimize code for better performance

## Acknowledgments

Acknowledgments to Andrew Ng's CNN course for foundational knowledge and guidance in this project.
