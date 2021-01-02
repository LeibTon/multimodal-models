## Implementing various Multimodal models (Visual and textua information) for Facebook Hateful memes competition. 
### Model 1:
A simple model that tries to learn textual features using attention model and learn Image features using pretrained models and then concatenate the result. However, the model has very less accuracy as it failed to see the relationship between textual and visual representation.

### Model 2:
Uses LSTM to extract features from textual data and uses Conv to extract information about visual data. Then uses a concatenation model based on [this](https://arxiv.org/pdf/1908.04107.pdf) paper. Model overfitted because of the complexity of model. Gave an accuracy of 98% on training data but around 60% on test data.

### Model 3:
Uses GLoVE Word Embeddings for textual feature extraction and trained model for visual feature extraction. Then uses same concatenation model as above for output. However the model again started overfitting.

### Model 4:
Use Some text filtering and then used GLoVE word embeddings for feature extraction and trained model for visual feature extraction. Simplified the above concatenation model to reduce the complexity and thus reduce overfitting. Accuarcy increased but wasn't much affected.

### Conclusion:
1. All these models possibly lose features during extraction. Can try a better feature extaction technique.
2. Can try data augmentation to reduce overfitting.
