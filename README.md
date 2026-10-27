# Gesture-Control-Presenter
Gesture-Controlled Presentation AssistantA real-time, computer vision-based presentation controller powered by OpenCV, MediaPipe, and PyAutoGUI. Control your slideshows (Google Slides, Keynote, PowerPoint) seamlessly using intuitive hand gestures through your webcam.FeaturesReal-Time Hand Tracking: Powered by Google MediaPipe's HandLandmarker for accurate, low-latency joint detection.Natural Mirror Display: Live video feedback is horizontally flipped to mirror user movement naturally.Cooldown Protection: Integrated gesture debouncing (1.5s cooldown) prevents duplicate keypresses when holding gestures.Cross-Platform Compatibility: Simulates native keyboard events to interact with presentational software seamlessly.Automated Model Management: Built-in setup script handles downloading and verifying required ML task models.Gesture Map & ControlsGestureActionShortcut Triggered🖐️ Open Palm (4 Fingers Up)Next SlideRight Arrow🤟 3 Fingers UpPrevious SlideLeft Arrow✌️ 2 Fingers UpStart SlideshowCmd + Enter (macOS) / F5✊ Fist (0 Fingers Up)Exit SlideshowEscapeNote: Press Q while focusing on the preview window to stop the application.Project Structure.
├── main.py            # Main application logic and hand gesture detection pipeline
├── setup_models.py    # Script to download MediaPipe model files automatically
├── requirements.txt   # Python dependencies
└── models/            # Folder created automatically to store MediaPipe task models
Getting StartedPrerequisitesPython 3.8 or higherA working webcamInstallationClone the repository:git clone https://github.com/your-username/gesture-slides-control.git
cd gesture-slides-control
Create and activate a virtual environment (optional but recommended):python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies:pip install -r requirements.txt
Download the required MediaPipe model:
Run the model downloader script once before starting the app:python setup_models.py
UsageRun the main application script:python main.py
Ensure your webcam is uncovered and well-lit.Open your presentation software (e.g., Google Slides or Keynote).Perform the hand gestures in view of your camera to navigate through your slides hands-free!Tech StackMediaPipe: Landmark detection and real-time computer vision tasks.OpenCV: Video stream processing and real-time visual overlay rendering.PyAutoGUI: Cross-platform GUI automation for keypress dispatch.LicenseThis project is open-source and available under the MIT License.
