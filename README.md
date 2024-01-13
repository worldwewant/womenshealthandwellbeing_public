# Women’s Health and Wellbeing Training Script

<a href="https://whiteribbonalliance.org"><span align="left">🌐 whiteribbonalliance.org</span></a>
<a href="https://explore.whiteribbonalliance.org/en/healthwellbeing"><span align="left">🌐 explore.whiteribbonalliance.org/en/healthwellbeing</span></a>


•	**Training Code:** If you want to train the model yourself, you can easily do so. The training code is available as a Jupyter notebook, which you can run in Google Colab with a single click. Additionally, the training data used for the model can be found here: Training Data.
<a href="https://colab.research.google.com/github/whiteribbonalliance/womenshealthandwellbeing_public/blob/main/multi_label_classification.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
•	**Inference Code:** If you have survey data in CSV or Excel format and would like to classify them, our NLU can be helpful for the efficient classification. Run the inference code as a Jupyter notebook in Google Colab with just one click. The model used for inference is the multi-label fine-tuned BERT model, which can be found at amoldwalunj/BERT_multi_label_classification_survey_repose_classification on Hugging Face.
<a href="https://colab.research.google.com/github/whiteribbonalliance/womenshealthandwellbeing_public/blob/main/Inference_code.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>


# About the campaign and analysis

Our campaign gathered 1,152,551 responses from 13 countries.

We categorised them using a Transformer model called BERT – trained on about 8,000 training examples. The training examples came from WRA and were augmented by taking more data from the What Women Want campaign and tagging with other tools such as OpenAI. Our overall accuracy was 78% across languages.

We have experimented with developing an array of multilingual (language specific) models, but for this project we used the English translations of non-English texts, as this made the model development easier, since we only needed to develop and quality control a single model. Languages where the classification was particularly tricky included Swahili, Hindi and Arabic, especially those responses in Hindi which mixed English and Hindi or included Hindi in English letters (Hinglish and Roman Hindi). In general the languages where the NLP and NLU was particularly challenging were not languages with smaller total numbers of speakers, but rather languages of the Global South which have been historically underserved by language technology.

The classification task was particularly difficult because we are performing multi-label classification rather than single-label classification (that is, each response can be assigned to one or more categories). When the task is single-label classification, a model receives a low score if it mis-assigns one category, whereas for multi-label classification, a response could correctly belong to three categories and the model might assign it only to two of those categories, and receive an accuracy of 67% on that response. The task is harder and so high accuracy scores are less attainable.

## Who to contact?

You can contact WRA team at https://whiteribbonalliance.org/, or Thomas Wood at https://fastdatascience.com/.
