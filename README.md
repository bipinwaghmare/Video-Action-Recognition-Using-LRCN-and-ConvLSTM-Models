# Video Action Recognition using Deep Learning

This project implements video action recognition using deep learning techniques. Two methods are employed for action recognition:
1. **LRCN (Long-term Recurrent Convolutional Networks)**
2. **ConvLSTM (Convolutional Long Short-Term Memory Networks)**

Both methods are used to predict actions in videos by analyzing sequences of frames. The results are displayed on the processed videos along with prediction confidence scores.

---

## Project Overview

### 1. **LRCN Model**
#### Description:
The LRCN model combines Convolutional Neural Networks (CNNs) for spatial feature extraction and Recurrent Neural Networks (RNNs) with LSTMs for temporal sequence learning. 

#### Key Features:
- **CNN Backbone:** Extracts spatial features from video frames.
- **LSTM Layer:** Captures temporal dependencies between frames.
- **Output:** Action predictions with probabilities for each frame.

#### Results:
- **Action Predicted:** `WalkingWithDog`
- **Confidence:** 98.8%

### 2. **ConvLSTM Model**
#### Description:
The ConvLSTM model extends LSTMs by incorporating convolutional operations within the LSTM architecture, making it more effective for spatio-temporal data.

#### Key Features:
- **ConvLSTM Layer:** Processes both spatial and temporal information in one step.
- **Direct Spatio-Temporal Learning:** Eliminates the need for separate feature extraction and temporal learning layers.

#### Results:
- **Action Predicted:** `WalkingWithDog`
- **Confidence:** 97.5%

---

## Implementation Details

### Dataset:
- The model was tested using publicly available videos downloaded from YouTube.
- Frames were preprocessed and normalized for both models.

### Frameworks and Libraries:
- TensorFlow/Keras
- OpenCV
- MoviePy
- NumPy
- Python

### Methodology:
1. **LRCN Methodology:**
   - Frames are extracted and resized to 224x224.
   - Normalized frames are passed through a pre-trained CNN for feature extraction.
   - LSTM layers process temporal sequences of these features.

2. **ConvLSTM Methodology:**
   - Frames are resized and directly passed through the ConvLSTM layers.
   - Spatio-temporal dependencies are learned simultaneously.

### Results:
| Model        | Action Predicted | Confidence |
|--------------|------------------|------------|
| LRCN         | WalkingWithDog   | 98.8%      |
| ConvLSTM     | WalkingWithDog   | 97.5%      |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/video-action-recognition.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the video prediction script for the LRCN model:
   ```bash
   python predict_lrcn.py
   ```
4. Run the video prediction script for the ConvLSTM model:
   ```bash
   python predict_convlstm.py
   ```

---

## Acknowledgment

This project is inspired by research on deep learning techniques for spatio-temporal data processing. Special thanks to the authors of:
- "Long-term Recurrent Convolutional Networks" by Jeff Donahue et al.
- "Convolutional LSTM Network" by Xingjian Shi et al.

Additionally, gratitude goes to:
- OpenAI for guidance and assistance during the project.
- The open-source community for providing pre-trained models and libraries.

---

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this project as long as proper credit is given.

---

## Contact

For any queries or collaborations, feel free to reach out:
- **Name:** Bipin Waghmare
- **GitHub:** [github.com/bipinwaghmare](https://github.com/bipinwaghmare)
- **LinkedIn:** [linkedin.com/in/bipinwaghmare](www.linkedin.com/in/bipin-waghmare-2bb623167)

