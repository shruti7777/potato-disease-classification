# 🥔 Potato Disease Classification using Deep Learning

A deep learning project that uses a **Convolutional Neural Network (CNN)** to classify potato leaf images into three categories: Early Blight, Late Blight, and Healthy. Built with TensorFlow, Keras, and Flask, the project combines image classification with a simple web interface for interactive predictions.

The goal is to explore how computer vision can help identify visual signs of potato leaf diseases and make machine learning models accessible through a web application.

## ✨ Features

- **Three-class classification:** Identifies Early Blight, Late Blight, and Healthy potato leaves.
- **CNN-based image recognition:** Learns visual patterns from labeled potato leaf images.
- **Image preprocessing:** Resizes input images and normalizes pixel values before classification.
- **Prediction confidence:** Displays the predicted class along with the model's confidence score.
- **Flask web application:** Provides an interface to upload a leaf image and view the prediction.
- **Model evaluation:** Tracks training performance and evaluates the trained model on a separate test dataset.

## 📊 Model Performance

The trained CNN achieved the following results on the project's test dataset:

| Metric | Result |
|---|---:|
| Test accuracy | **98.96%** |
| Test loss | 0.0327 |
| Training epochs | 20 |
| Batch size | 32 |
| Input image size | 255 × 255 pixels |
| Number of classes | 3 |

These results are from the test dataset used in this project. Performance on new images, especially photographs taken under different lighting conditions or backgrounds, may vary.

## 🌿 Classes Supported

| Class | Description |
|---|---|
| `Potato___Early_blight` | Potato leaves showing visual patterns associated with early blight |
| `Potato___Late_blight` | Potato leaves showing visual patterns associated with late blight |
| `Potato___healthy` | Potato leaves labeled as healthy in the dataset |

## 🛠️ Tech Stack

- **Python** — application and model development
- **TensorFlow & Keras** — CNN construction, training, and inference
- **NumPy** — numerical operations and prediction processing
- **Matplotlib** — visualization of images, accuracy, and loss
- **Flask** — backend web framework
- **HTML** — frontend interface
- **Pillow** — image loading and processing
- **Git & GitHub** — version control and project hosting

## 🧠 How It Works

1. **Dataset loading:** Loads labeled potato leaf images from the PlantVillage directory.
2. **Preprocessing:** Resizes images to 255 × 255 pixels and rescales pixel values to the range 0–1 inside the model.
3. **Dataset splitting:** Divides the dataset into training, validation, and test subsets.
4. **Data augmentation:** Applies random horizontal and vertical flips and rotations to increase training-image variation.
5. **CNN training:** Uses convolutional and max-pooling layers to learn visual features, followed by dense layers for classification.
6. **Model evaluation:** Measures accuracy and loss on the test dataset.
7. **Web deployment:** Loads the saved model in Flask and uses it to predict the class of an uploaded image.

The final classification layer uses softmax to produce a probability distribution across the three classes.

## 📁 Project Structure

```text
potato-disease-classification/
│
├── app.py                  # Flask application
├── potatodisease.ipynb     # Model development and training notebook
├── model.h5                # Trained model (download separately if not committed)
├── requirements.txt        # Python dependencies
├── .gitignore              # Files excluded from Git
│
├── templates/
│   └── index.html          # Web interface
│
├── static/                 # Static files and uploaded images
│
├── PlantVillage/            # Local dataset (not included in Git)
└── venv/                    # Local virtual environment (not included in Git)
```

The dataset and virtual environment are kept out of the repository to avoid unnecessarily large uploads. The trained model must be available locally for the Flask application to start.

## 🚀 Getting Started

### Prerequisites

- Python version compatible with your installed TensorFlow release
- Git
- Visual Studio Code or another Python editor
- A local copy of the trained model, `model.h5`

### 1. Clone the repository

```bash
git clone https://github.com/shruti7777/potato-disease-classification.git
cd potato-disease-classification
```

Replace `YOUR-USERNAME` with your GitHub username and use your actual repository URL.

### 2. Create a virtual environment

**Windows (PowerShell):**

```powershell
py -3.13 -m venv venv
.\venv\Scripts\Activate.ps1
```

Use a Python version supported by your chosen TensorFlow version. If Python 3.13 is incompatible with the TensorFlow release you install, choose a compatible Python version instead.

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Add the trained model

Place the trained `model.h5` file in the project's root directory, alongside `app.py`.

If the model file is not included in the repository, obtain it from the project's maintainer or save it from the training notebook.

### 5. Prepare the web application

Ensure that `templates/index.html` exists and that the `static/` directory is available for uploaded images.

### 6. Run the application

```bash
python app.py
```

Open the local address displayed in your terminal, typically:

http://127.0.0.1:5000

Upload a supported potato leaf image to view the predicted class and confidence score.

## 📦 Dependencies

The main dependencies are listed in `requirements.txt`:

```text
flask
tensorflow
numpy
pillow
```

Matplotlib is also used in the training notebook. If you plan to run the notebook, install it with:

```bash
python -m pip install matplotlib ipykernel
```

## 🔮 Future Improvements

- Add a confusion matrix and per-class precision, recall, and F1-score.
- Test the model on additional real-world potato leaf photographs.
- Improve the interface with image previews, clearer results, and error handling.
- Add a prediction history or downloadable result report.
- Explore transfer learning and compare model architectures.
- Deploy the application to a cloud platform for public access.

## ⚠️ Limitations

This project is an educational machine learning demonstration, not a substitute for expert agricultural diagnosis. Predictions can be affected by image quality, lighting, background, and differences between training images and real-world photographs. The confidence score is the model's output confidence, not a guarantee that the prediction is correct.

## 🤝 Contributing

Suggestions and improvements are welcome.

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test them.
4. Open a pull request describing your improvements.

## 📄 License

No license has been specified yet.

---

**Built as a hands-on deep learning project exploring CNN-based image classification and practical model deployment with Flask.**
