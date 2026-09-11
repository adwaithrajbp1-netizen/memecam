<img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />
# memecam....

**Pull a face at your webcam. It fires back a meme.**

*by Team Twinkleberry*

</div>

<table>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/08dfd3bb-18f8-485b-8481-0db0189acbdc" width="100%"></td>
    <td><img src="https://github.com/user-attachments/assets/818f54c7-4cd8-4b86-bd23-33368ffebf7c" width="100%"></td>
  </tr>
</table>

memecam🎥

## Basic Details

**Team Name:** Twinkleberry

### Team Members
* Team Lead: Adwaith Raj BP - Sahrdaya College of Engineering and Technology
* Member 1: Haya Ayoobkhan - Sahrdaya College of Engineering and Technology

## Project Description
memecam watches your webcam, works out which face you're pulling, and drops the matching meme over your head — scaled and tracked to follow you around the frame. Point it at Zoom's virtual camera and the whole call sees it.

### The Problem (that doesn't exist)
Nobody has ever once needed a computer vision pipeline to notice that they rolled their eyes in a meeting.

### The Solution (that nobody asked for)
A real-time face, hand, and body tracker that recognizes fourteen specific reactions — gasping, flirting, dancing, "crashing out" — and slaps the matching meme over your head, live, through a fake webcam your meeting app can't tell from a real one.

## Technical Details

### Technologies/Components Used
For Software:
* **Languages used:** Python
* **Frameworks used:** MediaPipe (face/hand/body landmark detection)
* **Libraries used:** OpenCV (pinned), NumPy 1.x (pinned), pyvirtualcam
* **Tools used:** OBS Studio / v4l2loopback (virtual camera backend)

## Implementation

### For Software:

#### Installation
```bash
python3.12 -m venv venv
source venv/bin/activate           # Windows: venv\Scripts\activate
pip install -r requirements.txt
```
> Requires Python 3.11 or 3.12. Dependencies are pinned on purpose — MediaPipe 0.10.30+ breaks on macOS, so it's held at 0.10.21, which forces NumPy 1.x and pinned OpenCV builds. Don't unpin one without unpinning all three.

#### Run
```bash
python twinkleberry.py --calibrate   # once, seven seconds — learns your neutral face
python twinkleberry.py               # preview + virtual camera
python twinkleberry.py --no-vcam     # preview only, no virtual camera
```

| key | does |
|:---:|---|
| `q` | quit |
| `d` | toggle the HUD |
| `c` | recalibrate |
| `1`–`9` `0` `-` `=` `[` `]` | force a reaction on screen for 2 seconds |

## Project Documentation

### For Software:

#### Screenshots (Add at least 3)
<img width="1600" height="899" alt="1" src="https://github.com/user-attachments/assets/0ff86409-5b22-42ad-9c73-37a5a7605ea7" />

<img width="1434" height="1600" alt="2" src="https://github.com/user-attachments/assets/4de5da4e-2df2-4442-800b-a4048c4fb427" />


#### Diagrams
*Camera frame → MediaPipe (face/hand/body landmarks) → measure expressions relative to your calibrated neutral face → decide() picks the first matching pose → meme overlay is scaled and composited onto the frame → pushed out through the virtual camera.*

## Project Demo

### Video
https://drive.google.com/drive/folders/19NY-VCgZPx6YRGDVJHnxjTSVDJm3EPbB?usp=sharing
calibrating, triggering a few reactions, and showing the virtual camera feed inside a meeting app.


## Team Contributions
* Name 1: Adwaith Raj BP - Coding, Debugging, Technical Lead
* Name 2: Haya Ayoobkhan - Documentation, Design, Demo & Pitch

---
Made with ❤️ at TinkerHub Useless Projects
