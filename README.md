# LW4-Improving-CNN-Performance

Google Colab Link: https://colab.research.google.com/drive/1vZwsPt-NsgdPaSdPkL-3lAMWLupQaDXY?usp=drive_link

Model Link: https://drive.google.com/drive/folders/1dtUobXWtuUS6aPkx_Qf7FwRxE9OIXcuS?usp=sharing
A. Model Evaluation Analysis

1. What were the weakest-performing classes based on the confusion matrix?
The weakest-performing classes were the ones with the highest number of misclassifications, shown by larger off-diagonal values in the confusion matrix. These classes were frequently confused with similar categories, indicating poor feature distinction. This suggests that the model struggled to correctly identify images with overlapping visual characteristics.

2. How did Precision, Recall, and F1-score vary across classes?
Precision, Recall, and F1-score differed depending on how well each class was recognized. Some classes achieved high scores, meaning the model classified them accurately and consistently. Other classes had lower scores due to false positives or false negatives, indicating imbalance in prediction quality. F1-score provided a balanced measure by combining both precision and recall.

3. What does a low recall indicate in your model?
Low recall indicates that the model failed to correctly identify many actual instances of a class, producing more false negatives. This means the model missed relevant samples, reducing its reliability for detecting that category. In practical terms, the model underperformed in recognizing all true examples of that class.

4. How does AUC score reflect model performance compared to accuracy?
AUC score measures the model’s ability to distinguish between classes across different threshold values, making it more comprehensive than accuracy alone. While accuracy only measures correct predictions overall, AUC evaluates classification quality even in imbalanced datasets. A higher AUC indicates stronger discrimination capability and better overall predictive performance.


B. Model Improvement

5. How did data augmentation affect validation accuracy?
Data augmentation improved validation accuracy by increasing dataset diversity through image transformations such as flipping, rotation, zooming, and contrast adjustment. This helped the model generalize better to unseen data and reduced overfitting. As a result, validation performance became more stable and accurate.

6. Why is Batch Normalization important in CNNs?
Batch Normalization stabilizes and accelerates training by normalizing layer inputs during each batch. It reduces internal covariate shift, allowing the network to learn faster and more efficiently. Additionally, it improves convergence and contributes to better generalization.

7. What role did Dropout play in improving your model?
Dropout reduced overfitting by randomly disabling a percentage of neurons during training. This forced the model to learn more robust and distributed features instead of memorizing patterns. Consequently, the model became more resilient and performed better on validation data.

8. How did Early Stopping prevent overfitting?
Early Stopping monitored validation loss and automatically halted training when performance stopped improving. This prevented excessive training that could cause memorization of the training dataset. By restoring the best weights, it preserved the model at its optimal generalization point.


C. Performance Comparison

9. What improvements were observed after modifying the model?
After enhancement, the model showed higher validation accuracy, lower validation loss, improved precision, recall, F1-score, and better AUC performance. The confusion matrix also reflected fewer classification errors. Overall, the improved model demonstrated stronger generalization and reliability.

10. Which enhancement contributed the most to performance improvement? Why?
Data augmentation and Dropout likely contributed the most because they directly addressed overfitting, which is a common CNN weakness. Data augmentation expanded effective training diversity, while Dropout regularized the network. Together, these significantly improved validation performance.

11. Did the gap between training and validation accuracy decrease? Explain.
Yes, the gap decreased after implementing regularization techniques. This indicates improved generalization, as the model’s performance on unseen data became closer to its training performance. A smaller gap suggests reduced overfitting and a healthier learning process.



D. Explainability (Grad-CAM Integration)

12. How did Grad-CAM help in understanding model predictions?
Grad-CAM provided visual heatmaps showing which image regions most influenced predictions. This allowed students to verify whether the model focused on relevant object features rather than irrelevant background details. It improved transparency and interpretability of CNN decision-making.

13. Did the improved model focus on more relevant regions? Provide evidence.
Yes, the improved model generally focused more accurately on the target objects, as shown by clearer and more concentrated Grad-CAM heatmaps over meaningful image regions. Compared to the baseline, less attention was given to background noise, indicating stronger feature learning.

14. Why is explainability important in real-world AI applications?
Explainability is crucial because it builds trust, ensures transparency, and helps identify model errors or biases. In sensitive applications such as healthcare, security, or autonomous systems, understanding AI decisions is necessary for safety and accountability. Explainable AI supports responsible deployment and user confidence.
