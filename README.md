# 🔊 VR Audio Localization Study (Unity + HTC Vive)

This repository documents the design, development, and testing of a user study in a virtual reality environment to assess **spatial audio localization accuracy** using different audio engines.

📍 Developed in collaboration with the Laboratory for Multimedia at the Faculty of Electrical Engineering (University of Ljubljana), under mentorship of **dr. Jaka Sodnik** and in cooperation with **Eva Gaberšček**.

---

## 🎯 Study Goal

Evaluate how accurately and quickly users can localize sound sources in a 3D virtual space using different spatial audio engines:

- Unity Audio (default)
- Oculus Spatializer
- Steam Audio (planned)

We log users' head orientation and position data in real-time while sounds are played in 3D space. Two different VR systems are used (Oculus Quest 1 and HTC Vive) to compare hardware performance as well.

---

## 💻 Setup & Technologies

- Unity 2022+
- VR Headsets: Oculus Quest 1 & HTC Vive
- SteamVR
- Audio spatialization plugins (Unity Audio, Oculus, Steam Audio)
- C# for scripting & head tracking
- CSV log files for data collection
- Python (optional) for result analysis

---

## 🧪 What We Track During the Study

Each test session logs the following data in `.csv`:

| Field             | Description                                       |
|------------------|---------------------------------------------------|
| timestamp         | Time since scene started                         |
| user_id           | Unique user ID                                   |
| sound_id          | Identifier of the played sound                   |
| audio_engine      | Unity / Oculus / Steam                           |
| head_position_xyz | 3D coordinates of user's head                    |
| head_rotation     | Orientation of head in yaw/pitch/roll            |
| sound_position    | 3D coordinates of the sound                      |
| reaction_time     | Time taken to localize the sound                 |
| error_angle       | Angular difference between head and source       |
| found             | Boolean – if user successfully localized source  |
