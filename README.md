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
python its_giving_v2.py --calibrate   # once, seven seconds — learns your neutral face
python its_giving_v2.py               # preview + virtual camera
python its_giving_v2.py --no-vcam     # preview only, no virtual camera
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
![Screenshot1](Add screenshot 1 here with proper name)
*Add caption explaining what this shows*

![Screenshot2](Add screenshot 2 here with proper name)
*Add caption explaining what this shows*

![Screenshot3](Add screenshot 3 here with proper name)
*Add caption explaining what this shows*

#### Diagrams
![Workflow](Add your workflow/architecture diagram here)
*Camera frame → MediaPipe (face/hand/body landmarks) → measure expressions relative to your calibrated neutral face → decide() picks the first matching pose → meme overlay is scaled and composited onto the frame → pushed out through the virtual camera.*

## Project Demo

### Video
[Add your demo video link here]
*Explain what the video demonstrates — e.g. calibrating, triggering a few reactions, and showing the virtual camera feed inside a meeting app.*

### Additional Demos
[Add any extra demo materials/links]

## Team Contributions
* [Name 1]: [Specific contributions]
* [Name 2]: [Specific contributions]
* [Name 3]: [Specific contributions]

---
Made with ❤️ at TinkerHub Useless Projects
- Want to change **how easily it goes off**? → `Z`, `FLOOR` and `ARM`
