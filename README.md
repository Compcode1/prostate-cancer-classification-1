This project simulated a prostate cancer screening test to evaluate how varying thresholds impact the ability of the model to correctly classify clinically significant prostate cancer. By adjusting the decision thresholds, we aimed to understand the trade-offs between **Sensitivity (Recall)**, **Specificity**, **Precision**, and the overall **F1 Score**.

### Key Findings:

1. **Optimal F1 Score at Threshold 0.6**:
   - The best **F1 Score** of **0.92** was achieved at a threshold of **0.6**, which provided a strong balance between Precision and Recall. 
   - At this threshold, the confusion matrix was as follows:
     ```
     Confusion Matrix for Threshold 0.6 (left to right: +,-, top to bottom: +,-):
     [[TP = 277  FP = 45]
      [FN = 0  TN = 678]]
     ```
     - **Accuracy**: 0.95
     - **Sensitivity (Recall)**: 1.00
     - **Specificity**: 0.94
     - **Precision**: 0.86
     - **F1 Score**: 0.92
   
   The **Sensitivity** at this threshold was perfect (1.00), meaning that all true positive cases (clinically significant prostate cancer) were correctly identified. This came at the cost of **45 false positives**, which slightly reduced Precision to **0.86**. However, the balance between Precision and Sensitivity led to an optimal **F1 Score** of **0.92**, indicating that this threshold offers a highly effective trade-off for this screening test.

2. **Threshold Performance Plot**:
   - The Threshold Performance Plot shows how **Sensitivity**, **Specificity**, **Precision**, and **F1 Score** change as we adjust the threshold from **0.0** to **1.0**.
   - At lower thresholds (0.0 to 0.4), **Sensitivity** remains high because the model classifies most instances as positive, but this results in low **Specificity** and **Precision** due to many false positives.
   - As the threshold increases, **Specificity** and **Precision** improve, peaking at around **0.6**, while **Sensitivity** gradually decreases.
   - Beyond **0.7**, **Sensitivity** drops significantly as the model becomes stricter, classifying fewer instances as positive. However, **Specificity** and **Precision** continue to rise, as fewer false positives are predicted.
   - **F1 Score** peaks around **0.6**, where the balance between catching true positives (Sensitivity) and minimizing false positives (Precision) is optimal.

3. **ROC Curve and AUC Analysis**:
   - The **ROC Curve** helped visualize the trade-off between Sensitivity and Specificity at various thresholds, showing the model's ability to distinguish between positive and negative cases.
   - The **AUC (Area Under the Curve)** of **0.97** indicates that the model is highly effective at separating clinically significant prostate cancer from healthy and indolent cases. This means the model has a **97% chance** of ranking a true positive higher than a false positive.
   
### Conclusion Summary:

By simulating this prostate cancer screening test, we demonstrated that the **0.6 threshold** provided the most balanced and effective screening performance, achieving an **F1 Score of 0.92**. This threshold captured all true positives while maintaining a reasonable level of false positives, making it a strong candidate for maximizing the screening test's effectiveness. The results from the **ROC curve** and **AUC** further supported this conclusion, showcasing the model's ability to perform well across a wide range of thresholds.
