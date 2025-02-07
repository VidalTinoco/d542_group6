# **Analyzing Developer Conversations with ChatGPT**  

## **Overview**  
This project explores developer interactions with ChatGPT, leveraging natural language processing (NLP) and machine learning techniques to analyze prompt structures, issue resolution patterns, and the predictability of conversation length. Using GitHub discussions and issue reports as a dataset, we aim to uncover key insights into how developers seek AI assistance and determine whether specific prompt characteristics influence conversation outcomes.  

## **Research Questions**  
1. What types of issues do developers bring to ChatGPT? (Research Question 1)  
2. Do structured prompts correlate with successful issue resolution? (Research Question 2)  
3. Can we accurately predict the length of a conversation based on the initial prompt and context? (Research Question 7)  

## **Project Structure**  

```plaintext
d542_group6/
│── data/                # Raw and clean dataset 
│── data_cleaning/       # Preprocessing scripts 
│── RQ1/                 # Analysis & results for Research Question 1
│── RQ2/                 # Analysis & results for Research Question 2
│── RQ7/                 # Analysis & results for Research Question 7
│── Project.pdf          # Final project report
│── .gitattributes       # Git tracking settings
│── .DS_Store            # macOS system file (ignore)
```

## **Methodology**  
### **1. Data Processing**  
- **Data Cleaning:** Extracted and normalized data from GitHub discussions and issues (August 31, 2023 snapshot).  
- **Language Filtering:** Kept only English conversations for better NLP performance.  
- **Feature Engineering:** Extracted textual features (word counts, sentiment, lexical diversity), code presence (via regex), and topic modeling (LDA, TF-IDF, embeddings).  

### **2. NLP Analysis & Machine Learning**  
- **Topic Modeling:** Identified common themes in developer queries using Latent Dirichlet Allocation (LDA).  
- **Prompt Structuring & Issue Resolution:** Analyzed correlation between prompt clarity and successful resolution using clustering techniques (K-means, WH-word analysis).  
- **Conversation Length Prediction:** Trained random forest, gradient boosting, and neural networks to predict conversation length.  

### **3. Model Evaluation**  
- Random Forest achieved the best results, though the overall prediction accuracy remained limited (R² ≈ 0.35, MAE ≈ 9.68 prompts).  
- Findings indicate that structured, well-defined prompts lead to shorter, more effective conversations, while vague prompts often result in longer, unresolved discussions.  

## **Key Findings**  
- Developers primarily use ChatGPT for debugging, implementation guidance, and theoretical questions.  
- Clear, structured prompts are linked to higher issue resolution rates, whereas ambiguous queries often lead to unresolved cases.  
- Predicting conversation length is challenging, as many external factors influence user interactions beyond textual features.  

## **Future Work**  
-  Explore advanced deep learning models (transformers, GPT embeddings) to improve prediction accuracy.
-  Analyze sequential conversation flow to understand how discussions evolve over time.  

## **How to Run This Project**  
1. Clone the repository:  
   ```bash
   git clone https://github.com/VidalTinoco/d542_group6
   cd d542_group6
   ```  
2. Run individual analysis scripts within the `RQ1`, `RQ2`, and `RQ7` folders.  
3. For full conversation length prediction, navigate to `RQ7` and execute the modeling script.  

## **References**  
- **NAIST (2023).** DevGPT Dataset.  
- **Chollet, F. (2023).** *Keras Sequential Model Guide.* Retrieved from [https://keras.io/guides/sequential_model/](https://keras.io/guides/sequential_model/)  
- **OpenAI & DeepSeek (2024).** Model architecture suggestions for neural network implementation.  
