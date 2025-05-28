# Named Entity Recognition (NER) with Hugging Face Transformers

This repository implements a Named Entity Recognition (NER) system using Hugging Face's Transformers library. The model is trained on the CoNLL-2003 dataset and leverages GPU acceleration for efficient training.

## Table of Contents

* [Overview](#overview)
* [Setup](#setup)

  * [Virtual Environment (Optional)](#virtual-environment-optional)
  * [Installation](#installation)
* [Dataset](#dataset)
* [Model Architecture](#model-architecture)
* [Training](#training)
* [Memory Efficiency](#memory-efficiency)
* [Evaluation](#evaluation)
* [Results](#results)
* [Acknowledgements](#acknowledgements)
* [License](#license)

## Overview

Named Entity Recognition (NER) is a subtask of information extraction that seeks to locate and classify named entities in text into predefined categories such as person names, organizations, locations, etc. This project utilizes Hugging Face's Transformers library to fine-tune a pre-trained model for the NER task.([GitHub][1])

## Setup

### Virtual Environment (Optional)

It's recommended to use a virtual environment to manage dependencies:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Installation

Install the required packages using pip:

```bash
pip install -r requirements.txt
```

## Dataset

The model is trained on the CoNLL-2003 dataset, which contains annotated text for NER tasks.([NLP-progress][2])

![image](https://github.com/user-attachments/assets/29da6321-622a-4090-9196-b3b3c44809d2)

## Model Architecture

The NER model is based on a pre-trained Transformer architecture, fine-tuned for token classification tasks. The architecture includes:

* Pre-trained Transformer encoder
* Token classification head

## Training

Training is performed using GPU acceleration, which significantly reduces training time. The training script is provided in `train_model.ipynb`.

## Memory Efficiency

To optimize memory usage during training, a custom data collator is implemented. This collator efficiently batches input sequences and handles padding, ensuring that GPU memory is utilized effectively.

## Evaluation

Evaluation metrics include precision, recall, and F1-score. The evaluation script is included in the repository and provides detailed performance metrics on the validation and test sets.

## Results

The model achieves competitive performance on the CoNLL-2003 dataset.([NLP-progress][2])

*Detailed results and performance metrics to be added here.*

## Acknowledgements

This project utilizes the following resources:([GitHub][1])

* [Hugging Face Transformers](https://github.com/huggingface/transformers)
* [CoNLL-2003 Dataset](https://www.clips.uantwerpen.be/conll2003/ner/)

## License

This project is under MIT License.

---

Feel free to customize this README further by adding specific details about your model architecture, training parameters, evaluation results, and any other relevant information.

[1]: https://github.com/axelmukwena/named-entity-recognition?utm_source=chatgpt.com "axelmukwena/named-entity-recognition: Person Named ... - GitHub"
[2]: https://nlpprogress.com/english/named_entity_recognition.html?utm_source=chatgpt.com "Named entity recognition - NLP-progress"
