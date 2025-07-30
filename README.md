# Football Analysis Pipeline

This repository provides a pipeline for analyzing football match videos using computer vision and deep learning. The pipeline tracks players and the ball, estimates camera movement, assigns teams, transforms views, and calculates speed and distance metrics.

## Features

- **Object Tracking:** Detects and tracks players and the ball using YOLOv5.
- **Camera Movement Estimation:** Estimates and visualizes camera movement per frame.
- **Team Assignment:** Assigns team colors to players.
- **Ball Possession:** Identifies which player has the ball and which team is in control.
- **Speed & Distance Estimation:** Calculates speed and distance for tracked objects.
- **View Transformation:** Transforms player and ball positions to a top-down view.
- **Video Output:** Annotates and saves the processed video.

## Directory Structure

```
input_videos/         # Raw input videos
output_videos/        # Annotated output videos
models/               # YOLOv5 model weights
stubs/                # Precomputed tracking/camera movement stubs
assign_team/          # Team assignment module
camera_movement_estimator/ # Camera movement estimation module
player_ball_assigner/ # Ball possession assignment module
speed_and_distance_estimator/ # Speed/distance estimation module
trackers/             # Object tracking module
utils/                # Utility functions
view_transformer/     # View transformation module
main.py               # Main pipeline script
```

## Getting Started

### Prerequisites

- Python 3.8+
- [YOLOv5](https://github.com/ultralytics/yolov5) model weights (`models/best.pt`)
- OpenCV, NumPy, and other dependencies (see `pyproject.toml`)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/CodeHive08/football-analysis.git
    cd football-analysis
    ```

2. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```

3. Place your input video in the `input_videos/` directory.

### Usage

Run the main pipeline:
```sh
python main.py
```
The processed video will be saved in `output_videos/output_video.avi`.

## Customization

- Change the input video path in [`main.py`](main.py).
- Replace model weights in [`models/`](models/) as needed.
- Modify modules in [`assign_team/`](assign_team/), [`camera_movement_estimator/`](camera_movement_estimator/), etc. for advanced features.

## License

This project is licensed under the MIT License.

## Acknowledgements

- [YOLOv5](https://github.com/ultralytics/yolov5)
-