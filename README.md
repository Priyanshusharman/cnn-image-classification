﻿# cnn-image-classification
**Happy-Sad Classifier**

This repository contains code for a simple model that classifies between happy and sad people. The model architecture is a convolutional neural network (CNN) implemented in Keras.

### Model Architecture

The model architecture is defined as follows:

```plaintext
Model: "sequential_2"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_5 (Conv2D)            (None, 254, 254, 16)      448       
                                                                 
max_pooling2d_3 (MaxPooling2 (None, 127, 127, 16)      0         
                                                                 
conv2d_6 (Conv2D)            (None, 125, 125, 32)      4640      
                                                                 
max_pooling2d_4 (MaxPooling2 (None, 62, 62, 32)        0         
                                                                 
conv2d_7 (Conv2D)            (None, 60, 60, 16)        4624      
                                                                 
max_pooling2d_5 (MaxPooling2 (None, 30, 30, 16)        0         
                                                                 
flatten_1 (Flatten)          (None, 14400)             0         
                                                                 
dense_2 (Dense)              (None, 128)               1843328   
                                                                 
dense_3 (Dense)              (None, 1)                 129       
=================================================================
Total params: 1,853,169
Trainable params: 1,853,169
Non-trainable params: 0
```

### Usage

To train the model, you can use the provided dataset and the Python script `train.py`. Make sure you have the necessary dependencies installed, preferably in a virtual environment.

```bash
python train.py
```

To use the trained model for inference or evaluation, you can load it using the `load_model` function provided by Keras.

```python
from keras.models import load_model

# Load the model
model = load_model('path/to/your/model.h5')

# Use the model for inference
result = model.predict(your_data)
```

### Dataset

The dataset used for training is not provided in this repository. You can use your own dataset of happy and sad images for training the model.

### Dependencies

- Python 3.x
- Keras
- NumPy
- (Optional) Matplotlib (for visualization)

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Feel free to reach out if you have any questions or suggestions!
