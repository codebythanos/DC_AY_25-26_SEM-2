# Model Performance Evaluation
dc_resnet(data_aug).ipynb
The model is based on the ResNet50 architecture using transfer learning.

Test Accuracy: 53%
Validation Loss: Reduced from ~1.98 to ~1.42
Macro Avg: Precision: 0.53 | Recall: 0.53 | F1-score: 0.52
Key Points
Used pretrained ResNet50 with frozen layers initially
Applied data augmentation to improve generalization
Fine-tuning of deeper layers boosted performance
Moderate confusion between similar script classes

updated_resnet_dc.ipynb
The model is based on the ResNet50V2 architecture using transfer learning .

Test Accuracy: 74.39%
Balanced Accuracy: 74.39%
Macro Avg F1-score: 0.74
Weighted Avg F1-score: 0.74
Key Points
Used pretrained ResNet50V2 with frozen base in initial phase
Applied heavy data augmentation to reduce overfitting
Fine-tuned top layers for better feature learning
Used class weights and Test-Time Augmentation (TTA) for improved accuracy
Significant improvement compared to basic ResNet50 model

dc-aug-3april(RESNET BACKBONE ).ipynb
The model is based on the ResNet50 architecture using transfer learning with combined training phases .

Test Accuracy: 77.56%
Macro Avg F1-score: ~0.77
Key Points
Combined both training phases (head training + fine-tuning)
Used large-scale augmentation (up to 50K images per class)
Best performance achieved with lr = 1e-5 and dropout = 0.4
Significant improvement with increasing data size
Strong performance across most classes

dc-noaug(VIT).ipynb
The model is based on the Vision Transformer (ViT) architecture using transfer learning with two-phase training .

Test Accuracy: 76.92%
Macro Avg F1-score: ~0.77
Key Points
Used pretrained ViT backbone with frozen layers in Phase 1
Fine-tuned full model in Phase 2 for better feature learning
Achieved best validation accuracy of 85.60%
Strong performance across most classes (especially Odia, Gujarati)
Handles complex patterns better than traditional CNNs

dc_vit.ipynb
The model is based on the Vision Transformer (ViT) architecture using transfer learning with hyperparameter tuning and fine-tuning .

Test Accuracy: 82.36%
Macro Avg F1-score: ~0.82
Key Points
Used pretrained ViT backbone with CLS token classification
Two-phase training (feature extraction + fine-tuning)
Best configuration: lr = 5e-5, dropout = 0.2, backbone trainable
Achieved highest validation accuracy: 87.48%
Significant improvement after hyperparameter tuning
Strong performance across all classes (especially Odia, Punjabi, Gujarati)

82.97.ipynb
The model is based on the Vision Transformer (ViT) architecture using transfer learning with mixed precision and hyperparameter tuning .

Test Accuracy: 82.97%
Macro Avg F1-score: ~0.83
Key Points
Used pretrained ViT backbone with CLS token classification
Applied mixed precision training for faster computation
Performed hyperparameter tuning (lr, dropout, fine-tuning)
Best configuration: lr = 5e-5, dropout = 0.2, backbone trainable
Achieved highest validation accuracy: 88.06%
Strong and consistent performance across all classes
