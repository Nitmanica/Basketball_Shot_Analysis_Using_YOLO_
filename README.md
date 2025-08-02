## Basketball Shot Prediction and Trajectory Analysis
This repository contains the source code for our computer vision-based basketball shot prediction tool. The primary objective of this project is to analyze and predict whether a basketball shot will go into the hoop using object detection and trajectory tracking.

We built this system to assist players and coaches by providing insights into shot success and helping refine techniques. The tool also offers visual feedback through a web interface, allowing users to upload gameplay footage for analysis.

## 🔍 Features
## Basketball and Rim Detection
Leveraging YOLOv5, YOLOv8, and YOLOv11 models, our application detects the basketball and hoop frame-by-frame from the uploaded video. This enables tracking the ball's trajectory and predicting shot outcomes.

## Shot Outcome Prediction
By analyzing the detected ball path, rim proximity, and final ball position, the tool predicts whether the shot is successful. It also visualizes the ball path to aid in understanding the trajectory.

## Model Comparison Dashboard
The tool provides performance comparisons (accuracy, speed, and confidence scores) between YOLOv5, YOLOv8, and YOLOv11 models to showcase advancements and help users choose the most suitable version.

## Interactive Web Interface
A Streamlit-based frontend allows users to upload videos, visualize detections, and view predictions and comparisons interactively.

## 🚀 Installation
To run this project locally:

Clone the repository:

bash
Copy
Edit
git clone https://github.com/Nitmanica/Basketball_Shot_Analysis_Using_YOLO_
cd basketball-shot-analysis
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Download or train the YOLO model weights and place them in the appropriate folders under models/.

▶️ Running the Application
To launch the web interface:

bash
Copy
Edit
cd source
streamlit run streamlit_app.py
Once running, the Streamlit app will open in your browser. Upload a video and select the model to view predictions and analysis.

📊 Dataset
We used a curated dataset sourced from Roboflow and additional gameplay recordings. It includes labeled frames of:

Basketball

Hoop/Rim

Player (for context and future expansion)

We augmented the dataset to include varied camera angles, lighting, and player movements for better generalization.

🧠 Training the Model
We trained YOLO models (v5, v8, v11) with the following hyperparameters:

Epochs: 40

Batch Size: 16

Optimizer: SGD

Momentum: 0.95 (0.8 for initial 3 warmup epochs)

Weight Decay: 0.0005

IOU Threshold: 0.2 (evaluation)

The trained weights, along with training metrics like precision-recall curves and confusion matrices, are stored in the weights/metrics/ directory.

🔮 Future Work
We plan to enhance the system by integrating:

Pose estimation for biomechanics analysis (elbow, knee, wrist angles)

Real-time prediction support using webcam or live feed

Shot classification based on player type (free throw, jump shot, etc.)

Integration with coaching dashboards and statistics tracking

👥 Contributors
This project was developed by Nitish Manica as part of a broader exploration into sports analytics using AI.
Open to collaboration—feel free to submit issues or pull requests!

📄 References
More technical details, visualizations, and supporting literature are available in the pdf file attached in this repository.
