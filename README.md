# Cifar10 image classification by cnn using pytorch

This was an assignment from artifical intelligence lecture (52641-01) of my university.

## Model
- Inspired by VGG16 Network
- Configured to fit to cifar10 dataset
<br><br>
- Layer1
  - Convolution / BatchNorm / ReLU
    - Input channel = 3, Output channel = 64
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 64, Output channel = 64
    - Kernel size = 3, Stride = 1, Padding = 1
  - MaxPool
    - Kernel size = 2, Stride = 2
- Layer2
  - Convolution / BatchNorm / ReLU
    - Input channel = 64, Output channel = 128
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 128, Output channel = 128
    - Kernel size = 3, Stride = 1, Padding = 1
  - MaxPool
    - Kernel size = 2, Stride = 2
- Layer3
  - Convolution / BatchNorm / ReLU
    - Input channel = 128, Output channel = 256
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 256, Output channel = 256
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 256, Output channel = 256
    - Kernel size = 3, Stride = 1, Padding = 1
  - MaxPool
    - Kernel size = 2, Stride = 2
- Layer4
  - Convolution / BatchNorm / ReLU
    - Input channel = 256, Output channel = 512
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 512, Output channel = 512
    - Kernel size = 3, Stride = 1, Padding = 1
  - Convolution / BatchNorm / ReLU
    - Input channel = 512, Output channel = 512
    - Kernel size = 3, Stride = 1, Padding = 1
  - MaxPool
    - Kernel size = 2, Stride = 2
- Layer5 (FC Layer)
  - Linear / ReLU
    - (2048, 2048)
  - Linear / ReLU
    - (2048, 2048)
  - Linear / ReLU
    - (2048, 10)

## Hyper Parameters
- Batch size: 100
- epochs: 15
- learning rate: 0.0025
- **Loss function: Cross Entropy Loss**
- **Optimizer: Adam**

## Result
- Accuracy after training: **84.68%**
- Elapsed time: 8.4Min