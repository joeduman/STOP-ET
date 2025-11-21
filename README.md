# **STOP-ET: Spatio-Temporal Optical Pipeline for Event-Based Threats**

STOP-ET is a modular, lightweight processing pipeline designed to detect, filter, and reconstruct event-camera data under adversarial manipulation.  
This repository includes a demo implementation and sample dataset fragments showing STOP-ET’s performance across multiple neuromorphic benchmarks.

---

## **Environment Setup**

STOP-ET was developed using **Python 3.10.12**.

### Create and activate a virtual environment
```bash
# Check Python version
python --version   # 3.10.12

# Create virtual environment
python3 -m venv stopetenv

# Activate (Linux / macOS)
source stopetenv/bin/activate

# Activate (Windows PowerShell)
.\stopetenv\Scripts\Activate.ps1

# Activate (Windows CMD)
.\stopetenv\Scripts\activate.bat
```

## **Required Packages**
The core dependencies used in the demo are:
```bash
pyinstaller==6.16.0
numpy==2.2.6
scipy==1.15.3
matplotlib==3.7.2
opencv-python==4.12.0.88
tqdm==4.67.1
```
Install all packages with:
```bash
pip install -r requirements.txt
```

## **Included Files** 
### Datasets.zip
----------------
### 1MPX Dataset Fragment
```bash
1MPX/
└── tmp/
    ├── voxel_XXXX.npy   # 10 clean samples
    └── voxel_XXXX.npy   # 1 attacked (Frame Attack)
```
### DVSGesture DAtaset Fragment
```bash
DVSGesture/
└── tmp/
    ├── voxel_XXXX.npy   # 11 clean samples
    └── voxel_XXXX.npy   # 1 attacked (Noise Attack)
```
### NMNIST Dataset Fragment
```bash
NMNIST/
└── tmp/
    ├── voxel_XXXX.npy   # 111 clean samples
    └── voxel_XXXX.npy   # 1 attacked (Removal Attack)
```

## **Executable Demonstration**

Two standalone executables are included for quick evaluation of the STOP-ET pipeline:

| **File**             | **Platform**     |
|----------------------|------------------|
| `STOP-ET_sample` [Anonymous Google Drive](https://drive.google.com/drive/folders/1boO1-lG9yDep87spzuHq1XRw8EWV8jyp?usp=sharing)     | Linux / macOS    |
| `STOP-ET_sample.exe` | Windows          |

Both executables showcase the same denoising, reconstruction, and prediction stages.

Please extract all dataset folders, and place them in the same directory as the executable.
---

## **Attack Generation Scripts**
Attack generation utilities (Noise Attack, Removal Attack, Manipulative Injection) can be provided upon request.


