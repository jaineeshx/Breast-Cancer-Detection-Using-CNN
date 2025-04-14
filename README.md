

# Breast Cancer Detection Using Deep Learning

This project uses a Convolutional Neural Network (CNN) to automatically detect and classify breast cancer from ultrasound images. The goal is to support early diagnosis by building an image-based classification model that distinguishes between benign, malignant, and normal breast tissue.

🩻 Dataset Source  
We used the Breast Ultrasound Images Dataset available on Kaggle:  
https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset

—

📂 Project Structure

| File | Description |
|------|-------------|
| Final_Project.ipynb | Main Jupyter notebook containing the entire workflow – from loading the dataset to training and evaluation |
| Mammo_Detect.pdf | Final report describing dataset, model, results, and future scope |
| /Dataset_BUSI_with_GT/ | Folder where images are stored, categorized into benign, malignant, and normal subfolders |
| /models/ | Optional folder to save trained CNN model |
| /outputs/ | Folder to save plots (confusion matrix, ROC curve, accuracy graphs) |

—

🧠 Model Summary

We implemented a CNN with:

- 3 convolutional blocks (Conv2D → MaxPooling → Dropout)
- Flatten → Dense → Dropout → Dense output
- Activation: ReLU & Softmax
- Optimizer: Adam
- Loss: Categorical Crossentropy

—

🧪 Steps to Run

✅ 1. Install Required Packages

Use pip:

pip install tensorflow numpy pandas matplotlib scikit-learn opencv-python seaborn

✅ 2. Load the Notebook

Open the notebook in Jupyter or VS Code:

jupyter notebook Final_Project.ipynb

✅ 3. Update Image Path (if needed)

Make sure the dataset path is correctly referenced in the notebook:

'./dataset/benign', './dataset/malignant', './dataset/normal'

✅ 4. Run All Cells

The notebook does the following:

- Loads and preprocesses image data
- Builds and trains the CNN
- Evaluates the model with accuracy, confusion matrix, and ROC curve
- Visualizes predictions

—

🧾 File Descriptions

- Final_Project.ipynb  
  Main code file. Covers data preprocessing, CNN architecture, training, evaluation, and result visualization.

- Mammo_Detect.pdf  
  Final written report describing the problem, methodology, findings, graphs, and conclusion.

- dataset/  
  Should be structured as:

  /dataset  
  ├── benign/  
  ├── malignant/  
  └── normal/  

  Each folder contains PNG ultrasound images.

- models/  
  This folder is used to optionally save the trained model (.h5 or .pkl).

- outputs/  
  Includes graphs such as:

  - Accuracy vs. Epoch
  - Confusion Matrix
  - ROC Curves for each class

—

📈 Results Summary

- The model achieved high accuracy in classifying benign and malignant cases.
- ROC-AUC scores were also high, indicating reliable performance.
- The confusion matrix showed very few misclassifications, especially between benign and malignant.

—

⚠️ Limitations

- The normal class had fewer samples, which slightly affected its prediction performance.
- The model is trained on a small dataset and hasn’t been clinically validated.
- Results may vary on real-world hospital data.

—

🧩 Future Improvements

- Apply transfer learning (e.g., with ResNet or MobileNet).
- Add Grad-CAM visualizations for explainability.
- Balance class distribution using augmentation or oversampling.
- Use more advanced metrics for evaluation.

—

👨‍💻 Team Members

- Ashutosh Shekhar (1RVU23CSE086)  
- Jaineesh Patel (1RVU23CSE199)  
- Keshav Singh (1RVU23CSE221)  
- Vanshaj (1RVU23CSE526)

—

📃 License

This project is for educational and academic purposes only. It is not intended for clinical use without validation.
