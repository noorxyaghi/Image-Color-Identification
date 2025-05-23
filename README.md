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
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

### 1. Image mode

Identify colors in a single image:

```bash
python detect_colors.py --image sample_images/demo1.jpg --colors 5
```

This will output something like:

```
Detected colors:
 - lightsteelblue   45.2%   RGB=(176,196,222)
 - crimson          30.1%   RGB=(220, 20, 60)
 - forestgreen      15.6%   RGB=(34,139, 34)
 - gold              5.8%   RGB=(255,215,  0)
 - slategray         3.3%   RGB=(112,128,144)
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

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to:

```text
https://github.com/<your-username>/color-detector
```

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE) for details.
