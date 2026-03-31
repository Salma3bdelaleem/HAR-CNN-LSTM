# 🎬 Human Activity Recognition (HAR) using CNN-LSTM

Welcome to my **Human Activity Recognition** project! 🏃‍♂️🤾‍♀️🎾  
This project detects human activities from videos using a **CNN + LSTM** deep learning model.

---

## 📂 Dataset

- **Dataset:** UCF50  
- **Selected Classes (8):**  
  🏀 Basketball  
  🚴 Biking  
  🤿 Diving  
  🏇 HorseRace  
  🎾 TennisSwing  
  🤺 Fencing  
  ⛳ GolfSwing  
  🏋️ Lunges  

- **Videos per class:** ~120  
- **Frames per video:** 20  
- **Frame size:** 64×64 RGB  

---

## 🏗 Model Architecture

The model uses:

1️⃣ **TimeDistributed CNN layers** – extract spatial features from frames  
2️⃣ **LSTM layer** – capture temporal dependencies across frames  
3️⃣ **Dense + Dropout layers** – classify activities and prevent overfitting  

**Training Details:**  
- Optimizer: Adam  
- Loss: Sparse Categorical Crossentropy  
- Epochs: 50  
- Batch Size: 8  

---

## 📊 Results

- **Test Accuracy:** 89% ✅  
- Training and validation graphs are in the `graphs/` folder.  

---

## 🎥 Sample Videos

You can watch the predictions directly here!  

<video width="640" height="360" controls>
  <source src="videos/sample1.mp4" type="video/mp4">
</video>

<video width="640" height="360" controls>
  <source src="videos/sample2.mp4" type="video/mp4">
</video>

> Note: Videos are stored in the `videos/` folder.

---

## 📂 Folder Structure
project/
│
├─ videos/                  # sample test videos
├─ model/                  # saved CNN-LSTM model (.h5)
├─ train_model.ipynb        # training notebook
├─ test_video.ipynb         # testing notebook
└─ README.

---

## 📖 References
UCF50 Dataset: https://www.kaggle.com/datasets/pypiahmad/realistic-action-recognition-ucf50

---

## ⚡ How to Run

1️⃣ Clone the repository:  
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

2️⃣ Run predictions on a new video:

python test_video.py --video_path "videos/sample1.mp4"

The script will:

Predict the activity
Display the video with the predicted label
Save the output video as output_with_label.mp4



