**Gesture Based Face Recognition Smart-Attendence System – README

**1. Overview**
The Gesture Based Face Recognition System is a dual-layer biometric authentication solution that enhances security by combining 
facial recognition with gesture-based liveness detection. This contactless system ensures that only authorized users gain access 
while preventing spoofing attempts using photos or videos.

**2. Features**
Dual-Layer Authentication – Combines face recognition with gesture verification.
Gesture-Based Liveness Detection – Prevents spoofing using static images or videos.
Real-Time Processing – Works efficiently with a standard webcam.
Multi-User Support – Allows registration and recognition of multiple users.
User-Friendly Interface – Simple interface using Tkinter or Streamlit.
Attendance Management (Optional) – Logs authenticated user entries.
High Accuracy & Performance – Optimized for CPU-based systems.

**3. System Architecture**

a) Facial Authentication Module
Detects faces using Haar Cascade or dlib.
Generates 128-dimensional facial encodings.
Matches live faces with stored embeddings using Euclidean distance/KNN.

b) Gesture Recognition Module
Utilizes MediaPipe Hands to detect 21 hand landmarks.
Recognizes predefined gestures such as:
Open Palm
Closed Fist
Hand Wave
Directional Movement

c) Access Control Decision Module
Grants access only when both facial recognition and gesture verification are successful.

**4. Technologies Used**
Technology	Purpose
Python 3.8+	Core programming language
OpenCV	Image processing and webcam handling
MediaPipe	Hand gesture recognition
face_recognition / dlib	Facial detection and encoding
NumPy	Numerical computations
Tkinter / Streamlit	Graphical User Interface
Pandas (Optional)	Attendance logging

**5. Installation Guide**
  Prerequisites
  Python: Version 3.8 – 3.10 (Recommended: Python 3.10)
Webcam
Operating System: Windows 10/11, macOS, or Linux

**Git**
Step 1: Clone the Repository
git clone https://github.com/your-username/gesture-face-recognition.git
cd gesture-face-recognition

Step 2: Create a Virtual Environment
python -m venv venv
Activate the Environment
**Windows**
venv\Scripts\activate
**macOS/Linux**
source venv/bin/activate

Step 3: Install Required Dependencies
pip install -r requirements.txt

Step 4: Install dlib (if not installed)
pip install cmake
pip install dlib

Note: On Windows, you may need to install Visual Studio Build Tools for successful installation.

Step 5: Verify Installation
python -c "import cv2, mediapipe, face_recognition, numpy; print('All libraries installed successfully!')"

**6. Usage Instructions**

Register a New User

python register_user.py

Train the Model

python train_model.py

Authenticate a User

python main.py

View Attendance (Optional)

python attendance.py

**7. Project Structure**
gesture-face-recognition/

├── dataset/                   # Stored face images

├── encodings/                 # Serialized facial embeddings

├── gestures/                  # Gesture data

├── attendance/                # Attendance logs

├── models/                    # Trained models

├── register_user.py           # User registration

├── train_model.py             # Model training

├── main.py                    # Authentication system

├── attendance.py              # Attendance management

├── requirements.txt           # Project dependencies

└── README.md                  # Project documentation

**8. Test Cases**
Correct face and gesture → Login successful
Incorrect face or gesture → Access denied
Duplicate user → Registration prevented
Low lighting → Warning displayed

**9. Future Enhancements**
Mobile and IoT integration.
Improved performance in low-light conditions.
Customizable user-defined gestures.
Cloud-based multi-user database.
Deep learning-based gesture classification.
Voice-assisted authentication.

**10. Troubleshooting**
Issue	Solution
ModuleNotFoundError	Install dependencies using pip install -r requirements.txt.
Webcam not detected	Check camera permissions and ensure no other application is using it.
dlib installation error	Install cmake and Visual Studio Build Tools.
Slow performance	Ensure adequate lighting and reduce camera resolution.
Face not recognized	Re-register the user with clearer images.

**11. License**

This project is developed for academic and research purposes. You may modify and use it with proper attribution.
