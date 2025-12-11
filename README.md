Real-Time Organ Detection for Laparoscopic Surgery using YOLOv11n

A lightweight, high-performance computer vision system designed to detect organs in live laparoscopic surgery using YOLOv11n.
This project explores how real-time AI can support surgeons by enhancing intra-operative visibility and reducing cognitive load during minimally invasive procedures.

🚀 Overview

This repository contains the full pipeline for training, validating, and deploying an organ detection model optimized for real-time surgical environments.
The model is trained on laparoscopic datasets and tuned to handle challenges such as:

Occlusions

Surgical instrument interference

Low-light/variable illumination

Complex tissue textures

The goal is to demonstrate how modern object detection architectures can be adapted for medical AI and operating-room assistance systems.

🧠 Model Architecture

The project uses YOLOv11n due to its balance of:

High inference speed

Lightweight deployment footprint

Strong accuracy for small and medium objects

Custom modifications were applied to improve detection stability during rapid camera motion and high-variance frames.

🏗️ Project Structure
├── data/
│   ├── raw/                  # Original dataset
│   ├── processed/            # Preprocessed images + annotations
├── notebooks/
│   ├── training.ipynb        # Model training workflow
│   ├── evaluation.ipynb      # Evaluation & visualization
├── models/
│   ├── yolov11n.pt           # Final trained weights
├── src/
│   ├── dataset.py            # Dataloader and preprocessing
│   ├── train.py              # Training pipeline
│   ├── infer.py              # Real-time inference script
│   ├── utils.py              # Helper functions
├── results/
│   ├── metrics.json          # Precision, recall, mAP, FPS
│   ├── sample_outputs/       # Annotated output frames
└── README.md

🧪 Training Pipeline

The training workflow includes:

Dataset annotation standardization

Image augmentation (blurs, rotations, low-light simulation)

Hyperparameter tuning

Validation and mAP analysis

FPS and latency testing for real-time use

You can run the official pipeline using:

python train.py --data data.yaml --weights yolov11n.pt --epochs 50

📊 Performance Summary
Metric	Value
Precision	XX%
Recall	XX%
mAP50	XX%
Real-time FPS	XX (on Colab T4)

Replace XX with your actual metrics.

🎯 Use Cases

This system is designed for research and prototyping in:

AI-assisted surgery

Laparoscopic guidance systems

Real-time medical imaging

Surgical tool/organ detection pipelines

Healthcare robotics

▶️ Real-Time Inference

Run live detection:

python infer.py --weights models/yolov11n.pt --source <video_path or webcam_id>


Output frames will be saved in results/sample_outputs/.

🛠️ Tech Stack

Python

PyTorch

YOLOv11n

OpenCV

NumPy

Jupyter/Colab

📁 Dataset

Due to medical imaging restrictions, datasets are not included in the repository.
Please refer to publicly available laparoscopic surgery datasets or use your own annotated dataset.

🤝 Contributing

Contributions are welcome.
Feel free to open issues, submit pull requests, or suggest improvements.

📜 License

This project is for research and educational purposes.
Not intended for clinical use without regulatory approval.
