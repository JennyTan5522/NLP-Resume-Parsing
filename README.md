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
2) Around 220 Annotated Resumes from Kaggle: **BERT** training and testing data (JSON format)
3) Around 200 Resumes from Kaggle: **Spacy** training and testing data (JSON format)
4) Additional 5 Resume randomly selected to perform testing based on different models

Data Preprocessing:

Based on our research, not all the resumes will be cleaned in the NER processes. Therefore, in this study, we will evaluate the performance of resume named entity extraction (NER) before preprocessing and after preprocessing. 

CV Recommendation Model
- TF-IDF vectoriser to find the important terms inside the document and then computes the cosine similarity between the job description and CV.
- Purpose: Allows the HR department to check for the similarity of job distributions based on Top N candidates.
  
  ![image](https://github.com/user-attachments/assets/03c04825-24d3-40c7-be76-b6d3cee987da)
  
  ![image](https://github.com/user-attachments/assets/8210fad8-3289-4ce4-af3a-92ed863e5b95)

Topic Modelling
- Latent Dirichlet Allocation (LDA) technique is used to identify the main topics present in a collection of resumes.
- Purpose: Quickly identify suitable candidates based on their skills and experiences listed in their resumes.
- Provided the function for users to search for the keyword appearing in each topic and ultimately return the relevant resumes.

  ![image](https://github.com/user-attachments/assets/b04312df-138f-4f23-90fa-9a8dc9648292)

  Search candidates' resume based on keywords
  
  ![image](https://github.com/user-attachments/assets/a6de1a2a-c87a-49c8-a7a2-fe777688f7b2)

EDA 
1) WordCloud

   ![image](https://github.com/user-attachments/assets/7f0f070f-1a23-4207-a4c5-ba17c0eb5a02)

3) N-Grams
   
   ![image](https://github.com/user-attachments/assets/e5cb1942-fcd0-478c-857c-d4a67c203654)


Rule-based Model (Established patterns or rules to identify)
1) Identify candidates name
2) Identify phone number
3) Identify email address
4) Identify qualifications
5) Identify graduation years
6) Identify locations
7) Identify candidate job skills (check if any keywords matched from the skill_set.txt corpus)
8) Identify university names
9) Identify company name
10) Identify candidate's designations or working experience (check if any keywords matched with job titles in the job-title.txt corpus)

Machine learning based named entities recognition labeling
![image](https://github.com/user-attachments/assets/30b0e2b0-7de3-45cd-9414-3f8a23de0878)

Spacy Model:
Pre-trained on a large dataset of text documents

Results
1) Rule-based
   
   ![image](https://github.com/user-attachments/assets/b22db245-f30d-40e1-acef-81a209bfc9ae)

3) Machine Learning + Rule-based
   
   ![image](https://github.com/user-attachments/assets/a3c52252-01b6-4bdf-a684-d76808b96c44)

5) Spacy
   
   ![image](https://github.com/user-attachments/assets/ce956f6a-8f5c-430a-9d41-c066be43cf91)
   
   ![image](https://github.com/user-attachments/assets/606a315c-89f7-494c-a290-0d8775e0911b)
   
   ![image](https://github.com/user-attachments/assets/c84166a0-4f08-4a7b-b226-ef0bfdbe9b8d)

  Spacy Prediction (Testing)
  
  ![image](https://github.com/user-attachments/assets/f14d92a7-40b7-49f3-a7b6-f57617be083d)

**Proposed Hybrid Model (Rule-based + Spacy)**
- The hybrid model is a combination of rule-based, machine learning, and transformer NER. It inherits all the strengths of each NER approach by covering the weaknesses of the others.
  
![image](https://github.com/user-attachments/assets/bda9b543-48d5-4d6e-8b58-f4fab260bb1c)


Sample Results:
![image](https://github.com/user-attachments/assets/193270aa-2334-4dff-a3f2-714b5bd6f4cf)

![image](https://github.com/user-attachments/assets/b4194fb1-d29d-4cdf-9e93-f3a260afb914)

![image](https://github.com/user-attachments/assets/27536c3d-73f8-4d87-82ab-47d488ef236c)

Preprocessing Results before and after
![image](https://github.com/user-attachments/assets/a21ebe85-a4f9-41bb-acbf-3e67322a7516)

Extra Modules (NER Functionalities - Search, Summary and Ranking)
1. Search candidate and retrieve the Resume Summary Report
   
![image](https://github.com/user-attachments/assets/b6374a10-7ec3-4e26-87b8-77e0819faa97)

3. Skills Ranking Score
   
![image](https://github.com/user-attachments/assets/48c9aa21-f0f6-401d-94aa-8850bac1dd60)

5. Search candidate
   
![image](https://github.com/user-attachments/assets/07fe3556-a047-4480-aea8-10da094b74c4)

Results and Findings:
1) Hybrid entity extraction showed better performance as compared to the single model. It has the highest detectability in classifying the value to respective entity labels. The hybrid model can extract the resume-named entities from the tested resume, such as name, email, phone number, skills, designation, company and more. The proposed hybrid strategy enhances the results for identifying the resume-named entities with an achievement of precision 87.62% and recall 96.91%. 

2) We found that preprocessed text caused our rule-based model to perform worse than when it was applied to the original text. This is likely because the preprocessing step removed important information.

Future Work and Limitation:
- The non-standardization of resume structure makes it difficult to automatically extract named entities recognition.








  





