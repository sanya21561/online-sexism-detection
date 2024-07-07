# Explainable Detection of Online Sexism

This project aims to develop a system that accurately flags text from online platforms as sexist or non-sexist. It further classifies sexist comments into four sub-categories: Threats plans to harm and incitement, Derogation, Animosity, and Prejudiced Discussion.

## Tech Stack
- Python
- RoBERTa
- DeBERTa
- BiLSTM
- sklearn
- Matplotlib

## Methodology
Our task is divided into two parts:
- **Task A: Binary Sexism Detection**: Classifies comments as sexist or non-sexist using RoBERTa-Large.
- **Task B: Multi-class Sexism Classification**: Classifies sexist comments into four categories using DeBERTa-v3-Large.

### Steps:
1. **Tokenization**: Using RoBERTa for Task A and DeBERTa tokeniser for Task B.
2. **Model Training**: Combining BERT, RoBERTa, DeBERTa, and BiLSTM for classification tasks.
3. **Explainability**: Using Pointwise Mutual Information (PMI) to find the association between words and labels.

## Experimental Setup
### Task A:
- **Epochs**: 3
- **Learning Rate**: 4e-6
- **Batch Size**: 10
- **Max Length**: 70

### Task B:
- **Epochs**: 8
- **Learning Rate**: 1e-5
- **Batch Size**: 10
- **Dropout Probability**: 0.3
- **Output Size**: 4 (for 4-class classification)

## Results
- **Binary Classification**: Achieved an accuracy of 85%.
- **Multi-class Classification**: Achieved a 70% F1 score across four categories.

## Conclusion
We achieved significant accuracy in both tasks. The model's explainability was enhanced by masking offensive words using PMI. The context of sentences heavily influenced the classification results.

## Future Work
Future work includes:
- Extending the research to Indian social media datasets.
- Addressing the imbalance in the dataset.
- Applying the model to social media platforms for real-world evaluation.


## References
- Hassan, F., Bouchekif, A., & Aransa, W. (2023). FiRC at SemEval-2023 Task 10: Fine-grained Classification of Online Sexism Content Using DeBERTa.
- Chiu, K.-L., Collins, A., & Alexander, R. (2022). Detecting Hate Speech with GPT-3.
- Younus, A., & Qureshi, M. A. (2022). A Framework for Sexism Detection on Social Media via ByT5 and TabNet.
- Meyer, R. (2016). Twitter’s Famous Racist Problem. The Atlantic.
- Paula, A. F. M. de, & Silva, R. F. da. (2022). Detection and Classification of Sexism on Social Media Using Multiple Languages, Transformers, and Ensemble Models.

