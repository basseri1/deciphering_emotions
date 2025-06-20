# Deciphering Emotions in Children Storybooks: A Comparative Analysis of Multimodal LLMs in Educational Applications

### Abstract:

Emotion recognition capabilities in multimodal AI systems are crucial for developing culturally responsive educational technologies, yet remain underexplored for Arabic language contexts where culturally appropriate learning tools are critically needed. This study evaluates the emotion recognition performance of two advanced multimodal large language models, GPT-4o and Gemini 1.5 Pro, when processing Arabic children's storybook illustrations. We assessed both models across three prompting strategies (zero-shot, few-shot, and chain-of-thought) using 75 images from seven Arabic storybooks, comparing model predictions with human annotations based on Plutchik's emotional framework. GPT-4o consistently outperformed Gemini across all conditions, achieving the highest macro F1-score of 59% with chain-of-thought prompting compared to Gemini's best performance of 43%. Error analysis revealed systematic misclassification patterns, with valence inversions accounting for 60.7% of errors, while both models struggled with culturally nuanced emotions and ambiguous narrative contexts. These findings highlight fundamental limitations in current models' cultural understanding and emphasize the need for culturally sensitive training approaches to develop effective emotion-aware educational technologies for Arabic-speaking learners.

### All original images referenced in this work are from:

We Love Reading, a community-led, shared book-reading program that was developed in Jordan by a Jordanian-run NGO.

### Analysis Tool:

The emotion annotation analysis was conducted using the automated annotation script available at: [LLM-Image-Emotion-Annotator](https://github.com/basseri1/LLM-Image-Emotion-Annotator/tree/main). This Python tool enables automated emotion labeling of images using GPT-4o and Gemini 1.5 Pro with multiple prompting strategies (zero-shot, few-shot, and chain-of-thought).


### Repository Files:

* #### Main_emotion_data_cleaned.csv:
  Contains the complete dataset with image labels and corresponding emotion annotations from human evaluators compared against AI model predictions. Includes results for both GPT-4 and Gemini models across three different prompting strategies:
  - **Zero-shot prompting**: Direct emotion classification without examples
  - **Few-shot prompting**: Classification with a small number of labeled examples  
  - **Chain-of-thought (CoT) prompting**: Step-by-step reasoning approach
  
  Each row represents a single storybook page image with columns for:
  - `image_name`: Filename of the storybook page image
  - `human_emotion`: Ground truth emotion annotation in Arabic
  - `gpt4o_zero_shot`, `gpt4o_few_shot`, `gpt4o_cot`: GPT-4 predictions for each prompting method
  - `gemini_zero_shot`, `gemini_few_shot`, `gemini_cot`: Gemini predictions for each prompting method

* #### Supplementary_analysis/:
  Contains alternative methodological approaches tested on approximately 10% of the image dataset:
  
  - **emotion_data_pluchik.csv**: Extended emotion analysis using the complete Plutchik's Wheel of Emotions with all 21 emotions rather than the 8 primary categories used in the main study. This approach provides a more granular emotional categorization system, allowing models to select from the full spectrum of Plutchik's emotional framework including complex emotions and intensities.
  
  - **emotion_data_segmentation.csv**: Image segmentation analysis focusing on specific visual elements within storybook illustrations. This dataset examines how AI models perform when analyzing cropped segments of images rather than complete pages, providing insights into the importance of contextual visual information for emotion recognition.

### Emotion Categories:

The main study focuses on eight primary emotions plus neutral, expressed in Arabic:
- **Anger** (غضب)
- **Sadness** (حزن)  
- **Happiness** (سعادة)
- **Fear** (خوف)
- **Surprise** (مفاجأة)
- **Anticipation** (ترقب)
- **Trust** (ثقة)
- **Disgust** (قرف)
- **Neutral** (محايد)

The supplementary Plutchik analysis expands this to the complete 21-emotion framework, including complex emotions such as love, submission, awe, disapproval, remorse, contempt, aggressiveness, optimism, and others to provide a more nuanced emotional assessment.


## About

This repository contains the complete dataset and analysis framework for evaluating Large Language Model performance in emotion recognition within children's storybook illustrations, with a focus on Arabic language emotional concepts and cultural context. 