# txtsumm(Text Summarizer API)

## Overview
This project trains a language model to generate concise summaries from longer texts using the CNN/Daily Mail dataset. The trained model is exposed via a RESTful API i.e. FastApi

## Model Training
1. **Dataset**: The model is trained using the [CNN/Daily Mail dataset](https://huggingface.co/datasets/abisee/cnn_dailymail).
2. **Pre-trained Model**: I fine-tuned the `facebook/bart-base` model for the summarization task.
3. **Training Process**: The model was trained for 1 epochs with a learning rate of 2e-5.

### Before and After Training
- Before training: The model produces generic summaries.
- After training: The model generates more context-aware summaries.

## Sample API Requests and Responses
**Request**:
```json
POST /summarise
{
  "prompt": "Your long text here."
}
