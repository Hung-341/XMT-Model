
# XMT-Model

## New Approach X-Model Transformers Against the Challenge of DEEPFAKE Technology

This project introduces a novel X-Model Transformer (XMT) approach to tackle the challenges posed by DeepFake technology, leveraging advanced face extraction techniques and neural networks for detection.

### Requirements:

- **Pytorch** >= 1.4

You can install the required dependencies using:
```bash
pip install -r requirements.txt
```

### Preprocessing:

Before training or prediction, perform face extraction from video data. We use a pretrained YOLOv5 model for accurate face recognition and extraction.

### Training the Model:

You can train the XMT-Model on your own dataset using customizable parameters. Below are the available parameters:

- `-e`: Number of epochs.
- `-s`: Session type (`g` for GPU or `c` for CPU).
- `-w`: Weight decay (default: `0.0000001`).
- `-l`: Learning rate (default: `0.001`).
- `-d`: Path to training data.
- `-b`: Batch size (default: `32`).
- `-p`: Option to display the accuracy and loss during training.

#### Example Command:

To train the model with specific parameters, use the following example:

```bash
python train.py -e 15 -s 'g' -l 0.0001 -w 0.0000001 -d data/sample_train_data/ -p
```

### Model Weights:

- **`xmodel_deepfake_sample.pth`**: This file contains the full weights for deepfake detection using the XMT-Model.

### Prediction:

You can run predictions on both images and videos using the following commands:

#### Predict on Image:
```bash
python image-prediction.py --image_path <your_image_path>
```

#### Predict on Video:

To predict on a video and display the result:
```bash
python video-prediction.py --video_path <your_video_path> --display
```

To predict on a video and save the result to an output file:
```bash
python video-prediction.py --video_path <your_video_path> --output_path <your_output_path> --save
```

### Authors:

- **Le Dang Khoa**
- **Le Gia Hung**
- **Nguyen Hung Thinh**
