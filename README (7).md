# Machine Learning

# ESSY: Essay Scoring System
![Application Display](https://github.com/tsabitapr/PBKK/assets/93377643/536d344e-1e4a-4968-b66d-ebfd4150f77f)

## Team Information
**Team ID: C241-PS117**
| Bangkit Student ID | Name                                  | Institution                        | Specialization         |
|--------------------|---------------------------------------|------------------------------------|------------------------|
| M004D4KX3328       | Melanie Sayyidina Sabrina Refman      | Institut Teknologi Sepuluh Nopember| Machine Learning       |
| M004D4KX2891       | Yusna Millaturrosyidah                | Institut Teknologi Sepuluh Nopember| Machine Learning       |
| M004D4KX1711       | Tsabita Putri Ramadhany               | Institut Teknologi Sepuluh Nopember| Machine Learning       |

## Project Overview
ESSY is an essay scoring system that utilizes Optical Character Recognition (OCR) and cosine similarity for autograding essays. The primary goal of this application is to assist teachers in automating the grading process for essay answers, thereby reducing manual workload and improving efficiency.

## Dataset
The dataset used for this project is the IAM Handwriting Word Database. You can access the dataset [here](https://www.kaggle.com/datasets/nibinv23/iam-handwriting-word-database).

## Machine Learning Workflow
1. **Data Collection**: The dataset is sourced from Kaggle, containing various handwriting samples.
2. **Data Preprocessing**: Images are processed and resized to a standard format. Labels are encoded for training.
3. **Model Development**: The model uses CNN for feature extraction and bidirectional LSTM for text prediction. The model is trained with CTC loss to handle variable length sequences.
4. **Training**: The model is trained using TensorFlow and Keras, with checkpoints to save the best models based on validation loss.
5. **Evaluation**: The model's performance is evaluated using validation data. The best performing model is saved.
6. **Prediction and Scoring**: The model predicts text from images, which is then compared using cosine similarity for scoring essays.

## Model
The model architecture includes:
- **Input Layer**: Accepts images of shape (32, None, 1).
- **Convolutional Layers**: Extract features from the input images.
- **Bidirectional LSTM Layers**: Learn temporal dependencies.
- **Dense Layer**: Output layer with softmax activation for character probabilities.

![Model Architecture](https://github.com/tsabitapr/PBKK/assets/93377643/0b64d3d4-37b0-47f4-85fd-a4b9e0682896)

## Video Presentation
For a detailed explanation, watch our 10-minute video presentation [here](https://youtu.be/yo58GTY1zxw).

## Slide Presentation
You can view our slide presentation [here](https://www.canva.com/design/DAGIRqENrXY/fYHLl7T-LwJOd8Y7C-U4ew/view?utm_content=DAGIRqENrXY&utm_campaign=designshare&utm_medium=link&utm_source=editor).

## Latest Code and Model
- **Latest Code**: [machine-learning/model_HTR_OCR_update.ipynb](https://github.com/C241-PS117/machine-learning/blob/main/model_HTR_OCR_update.ipynb)
- **Latest Model**: [Link to the latest model](https://github.com/C241-PS117/machine-learning/blob/main/Update-Text-Recognition.h5) (Update with actual link)

## Contributors
- Melanie Sayyidina Sabrina Refman
- Yusna Millaturrosyidah
- Tsabita Putri Ramadhany

## Acknowledgments
We would like to thank our instructors and mentors for their guidance and support throughout this project.

## Contact
For any questions or inquiries, please contact us at our respective email addresses provided in our GitHub profiles.
