# VideoToFace

This project provides a pipeline to extract faces from a video file and cluster them to identify unique individuals. It consists of three main scripts:

- `detect.py`: Extracts faces from a video at specified frame intervals.
- `filter.py`: Clusters the extracted faces to group images of the same individual together.
- `main.py`: Orchestrates the entire process by running `detect.py` and `filter.py` sequentially.

## Features

- **Face Detection**: Uses MTCNN for accurate face detection and alignment
- **Face Recognition**: Uses InceptionResnetV1 model for facial embeddings
- **Clustering**: Groups similar faces using Agglomerative Clustering
- **Quality Filtering**: Selects best images based on clarity and contrast

## Requirements

- Python 3.7+
- opencv-python-headless
- facenet-pytorch
- torch
- torchvision 
- numpy
- scikit-learn
- Pillow
- tqdm

## Installation

```bash
git clone https://github.com/sp3ked/VideoToFace.git
cd VideoToFace
python main.py
