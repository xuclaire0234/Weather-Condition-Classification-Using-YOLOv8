# Weather-Condition-Classification-Using-YOLOv8
This project involves building a weather condition classification model using a pre-trained YOLOv8 network and a custom image dataset. The goal is to classify images into categories such as "snowy," "rainy," and "foggy" by leveraging YOLOv8's lightweight and efficient architecture.

## 2. Dataset Preparation

### Dataset Organization
The dataset is structured into three subsets: training, validation, and testing. The split ratios are:
- **Training:** 50%
- **Validation:** 30%
- **Testing:** 20%

Each subset is organized into subdirectories corresponding to their respective categories.

### Process Overview
- **Data Extraction:** Extract image files from the root directory.
- **Splitting:** Divide the data into training, validation, and testing sets using `train_test_split`.
- **File Organization:** Copy images into their respective subdirectories for seamless integration with YOLO's training pipeline.

## 3. Model Training

### YOLOv8 Classifier
- **Pre-trained Model:** YOLOv8n (nano version) was selected for its efficiency in lightweight applications.
- **Input Size:** Images were resized to 64x64 for faster training.
- **Epochs:** The model was trained for 100 epochs to ensure convergence.

## 4. Visualization of Training Metrics

### Loss vs. Epochs
- **Training Loss:** Indicates the model's performance on the training dataset.
- **Validation Loss:** Measures the model's generalization ability on unseen data.

### Validation Accuracy vs. Epochs
- The accuracy metric evaluates the percentage of correctly classified images in the validation set.

### Key Observations:
- Gradual reduction in training and validation loss.
- Increasing validation accuracy demonstrates improved model performance and generalization.

---

## 5. Model Evaluation

### Test Predictions
The trained model was tested on unseen images from the testing set. It predicted weather conditions with probabilities for each class. The final prediction was based on the class with the highest confidence score.

### Results:
- **Class Labels:** Snowy, Rainy, Foggy.
- **Confidence Scores:** The model outputs a confidence score for each class, providing insights into its decision-making.

---

## 6. Conclusion

### Summary
This project demonstrates the application of YOLOv8 in image classification tasks, specifically for weather condition recognition. The model achieved high accuracy and was able to generalize well to unseen data.

### Key Learnings
1. **Dataset Preparation:** Proper organization and splitting significantly impact model performance.
2. **YOLOv8 Efficiency:** YOLOv8’s lightweight architecture makes it suitable for resource-constrained environments.
3. **Metrics Monitoring:** Visualizing training metrics provides valuable insights for diagnosing and optimizing model performance.

### Future Work
1. Expand the dataset to include additional weather conditions (e.g., sunny, cloudy).
2. Explore higher-resolution images to improve model accuracy.
3. Optimize the model for deployment on edge devices for real-time weather classification.
