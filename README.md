# Machine Translation with Transformer
Project for the Programming Integration Project - AI course.

## Summary
Building a **Transformer** model for language translation, apply on 4 different languages (Vietnamese, English, Italian, French) then deploy the model on **Flask** web application.


## Background

In this project, I used Keras - Tensorflow library to implement the Transformer architecture, and train on 5 different data-sets. This is group work with 5 members, and I'm responsible for applying on Eng-Vie data-set and building the Flask web application.

The application is described as:
* Get an input sentences of language A
* Output a sentence of language B corresponding to user's choice.

## Installation
### Environment
```bash
pip install requirements.txt
```
### How it's used?:
The model is deployed using *Flask*, to run and demonstrate the application: 
If you are using anaconda3, do the following:
1. Activate the GPU-environment.
`conda activate [YOUR_GPU_ENVIRONMENT]`
2. Run the `demo.py` file.
`python demo.py`
3. Wait for about 1 minutes for the program to load the model and deploy it on `localhost`.
4. Go to `http://127.0.0.1:5000/` and test the model.

### Data-sets: 5 different data-sets from *Kaggle*.
1. [VietNamese to English](https://www.kaggle.com/hungnm/englishvietnamese-translation)
2. [English to Vietnamese](https://www.kaggle.com/hungnm/englishvietnamese-translation)
3. [English to France](https://www.kaggle.com/digvijayyadav/frenchenglish)
4. [France to English](http://www.manythings.org/anki/fra-eng.zip)
5. [English to Italian](https://www.manythings.org/anki/ita-eng.zip)

## Architecture
<p style="text-align:center;"><img src="https://firebasestorage.googleapis.com/v0/b/mp212-ai.appspot.com/o/camera_capture%2Fpic1.png?alt=media&token=aa74484c-da71-4a7d-83d6-9e30ca177ab9" width="400" height="400"></p>

## Optimization and Metrics:
* Evaluation Metric: **Accuracy**
* Optimization algorithm: **Adam**
* Loss function: **Sparse categorical cross-entropy**

## Performance

| Dataset        | Training Accuracy | Validation Accuracy
| -----------    | ----------------- | ------------------
| Vietnamese-English           | 84%               | 79%
| English-Vietnamese              | 83%               | 82%
| English - Italian              | 77%               | 66%
| French - English              | 86%               | 73%
| English - French              | 72%               | 63%

## Web Application
<p style="text-align:center;"><img src="https://firebasestorage.googleapis.com/v0/b/mp212-ai.appspot.com/o/camera_capture%2Fimage.png?alt=media&token=d12384d2-f79a-4585-a8e1-2076a79183f4" width="700" height="400"></p>

## Challenges
* Some languages didn't perform well (English-French, English-Italian)
* The data-set isn't large enough.

## What next?
* Tune parameters to get higher performance.
* Collect more data.


# Reference. 
* [English-to-Spanish translation with a sequence-to-sequence Transformer](https://keras.io/examples/nlp/neural_machine_translation_with_transformer/).
* Fran ̧cois Chollet (2021),Deep Learning with Python, Second Edition
* Vũ Hữu Tiệp (2018), Machine Learning cơ bản

