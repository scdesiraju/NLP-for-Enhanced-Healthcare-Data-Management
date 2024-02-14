# NLP-for-Enhanced-Healthcare-Data-Management

## Introduction

This project aims to develop a methodology for converting unstructured Electronic Health Record (EHR) data into structured formats using Natural Language Processing (NLP) techniques. By employing diverse classification models and integrating advanced models like T5, the project seeks to enhance healthcare data management by transforming unstructured transcriptions into structured data.

## Approach

### Extracting Structured Information from the Data

- **Regex-based extraction:** The initial phase of the data extraction process involved the identification of key headings within medical transcripts by recognizing capitalized words. Subsequently, data extraction for each selected keyword was executed using regular expressions (regex) to capture pertinent information under each heading.

- **GPT-based extraction:** GPT-3.5 was employed to extract medical entities from transcription texts, complementing regex-based extraction.

### Classification Model Development and Selection

- **Data Transformation Technique:** Term Frequency-Inverse Document Frequency (TF-IDF) was employed for transforming medical transcriptions, highlighting important terms while minimizing the impact of less significant words.

- **Implemented Models:** Multinomial Naive Bayes, One-vs-Rest Logistic Regression, Word2Vec, and LightGBM were selected and configured for categorizing medical transcriptions into distinct classes such as Gender, Medical Specialty, and Treatment Type.

### Entity and Sequence Generation Model

- **Data Structuring:** Following entity extraction, the extracted entities were concatenated into a unified column for structured data.

- **Transition to T5 Model:** Initially exploring SciSpacy and Fine-tuned BioBERT for entity tagging and sequence generation tasks, the focus shifted to the T5 model due to its flexibility and proficiency in handling sequence-to-sequence tasks.

## Related Work

The intersection of Natural Language Processing (NLP) and Artificial Intelligence (AI) in healthcare, especially Electronic Health Record (EHR) data management, has been extensively explored. Previous research in this field provides a foundation for this project.

## Experiments

- **Data:** The project utilized a Kaggle dataset comprising 5,000 entries across six columns, encompassing a diverse array of medical transcripts spanning various specialties.

- **Evaluation Method:** The primary evaluation metric selected was the Receiver Operating Characteristic Area Under the Curve (ROC AUC) for classification models and ROUGE-L metric for the T5 model.

- **Experimental Details:** Specific configurations of classification models and training parameters were detailed in the report.

## Results

- **Classification Task Results:** The average ROC AUC scores for various classification tasks were reported, showcasing the performance of different models in gender classification, specialty classification, and treatment type prediction.

- **T5 ROUGE-L Scores:** ROUGE-L scores for the T5 model using different hyperparameter settings were provided.

## Analysis

Qualitative evaluation of the system revealed insights into model performance and limitations observed. Different models exhibited distinct performances influenced by various factors.

## Conclusion

In summary, the project addresses the critical need for structured electronic health record (EHR) data by presenting a systematic approach that transforms unstructured medical transcripts into actionable formats. Achievements, limitations, and suggestions for future work were discussed.
