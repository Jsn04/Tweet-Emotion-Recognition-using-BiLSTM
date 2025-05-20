📘 Project: Tweet Emotion Recognition using BiLSTM
🔍 Objective
The goal of this project is to classify tweets into emotional categories using a deep learning model. By analyzing the emotional tone behind each tweet, the system can identify whether the tweet expresses joy, sadness, anger, fear, love, or surprise.

🧠 Model Architecture
Model Type: Sequential
A deep learning model implemented using TensorFlow and Keras.

Layers Overview:

📦 Embedding Layer
Vocabulary size: 10,000

Embedding dimension: 16

Input length: maxlen (max tweet length after padding)

🔁 Recurrent Layers
Bidirectional LSTM (1): 20 units, return_sequences=True

Bidirectional LSTM (2): 20 units

🔚 Output Layer
Dense Layer: 6 units (one for each emotion category), activation: softmax

Output: Probabilities for each class (multiclass classification)

📊 Dataset
Source: Hugging Face Emotion Dataset

Emotion Classes:

joy, sadness, anger, fear, love, surprise

Split:

Training: 16,000 samples

Validation: 2,000 samples

Test: 2,000 samples

⚙️ Training Details
Loss Function: SparseCategoricalCrossentropy

Optimizer: Adam

Metrics: Accuracy

Epochs: Up to 20

EarlyStopping: Enabled with patience=6 (stops training when val_accuracy plateaus)

Input Padding:
All input sequences are padded to uniform length using pad_sequences for compatibility with the embedding layer.

📈 Evaluation Metrics
✅ Accuracy
Training Accuracy: ~97%

Validation Accuracy: ~87–88%

Test Accuracy: ~87–88%


📁 Files
Tweet_Emotion_Recognition_Learner.ipynb:
Complete notebook containing:

Data preprocessing

Tokenization and padding

Model definition and training

Evaluation with accuracy and confusion matrix

