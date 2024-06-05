# Question Answering System via Semantic Role Labeling Using Diverse Token Classification Techniques

This project was taken up as a part of project-work for Deep Learning course of 6th semester.

## Abstract
This project develops a Question Answering (QA) system using Semantic Role Labeling (SRL) to identify semantic roles of words in sentences and find answers from text. The motivation stems from the need for intelligent systems that understand and respond to natural language queries. By incorporating SRL, the system comprehends roles and relationships within sentences, enhancing QA accuracy. In this project work, in order to classify the phrases we explore a number of token classification techniques like NER tags, POS tags, dependency parse tags. We have utilized the Pretrained BERT, Spacy models for token classification tasks. The evaluation is conducted using average cosine similarity metric to assess the performance of the model. The experiments demonstrate that results from diverse token classifications can be fused to predict the semantic roles within sentences and can be effectively integrated with the QA systems.

## Objectives
- Create a Question Answering system that effectively utilizes SRL to understand and process natural language queries.
- Seamlessly integrate SRL into the QA system to identify the semantic roles of words within sentences, enhancing the system's comprehension
- Employ straightforward and easy-to-implement token classification techniques to achieve robust SRL results, making the system more accessible for practical applications.
- Develop and utilize suitable evaluation metrics, such as cosine similarity for semantic closeness, to assess the performance and effectiveness of the integrated QA system.

## Architecture diagrams
|**SRL system**|**QA system**|
|:-:|:-:|
|![semantic-role-labeling-architecture](https://github.com/Nanditha-Prabhu/qa-system-via-srl/assets/107810300/dda90adf-31c1-40e3-9333-f96864e9aa3b) |![qa-system-architecture](https://github.com/Nanditha-Prabhu/qa-system-via-srl/assets/107810300/285dd2a3-850a-4b39-9fae-05067ecfbb06)|
<!--https://medium.com/analytics-vidhya/7-advanced-markdown-tips-5a031620bf52-->

## Results
**Paragraph**: *Alice visited the museum on Tuesday afternoon. The stock market experienced a significant drop last week. Bob enjoys playing the guitar in his free time. The weather forecast predicts rain for the weekend. Sarah bought a new dress for the upcoming party. The new cafe downtown serves the best coffee in the city. Mike is planning a hiking trip next month. The movie was released to critical acclaim. The cat slept peacefully on the windowsill. Jenny is taking a course on digital marketing.* \
\
**Question 1**: *Who enjoys playing guitar?* \
**Semantic Role Labeling of the relavant sentence**: `{'Agent': 'Bob', 'Patient': 'the guitar', 'Predicate': 'enjoy'}` \
**Answer**: *Bob* \
\
**Question 2**: *Who serves the best coffee in the city?* \
**Semantic Role Labeling of the relavant sentence**: `{'Agent': 'The new cafe downtown', 'Patient': 'the best coffee', 'Predicate': 'serve', 'Destination': 'the city'}` \
**Answer**: *The new cafe downtown* \
\
**Question 3**: *Where was the cat sleeping?* \
**Semantic Role Labeling of the relavant sentence**: `{'Agent': 'The cat', 'Predicate': 'sleep', 'Patient': 'the windowsill'}` \
**Answer**: *the windowsill* \
\
**Average cosine similarity achieved** = 0.8144

## Conclusion
The developed QA system, utilizing SRL and token classification techniques, has demonstrated strong performance in understanding and responding to natural language queries. By integrating advanced models such as BERT for NER and Sentence Transformers for embeddings, the system effectively identifies semantic roles, parses dependencies, and evaluates sentence relevance through cosine similarity. Achieving an average cosine similarity score of nearly 0.8144, the system proves its capability in aligning predicted answers with ground truth responses. This has potential applications in domains like customer support and information retrieval. To improve the precision and adaptability for a particular application, further fine-tuning and integration with advanced parsing techniques might be helpful. Thus, this will help in serving as a base model for such NLP applications.
