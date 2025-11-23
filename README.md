# FACE-RECOGNITION-SYSTEM-IN-PYTHON

Face Recognition Attendance System - Complete
 Detailed Explanation
 Project Objective:
 The main objective of this project is to automate the attendance system using facial recognition
 technology. Instead of manually marking attendance, this system uses a camera to detect and
 recognize student faces and automatically record their attendance in a database. It aims to reduce
 manual errors and save time.
 
 Project Workflow:
 1. Initialize Database and Tables
 2. Register Students (Add Details and Capture Faces)
 3. Train Face Recognition Model (LBPH)
 4. Start Real-Time Face Recognition and Mark Attendance
 5. View or Delete Attendance Records
 6. Retrain Model as Needed
    
 1. Database Initialization:
 The system creates a SQLite database named attendance.db. It contains two main tables:
 students and attendance. These tables store student information and daily attendance records
 respectively.
 
 2. Student Registration:
 Students can be added in two ways: using the webcam or using an existing image. Once the
 student’s details are entered, the system captures their face images or extracts them from the
 provided image file. These images are saved inside a folder named after their student ID in the
 'known_faces' directory.
 After capturing the images, the system retrains the model so it can recognize the new student in
 future sessions.

 3. Model Training (LBPH Algorithm):
 The Local Binary Pattern Histogram (LBPH) algorithm is used for face recognition. It works by
 analyzing small patterns on the face and converting them into a histogram representation. All saved
 face images are used to train the model, which is saved as 'face_model.yml'. Labels (student IDs
 and names) are saved in 'face_labels.pkl' using Pickle.

 4. Real-Time Face Recognition and Attendance Marking:
 When the system starts recognition, it opens the webcam and detects faces in real-time. For each
 detected face, the recognizer predicts the student ID and calculates a confidence value. If the
 confidence value is below a threshold (e.g., 70), it confirms recognition and marks attendance in the
 database. If the student’s attendance for that day is already marked, it skips to avoid duplication.

 5. Viewing and Managing Attendance:
 The user can view recent attendance records or records for a specific date. The data is retrieved
 from the database and displayed in a structured format, showing the student’s name, date, time,
 and status.

 6. Key Features and Functions:- Add, list, and delete student records.- Capture faces using webcam or image.- Train and load the LBPH recognition model.- Recognize faces in real time and mark attendance.- Store attendance in the database.- View attendance reports by date.- Retrain model automatically after changes.

    
 Conclusion:
 This project effectively demonstrates how artificial intelligence and computer vision can be used for
 real-world automation. By integrating face recognition with database management, it ensures a
 reliable and efficient attendance process. It eliminates manual effort and provides accurate,
 automatic record-keeping
