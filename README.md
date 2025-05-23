# Color Detector

A Python tool for identifying the dominant colors in images (and videos) using K-Means clustering and mapping to named CSS4 colors.

## Features

* **Image analysis**: extract and name the top *k* dominant colors in any image.
* **Visualization**: display a color bar and report each color’s percentage.
* **Video support**: annotate each frame of a video file (or webcam) with the most prominent color.
* **Offline mapping**: uses Matplotlib’s CSS4 color database—no external API calls.

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/color-detector.git
   cd color-detector
   ```

### 2. Notebook demo

Open `demo.ipynb` to see how to call the `identify_colors()` function in a Jupyter environment, plot the color bar, and customize the cluster count.

### 3. Video mode

Process a video file and save an annotated output:

```bash
python realtime.py --input /path/to/video.mp4 --output annotated.mp4 --colors 3
```

Or, if running locally with a webcam:

```bash
python realtime.py --webcam 0 --colors 3
```

## Configuration Options

* `--colors`: number of clusters/colors to detect (default: 5)
* `--image`: path to input image file
* `--input`: path to input video file
* `--output`: path to save annotated video
* `--webcam`: use a webcam by device index instead of a video file


```text
https://github.com/<your-username>/color-detector
```

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE) for details.
