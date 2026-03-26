#### English-to-Hindi Neural Machine Translation (NMT)
This repository contains a complete case study for building an Encoder-Decoder Machine Translation model using LSTM networks and an Attention Mechanism. 
The project demonstrates the full NLP pipeline from raw text preprocessing to model evaluation.

#### Project Overview
Machine Translation is a sequence-to-sequence (Seq2Seq) problem where the goal is to map an input sequence (English) to a target sequence (Hindi). 

#### Key Features:
Custom Text Pipeline: Implemented specialized cleaning for Hindi (Unicode) and English text.
Architecture: Seq2Seq model utilizing LSTM units for capturing long-term dependencies.
Attention Mechanism: Integrated Bahdanau/Luong attention to allow the decoder to focus on specific parts of the input sentence during translation.

#### Dataset & Preprocessing
The dataset consists of parallel English-Hindi sentence pairs.
Text Cleaning: Removal of special characters and normalization.
Tokenization: Mapping words to integers and creating word-to-index dictionaries.
Padding: Standardizing sequence lengths for efficient GPU batch processing.
Special Tokens: Addition of <start> and <end> markers to guide the Decoder’s generation process.

#### Model Architecture
The model consists of two main components:
The Encoder: Processes the English input and compresses the information into a context vector.
The Decoder: Uses the context vector and Teacher Forcing during training to predict the Hindi translation word-by-word.

#### Results
Training Performance: The model achieved a significant reduction in categorical cross-entropy loss over 30+ epochs.
Evaluation: Demonstrates the ability to translate common phrases with a focus on maintaining Subject-Object-Verb (SOV) structure inherent in Hindi.
