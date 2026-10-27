
#Gesture-Controlled Presentation Assistant

A real-time, computer vision-based presentation controller powered by OpenCV, MediaPipe, and PyAutoGUI. Control your slideshows (Google Slides, Keynote, PowerPoint) seamlessly using intuitive hand gestures through your webcam.

📍Features:

Real-Time Hand Tracking: Powered by Google MediaPipe's HandLandmarker for accurate, low-latency joint detection.

Natural Mirror Display: Live video feedback is horizontally flipped to mirror user movement naturally.

Cooldown Protection: Integrated gesture debouncing (1.5s cooldown) prevents duplicate keypresses when holding gestures.

Cross-Platform Compatibility: Simulates native keyboard events to interact with presentational software seamlessly.

Automated Model Management: Built-in setup script handles downloading and verifying required ML task models.

📍Gesture Map & Controls

Gesture ActionShortcut Triggered

🖐️ Open Palm (4 Fingers Up)Next SlideRight Arrow

🤟 3 Fingers UpPrevious SlideLeft Arrow

✌️ 2 Fingers UpStart SlideshowCmd + Enter (macOS) / F5

✊ Fist (0 Fingers Up)Exit SlideshowEscape


⭐Note: Press Q while focusing on the preview window to stop the application.

Project Structure.
├── main.py            # Main application logic and hand gesture detection pipeline
├── setup_models.py    # Script to download MediaPipe model files automatically
├── requirements.txt   # Python dependencies
└── models/            # Folder created automatically to store MediaPipe task models


**Getting Started

📌Prerequisites
1.Python 3.8 or higher
2.A working webcam

📌Installation
1.Clone the repository:
git clone https://github.com/your-username/gesture-slides-control.git
cd gesture-slides-control

2.Create and activate a virtual environment (optional but recommended):python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3.Install dependencies:
pip install -r requirements.txt

4.Download the required MediaPipe model:
Run the model downloader script once before starting the app:
python setup_models.py


📌Usage
Run the main application script:
python main.py

1.Ensure your webcam is uncovered and well-lit.

2.Open your presentation software (e.g., Google Slides or Keynote).

3.Perform the hand gestures in view of your camera to navigate through your slides hands-free!

📍Tech Stack

**MediaPipe: Landmark detection and real-time computer vision tasks.

**OpenCV: Video stream processing and real-time visual overlay rendering.

**PyAutoGUI: Cross-platform GUI automation for keypress dispatch.


📍LicenseThis project is open-source and available under the MIT License.
