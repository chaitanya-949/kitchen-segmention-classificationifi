# Kitchen Layout Classification and Object Detection

This project uses Detectron2 for instance segmentation and ResNet18 for classification of kitchen layouts (e.g., L-shaped, U-shaped, Parallel). It includes steps for training, testing, and inference, along with a utility to calculate dimensions of objects using bounding box predictions. Data annotation was done using LabelMe.

## Note:
This is intended as a reference; leveraging a larger dataset with higher-quality annotations can significantly enhance the output.

## Features

Instance Segmentation: Detect kitchen objects like stove, sink, storage, and counter.

Layout Classification: Classify kitchen layouts into L-shaped, U-shaped, or Parallel.

Bounding Box Dimension Calculation: Extract dimensions of detected objects for further analysis.


## Dependencies

Python Libraries

Python 3.8+

Detectron2

PyTorch

torchvision

NumPy

Matplotlib

OpenCV

Pillow

Clone this repository:

bash
Copy code
git clone 

https://github.com/yourusername/kitchen-segmention-classificationifi.git

cd kitchen-segmention-classificationifi

Install Detectron2:

bash
Copy code
python -m pip install 'git+https://github.com/facebookresearch/detectron2.git'

## Dataset Preparation
Annotation:
Annotations were created using LabelMe and stored as .json files. Each annotation file includes object shapes and labels.

## Directory Structure

/content/drive/MyDrive/data/

    ├── train/
    
    │   ├── L-vorm/
    
    │   ├── U-vorm/
    
    │   ├── Parallel/
    
    └── test/
    
        ├── L-vorm/
        
        ├── U-vorm/
        
        ├── Parallel/

## Training Parameters
### Detectron2 Configuration:

Model: mask_rcnn_R_50_FPN_3x

Base LR: 0.00025

Max Iterations: 1000

Classes: ['stove', 'sink', 'storage', 'counter']

### ResNet18 Classification:

Optimizer: Adam

Learning Rate: 0.001

Epochs: 30

Weighted Loss: [1.0, 2.0, 1.5]


## Future Enhancements
Add more kitchen layout categories.
Fine-tune hyperparameters for better accuracy.

