## Emotion Classification using LSTM and GRU with the Electroencephalography(EEG) Dataset:

### Objective
The primary goal of this project is to classify EEG signals into emotional states using deep learning models, specifically Long Short-Term Memory (LSTM) and Gated Recurrent Unit (GRU).

### Dataset
#### Overview
This dataset comprises EEG brainwave data collected from two individuals **`(1 male, 1 female)`** using a Muse EEG headband. The data capture involved three emotional states **`(positive, neutral, negative)`**, each recorded for **`3 minutes`**. Additionally, six minutes of resting neutral data was recorded. The EEG placements include TP9, AF7, AF8, and TP10, recorded via dry electrodes.

#### Stimuli for Emotion Elicitation
The emotional states were evoked using specific stimuli, including scenes from movies such as "Marley and Me" for negative emotions and "La La Land" for positive emotions.

#### License
- Usability: 6.47
- License: Data files are © Original Authors

### Model Architecture

#### Data Overview
- The dataset consists of **`2548 features`**, including **`mean values, Fast Fourier Transform (FFT) data columns, and label information`**. Exploratory Data Analysis (EDA) involves utilizing FFT for feature extraction and autocorrelation plots for understanding signal characteristics.

#### Data Preprocessing
- FFT is applied for feature extraction, transforming raw EEG readings into frequency-dependent functions.
- Autocorrelation plots offer insights into signal characteristics.

#### Label Encoding
- Labels are encoded using scikit-learn's LabelEncoder to transform them into numeric format.

#### Train-Test Split
- Data is split into training(0.8) and testing sets(0.2) using `train_test_split` from scikit-learn.

#### Model Architecture (LSTM)
- Sequential model with an LSTM layer **`(256 units)`** and a Dense output layer **`(3 units for classification)`**.
- **`Categorical cross-entropy loss`** and **`Adam`** optimizer are used for compilation.
- Early stopping is implemented to prevent overfitting.

#### Model Training (LSTM)
- The LSTM model is trained for **`100`** epochs with a batch size of **`32`**.
- Training and validation accuracy and loss are monitored.

#### Model Architecture (GRU)
- Similar to LSTM, a Sequential model with a GRU layer **`(256 units)`** and a Dense output layer **`(3 units)`** is used.

#### Model Training (GRU)
- The GRU model is trained and evaluated similarly to the LSTM model.

### Model Evaluation

#### Performance Metrics
- Test accuracy and loss are evaluated for both LSTM and GRU models.
- Confusion matrix provides insights into classification performance.

#### Performance Visualization
- Training and validation accuracy and loss are visualized over epochs for both LSTM and GRU models.
- A heatmap of the confusion matrix illustrates classification results.

#### Final Metrics
- **LSTM Final Training Accuracy: `76.77%`**
- **LSTM Final Validation Accuracy: `75.64%`**
- **LSTM Final Training Loss: `51.15%`**
- **LSTM Final Validation Loss: `54.31%`**

- **GRU Final Training Accuracy: `77.42%`**
- **GRU Final Validation Accuracy: `75.88%`**
- **GRU Final Training Loss: `50.34%`**
- **GRU Final Validation Loss: `54.20%`**

### Conclusion
The LSTM and GRU models demonstrate effectiveness in classifying EEG signals. Model performance is visualized, providing insights into training dynamics.

### Next Steps
Further tuning or exploration of different architectures to enhance model performance.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
