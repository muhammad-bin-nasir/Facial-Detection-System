
Face Recognition Attendance System with Anti-Spoofing

This project is an advanced Face Recognition-based Attendance System with built-in Anti-Spoofing features to ensure secure and reliable attendance marking. The system detects and recognizes faces in real-time and prevents unauthorized access using live face detection techniques.

🚀 Features

- Real-time Face Detection & Recognition (using face_recognition and OpenCV)
- Anti-Spoofing Mechanism (using Mediapipe Face Mesh to detect real human faces)
- Automatic Attendance Logging to an Excel file (Attendance.xlsx)
- Password-Protected System Access
- Session Control (Only one attendance per person per session)
- Email Report Sending (via configured Gmail account)
- Planned GUI Integration (PyQt/Kivy preferred over Tkinter)
- Face Addition/Removal Feature (for managing registered users)

🛠️ Technologies Used

- Python 3.x
- OpenCV
- face_recognition
- Mediapipe (for Anti-Spoofing via Face Mesh)
- Pandas (for Excel operations)
- smtplib & email (for Email reporting)
- Tkinter / PyQt (planned GUI)

📂 Project Structure

├── main.py                    # Main execution file (real-time detection & attendance)
├── anti_spoofing.py           # Mediapipe Face Mesh based anti-spoofing module
├── face_encodings/            # Stored face encodings of authorized users
├── Attendance.xlsx            # Excel sheet where attendance records are saved
├── utils.py                   # Utility functions (date-time, session handling)
├── email_report.py            # Sends attendance report via email
├── requirements.txt           # Python libraries required
└── README.txt                 # Project documentation

⚙️ Setup Instructions

1. Clone this Repository:

git clone https://github.com/muhammad-bin-nasir/Facial-Detection-System.git
cd Facial-Detection-System

2. Install Required Packages:

pip install -r requirements.txt

3. Run the Application:

python main.py

4. To Train/Add New Faces:
- Place clear face images in the face_encodings/ folder.
- Re-run the encoding generation module (if applicable).

📧 Email Reporting Setup (Optional)

- Update your Gmail credentials in email_report.py.
- Enable "Less secure app access" or generate an App Password if 2FA is enabled.

⚠️ Anti-Spoofing Details

- Uses Mediapipe Face Mesh to ensure that detected faces are real, 3D, and live.
- Prevents photo/video-based spoofing attempts.
- Optionally restricts detection to single-face only to avoid multiple person confusion.

🔮 Future Enhancements

- Full-featured GUI with Face Add/Remove options (planned via PyQt/Kivy)
- QR Code/RFID integration for session-level security
- Liveness Detection using advanced techniques (eye blink, head movement)
- Cloud-based attendance storage (Google Sheets, Firebase)

🤝 Contributions

Pull requests are welcome! For significant changes, please open an issue first to discuss what you would like to change.

📄 License

This project is licensed under the MIT License — see the LICENSE file for details.

✨ Acknowledgements

- OpenCV: https://opencv.org/
- face_recognition: https://github.com/ageitgey/face_recognition
- Mediapipe: https://google.github.io/mediapipe/
