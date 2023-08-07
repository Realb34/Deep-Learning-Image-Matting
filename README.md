# Deep Image Matting with Custom Loss and Dataset

## Overview
This repository contains the implementation of a deep learning model for image matting, using custom-designed loss and dataset handling functionalities. The main components include the architecture, training loop, evaluation, and various error metric calculations.

The model consists of an Encoder for feature extraction and a Decoder for reconstructing the matted image. You can find the main implementation inside the DeepMatting class.

## Custom Loss Function
The AlphaLoss class defines a custom loss function, calculating the mean absolute difference between the predicted and ground truth alpha (transparency) values.

## Custom Dataset Handling
The CustomDataset class handles the loading and preprocessing of images and their corresponding masks.

## Error Metrics
Three error metrics are implemented for evaluation:

- Sum of Absolute Differences (sad_score)
- Mean Squared Error (mse_score)
- Custom Gradient Error (gradient_error)

## Training Loop
The training is set to run for 1500 epochs, using the Adam optimizer. It prints the loss and error metrics for each batch and saves the best model.

## Evaluation
The evaluation section loads a test image, runs it through the model, and displays the original image, output mask, and masked image side by side.

## Instructions:

## Training
1. Place your images and corresponding masks in the designated directories.
2. Set the desired parameters such as batch size, learning rate, etc.
3. Run the training loop.

## Evaluation
1. Place the test image in the specified path.
2. Load the pre-trained model using torch.load.
3. Run the evaluation code to visualize the results.

### Dependencies
- PyTorch
- Matplotlib
- PIL
- os
- CUDA GPU acceleration

## Conclusion
This repository provides a robust framework for deep image matting with custom functionalities for loss computation and dataset handling. It also includes comprehensive error metrics and evaluation functionalities to analyze and visualize the model's performance.

