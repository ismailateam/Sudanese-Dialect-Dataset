# SudaHate – Sudanese Hate Speech and Abusive Dataset

## 📌 Overview

**SudaHate** is The first Sudanese Arabic Hate Speech and Abusive Language Dataset designed to support research on toxicity detection in Sudanese dialect Arabic.

With the rapid expansion of social media usage in Sudan, online platforms have experienced increasing levels of toxic discourse including abusive and hate speech.  

SudaHate consists of 6908 Sudanese comments labeled as:

- Normal  
- Abusive  
- Hate  

---

## 📊 Dataset Statistics

- Total instances: 6908  
- Normal: 4859  
- Abusive: 1063  
- Hate: 986   
- Train/Test split:70% / 30% (4836 / 2072) 

---

## 🗂 Data Collection
The SudaHate dataset was constructed from two complementary sources to ensure both diversity and dialectal authenticity.

### 1️⃣ Lîsan Corpus (Sudanese Subset)

Part of the SudaHate dataset incorporates the Sudanese subset of the Lîsan corpus:

Jarrar, M. et al. (2023). *Lîsan: A corpus, dictionary, and POS tagger for dialectal Arabic processing*. Language Resources and Evaluation, 57, 1025–1067.

Official dataset page:
https://sina.birzeit.edu/resources/index.html

The Lîsan corpus is publicly available and permits redistribution under its original license. In accordance with those terms, we include the Sudanese subset (3,000 instances) in this repository.

Since the original Lîsan corpus was not annotated for hate or abusive language, all reused instances were fully re-annotated in this study using our unified three-class annotation scheme (Normal, Abusive, Hate).

The original Lîsan license terms remain applicable to the redistributed portion included in this repository.

### 2️⃣ Facebook Data Collection

To enhance coverage of contemporary Sudanese online discourse, we collected publicly accessible posts and comments from Sudanese Facebook pages using the Facebook Graph API via the Facepager tool.

Data collection was conducted in compliance with Facebook’s publicly available data access policies at the time of collection. Only content from public pages was retrieved.

More than 7,000 posts and comments were initially gathered. After automatic filtering (e.g., minimum length constraints and content cleaning), 4,441 texts were manually reviewed by three native Sudanese annotators to verify dialect authenticity and remove non-relevant or non-Sudanese content.

All personally identifiable information (PII), including usernames, profile identifiers, and metadata, was removed prior to annotation. The dataset contains text content only.

After automatic length filtering and cleaning, 4,441 texts were manually reviewed by three native Sudanese annotators to verify dialect authenticity and remove non-Sudanese or irrelevant content.

### 🔗 Final Annotation Pool

The verified Facebook texts were integrated with the re-annotated Lîsan subset to form an initial annotation pool of 7,049 Sudanese dialect sentences.

All data were collected from publicly available content. Personally identifiable information (PII), including usernames and metadata, was removed prior to annotation to ensure privacy protection and ethical compliance.


---

## 🏷 Annotation Guidelines

The annotation process was conducted by three Sudanese Arabic native-speaking annotators.

Labels were defined as follows:

### • Normal
Instances with no offensive, aggressive, insulting, or profane content.

### • Abusive
Instances containing offensive, aggressive, insulting, or profane language without targeting a protected group.

### • Hate
Instances that:
1. Contain abusive language,
2. Target a specific individual or group,
3. Demean or dehumanize the target based on identity (e.g., ethnicity, tribe, religion, gender, skin color, political affiliation, or belief).

Annotators were provided with contextual examples of Sudanese dialect expressions commonly used in toxic discourse (e.g., “______”, “______”).

---

## 📏 Annotation Quality

Annotation agreement was evaluated using:

- Pairwise Percent Agreement (PRAM): best value between annotator 1 & annotator 3 =  0.987 
- Cohen’s Kappa (K): best value between annotator 1 & annotator 3 =  0.973
- Fleiss’ Kappa: global reliability among the three annotators = 0.921

---

## 🧪 Baseline Experiments
### Multi-Class Classification (Normal / Abusive / Hate)

- Model: ______  
- Macro-F1: ______  
- Precision: ______  
- Recall: ______  

---

## ⚖ Ethical Considerations

- Data were collected from publicly accessible content.
- Usernames and identifying information were removed.
- The dataset contains offensive and potentially harmful language.
- Intended strictly for research purposes.
- Misuse for harassment, profiling, or discrimination is strongly discouraged.

---

## 📎 Citation

If you use SudaHate, please cite:

```bibtex
@article{SudaHate2025,
  title={SudaHate: A Sudanese Arabic Hate Speech Dataset},
  author={______},
  journal={______},
  year={2025}
}
```

---

## 🔖 Version

This release (v1.0) corresponds to the experiments reported in the associated publication.
