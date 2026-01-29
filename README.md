# Real-Time-Intelligent-Object-Detection-and-Alert-System-Using-YOLO
🧠 1. Problem Statement

⚠️ Road accidents happen due to:

🚘 Vehicles coming too close

🚀 Overspeeding

Drivers need a real-time warning system when:

📏 Distance < 100 meters

⏱ Speed > 70 km/h

🎯 2. Project Objectives

✔ Detect vehicles using YOLOv8n
✔ Estimate distance between vehicles
✔ Calculate speed of nearby vehicles
✔ Trigger SMS alerts 📩 via Twilio
✔ Provide UI interface 🖥️ for video upload
✔ Display live results on video

🔍 3. Scope
✅ In Scope

🎥 Video-based vehicle detection

📐 Distance estimation

🧮 Speed calculation

📲 SMS alert system

🖱️ UI for upload & visualization

❌ Out of Scope

🚦 Vehicle control (braking/steering)

🌐 Cloud deployment

📷 Live hardware camera (future work)

🏗️ 4. System Architecture
👤 User Uploads Video
        ⬇️
🖥️ UI Interface (Streamlit / Tkinter)
        ⬇️
🤖 YOLOv8n Vehicle Detection
        ⬇️
🆔 Object Tracking
        ⬇️
📏 Distance Estimation
        ⬇️
⏱ Speed Calculation
        ⬇️
⚠ Rule Engine
(Distance < 100m & Speed > 70 km/h)
        ⬇️
📩 Twilio SMS Alert

⚙️ 5. Functional Requirements
🎥 FR1: Video Upload

📁 Upload video (.mp4 / .avi)

▶ Start & ⏹ Stop processing

🖼️ Display output frames

🚗 FR2: Vehicle Detection

Detect 🚘 Car, 🚌 Bus, 🚛 Truck

Use YOLOv8n

Draw 🟩 bounding boxes

📏 FR3: Distance Estimation

Use camera calibration

Show distance in meters (m)

⏱ FR4: Speed Calculation

Track same vehicle

Display speed in km/h

⚠ FR5: Alert Condition

Trigger alert if:

📏 Distance < 100 m

🚀 Speed > 70 km/h

📩 FR6: SMS Notification

Twilio SMS

Prevent repeated alerts ⏳

🛡️ 6. Non-Functional Requirements
🧩 Category	📌 Requirement
⚡ Performance	≥ 15 FPS
🎯 Accuracy	±10%
🧑‍💻 Usability	Easy UI
🔒 Security	Secure API keys
♻ Reliability	No SMS spam
🧰 7. Technology Stack
🐍 Programming Language

Python 3.9+

📦 Dependencies
ultralytics
opencv-python
numpy
torch
twilio
streamlit
lap

🤖 Model

YOLOv8n (Fast & Lightweight)

📐 8. Distance Estimation Formula
📏 Distance = (Known Width × Focal Length) / Bounding Box Width


🚘 Vehicle width ≈ 1.8 m

📷 Focal length from calibration

⏱️ 9. Speed Calculation Formula
🚀 Speed = (Distance Travelled / Time) × 3.6


Output in km/h

⚠️ 10. Alert Rule Engine
if distance < 100 and speed > 70:
    send_sms_alert()

📩 11. SMS Alert Format
⚠ ALERT!
🚘 Vehicle approaching dangerously

📏 Distance: 65 m
🚀 Speed: 82 km/h

⚠ Please drive safely!

🖥️ 12. UI Requirements
UI Features

✔ 📁 Video Upload
✔ 🎥 Live Video Display
✔ 🟩 Bounding Boxes
✔ 📏 Distance Overlay
✔ 🚀 Speed Overlay
✔ 🔔 Alert Indicator

UI Framework

Streamlit 🟢 (Recommended)

📂 13. Project Folder Structure
📁 vehicle_alert_system/
│
├── 🤖 models/
│   └── yolov8n.pt
│
├── 🖥️ ui/
│   └── app.py
│
├── 🚗 detection/
│   ├── detector.py
│   └── tracker.py
│
├── 🧰 utils/
│   ├── distance.py
│   ├── speed.py
│   └── alert.py
│
├── 📄 requirements.txt
└── 📘 README.md

✅ 14. Success Criteria

✔ Accurate vehicle detection
✔ Correct distance calculation
✔ Reliable speed estimation
✔ SMS sent on alert conditions
✔ Smooth UI performance

🔮 15. Future Enhancements

🚦 Lane detection
📷 Real-time camera feed
📱 Mobile app
☁ Cloud dashboard
🤝 Multi-vehicle prioritization

🏁 16. Conclusion

This project integrates:
🤖 AI + Computer Vision
📏 Distance & Speed Analytics
📩 IoT Alert System
