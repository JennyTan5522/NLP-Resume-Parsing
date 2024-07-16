About:

Managing and organizing resumes may be a challenging operation as traditional resume management, which is **time-consuming** and requires **manually sorting, organizing, and assessing** endless resumes. Named Entity Recognition (NER) is a technique used in Document Management System (DMS) for automatically extracting and categorising significant information from documents. NER entails identifying and categorizing entities inside a document, such as persons, organisations, and locations. By automating this process, NER can increase the efficiency and accuracy of document management while allowing users to quickly and readily obtain critical information.

In this study, we aim to solve the problem of manually screening resumes by proposing a **hybrid Automated Resume Named Entity Extraction (NER)** to automate resume data.

Objectives:
- Develop an effective Automated Resume NER system in processing resumes.
- Evaluate the performance of the Traditional Baseline Model (Rule-based model), Machine Learning-Based Model and Transformer-Based Model in performing Resume Named Entity Extraction (NER).
- CV Recommendation Model using Latent Dirichlet Allocation (LDA) based topic modelling on resume keywords and similarity scores of topic distributions.
- The hybridisation approach of the Traditional Baseline Model, Machine-Learning-Based Model and Transformer-Based Model for named entity resume documents.
- Automated summarization of candidates data and providing the functionalities such as searching and ranking based on the scores.

Dataset:
1) Around 200 Resumes from Kaggle: **Rule-based and Machine Learning** training and testing data
2) Around 220 Annotated Resumes from Kaggle: **BERT** training and testing data
3) Around 200 Resumes from Kaggle: **Spacy** training and testing data
4) Additional 5 Resume randomly selected to perform testing based on different models

Data Preprocessing:
Based on our research, not all the resumes will be cleaned in the NER processes. Therefore, in this study, we will evaluate the performance of resume named entity extraction (NER) before preprocessing and after preprocessing. 

CV Recommendation Model
- TF-IDF vectoriser to find the important terms inside the document and then computes the cosine similarity between the job description and CV.
- Purpose: Allows the HR department to check for the similarity of job distributions based on Top N candidates.

Topic Modelling
- Latent Dirichlet Allocation (LDA) technique is used to identify the main topics present in a collection of resumes. E.g. Group resumes into themes or topics, such as "Project Management", "Software Development" or "Data Analysis".
- Purpose: Quickly identify suitable candidates based on their skills and experiences listed in their resumes.
- Provided the function for users to search for the keyword appearing in each topic and ultimately return the relevant resumes.

  





