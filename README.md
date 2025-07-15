
# 🎶 Beat-Synced Visualizer 🎥

**Beat-Synced Visualizer** is a Python-based tool that overlays animated squares and connecting lines onto a video, perfectly synced with the beats detected from its audio track. It uses computer vision and audio signal processing to generate eye-catching visual effects.

---

## 📸 Demo Preview

> 🔊 The video below demonstrates how squares and connectors dynamically appear in sync with the beats:

🎬 `Output Video`(https://drive.google.com/file/d/1fT6o3C9wSfdPZ_zXNYTiX_BYvJG1b7fp/view?usp=drive_link)  
_(Run the script with your own video to generate this!)_

---

## ✨ Features

✅ Detects **audio onsets** (beats) using `librosa`  
✅ Tracks points with **Lucas-Kanade Optical Flow**  
✅ Randomized animated **squares** with text inside  
✅ **Connecting lines** drawn between nearby points  
✅ Ambient noise simulation for dynamic motion  
✅ Fully **customizable parameters**  
✅ Output is an aesthetic, synced video  

---

## 📁 Project Structure

```
Beat-Synced-Visualizer/
│
├── main.py                  # 🧠 Core script
├── requirements.txt         # 📦 Dependency list
├── output_with_boxes.mp4    # 🎞 Sample output video
```

---

## ⚙️ How It Works

🎵 The program extracts audio from the input video using `moviepy`, detects beat onsets using `librosa`, then:

1. 📌 Spawns visual squares at beat timestamps using ORB feature detection.
2. 🔁 Tracks the motion of those points frame-by-frame using Lucas-Kanade Optical Flow.
3. 🎨 Animates the visual elements with randomized labels, colors, and movements.
4. 🧵 Draws lines connecting nearby points for a networked aesthetic.
5. 💥 Applies a pop effect by inverting box color regions.

---

## 🛠️ Installation

1. Clone the repository:

```bash
git clone https://github.com/Prixis10/Beat-Synced-Visualizer.git
cd Beat-Synced-Visualizer
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
venv\Scripts\activate  # On Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage

Run the script with your video:

```bash
python main.py -i input.mp4 -o output_with_boxes.mp4
```

🧩 Available options:

| Argument               | Description                                       | Default                       |
|------------------------|---------------------------------------------------|-------------------------------|
| `-i`, `--input`        | Input video file                                  | `sample_data/playing_dead.mp4` |
| `-o`, `--output`       | Output video filename                             | `output_with_boxes.mp4`       |
| `--fps`                | Output frames per second                          | Same as input                 |
| `--life-frames`        | Lifetime (in frames) of each visual square        | `10`                          |
| `--pts-per-beat`       | Max points to spawn on each beat                  | `20`                          |
| `--ambient-rate`       | Points spawned per second regardless of beat      | `5.0`                         |
| `--jitter-px`          | Visual motion jitter in pixels                    | `0.5`                         |
| `--min-size` / `--max-size` | Range for square sizes                       | `15 / 40`                     |
| `--neighbor-links`     | Number of nearest neighbors to link               | `3`                           |
| `--orb-fast-threshold` | ORB keypoint detection sensitivity                | `20`                          |
| `--bell-width`         | Distribution curve width for square sizes         | `4.0`                         |
| `--seed`               | Random seed for reproducibility                   | `None`                        |

---

## 🧠 Technologies Used

- `Python 3.10+`
- `OpenCV` - for computer vision & tracking
- `Librosa` - for beat/onset detection
- `MoviePy` - for video/audio processing
- `NumPy` - for mathematical operations
- `UUID` & `random` - for aesthetic randomness

---

## 🔮 Possible Enhancements

- 📷 **Webcam/Live video** integration (in progress)
- 🌈 Add color theme modes (retro, techno, cyberpunk)
- 🧠 Integrate audio frequency analysis for style control
- 🌐 Real-time stream overlay (for live performances)

---

## 🧑‍💻 Author

Made with 💡 by [**Pramit Roy**](https://github.com/Prixis10)  
🔗 [LinkedIn](https://linkedin.com/in/prxmit) | 📧 prxmit.roy@gmail.com

---

## 📃 License

This project is licensed under the **MIT License**.  
Feel free to fork, modify, and build upon it! 🚀

---

⭐ **If you like this project, consider giving it a star!**
