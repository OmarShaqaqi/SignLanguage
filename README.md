Sign Language Recognition Using Deep Learning
This project focuses on building a deep learning model for sentence-level sign language recognition, where input videos of sign language gestures are translated into text. The task is similar to video captioning, where the input is a sequence of frames from a video, and the output is the corresponding text representation of the performed sign(s).

Project Overview
The goal of this project is to develop a system that can recognize sign language gestures at the sentence level. The system takes a video as input and outputs the corresponding text representation of the sign(s) performed in the video. This involves:

Feature Extraction: Extracting features from video frames using a pre-trained model (MobileNetV2).

Sequence-to-Sequence Modeling: Using encoder-decoder architectures (LSTM, LSTM with Attention, and Transformer) to map the sequence of video features to a sequence of text tokens.

Evaluation: Measuring the performance of the model using the Word Error Rate (WER) metric.

Dataset
The dataset consists of:

10 different sentences performed by three signers.

80 frames extracted from each video sample.

The dataset is provided as images, with each video sample represented as a sequence of frames.

Models Implemented
1. LSTM-based Encoder-Decoder Model
Encoder: An LSTM network processes the sequence of video features extracted by MobileNetV2.

Decoder: An LSTM network generates the text sequence token by token.

Loss Function: Cross-Entropy Loss.

Evaluation: Achieved a WER of 0.9788.

2. LSTM with Attention
Encoder: An LSTM network processes the sequence of video features.

Decoder: An LSTM network with an attention mechanism to focus on relevant parts of the input sequence.

Loss Function: Cross-Entropy Loss.

Evaluation: Achieved a WER of 1.0678.

3. Transformer Model
Encoder: A Transformer encoder processes the sequence of video features.

Decoder: A Transformer decoder generates the text sequence.

Loss Function: Cross-Entropy Loss.

Evaluation: Achieved a WER of 1.0.

Key Features
Feature Extraction: MobileNetV2 is used to extract features from each frame of the video.

Word Embeddings: Pre-trained GloVe embeddings are used to represent the ground truth text.

Attention Mechanism: Added to the LSTM-based decoder to improve performance.

Transformer Architecture: Implemented for sequence-to-sequence modeling, leveraging self-attention mechanisms.

Evaluation Metric: Word Error Rate (WER) is used to measure the performance of the models.

Results
Model	WER
LSTM	0.9788
LSTM with Attention	1.0678
Transformer	1.0
