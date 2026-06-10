# AI-Driven Face Tracking & Cropper 📱

An automation solution built for the short-form video era. This tool handles the manual work of converting horizontal landscape footage into vertical social media clips by utilizing **OpenCV** face detection models to shift the 9:16 crop window relative to the active speaker's location.

### Key Capabilities
- Real-time frame-by-frame bounding box coordinates tracking.
- Intelligent smoothing logic to prevent jittery camera movements.
- Automated export configurations preset for mobile viewing.
- 
## 📱 Smart-Framing Example

### 📥 Input Framework (Widescreen 16:9)
- **Source Resolution:** 1920 x 1080 pixels
- **Subject Position:** Speaker moves from the left third of the screen to the right third over 10 seconds.

### 🧠 OpenCV Coordinate Processing
- **Frame 001:** Face coordinates localized at `X: 450, Y: 200`. Center crop window at `X: 450`.
- **Frame 150:** Subject steps right. Face localized at `X: 980, Y: 205`. Center crop window smoothly interpolates to `X: 980`.

### 📤 Output Framework (Vertical 9:16)
- **Export Resolution:** 1080 x 1920 pixels (Social Media Ready)
- **Result:** The camera tracking system acts like a virtual cameraman, panning automatically to keep the speaker dead center.
