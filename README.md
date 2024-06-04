# DCU-Net: Dual-Channel U-Net for Image Splicing Forgery Detection

DCU-Net is a dual-channel U-shaped network designed to detect and locate image splicing forgeries. This method is capable of identifying suspicious tampered areas within images by leveraging deep learning techniques. The DCU-Net model incorporates both RGB and residual image features to improve accuracy and robustness in forgery detection.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Model Architecture](#model-architecture)
- [Datasets](#datasets)
- [Results](#results)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Image splicing forgery detection involves identifying regions within an image that have been tampered with, often by cutting content from one image and pasting it into another. DCU-Net addresses this challenge by using a dual-channel approach to capture both the original and tampered features of an image.

## Features
- **Dual-Channel Input:** Utilizes both RGB features and residual image features to enhance detection accuracy.
- **High-Pass Filters:** Extracts edge information of tampered areas to generate residual images.
- **Dilated Convolution:** Captures tampered features with varying granularity.
- **Robust to Attacks:** Maintains performance under Gaussian noise and JPEG compression attacks.

## Model Architecture
The DCU-Net model is composed of three main parts:
1. **Encoder:** Extracts deep features from both the original and residual images using a dual-channel network.
2. **Feature Fusion:** Combines deep features from both channels at multiple stages to enhance contextual understanding.
3. **Decoder:** Decodes the fused features to predict the tampered regions at the pixel level.

## Datasets
DCU-Net was evaluated using two datasets:
- **CASIA 2.0:** A widely-used dataset for image tampering detection.
- **Columbia:** Another benchmark dataset for evaluating forgery detection methods.

## Results
DCU-Net outperforms state-of-the-art methods in both accuracy and robustness. Key performance metrics on the CASIA and Columbia datasets include:

| Metric     | CASIA | Columbia |
|------------|-------|----------|
| F-measure  | 0.7667| 0.8992   |
| Precision  | 0.7772| 0.8406   |
| Recall     | 0.7893| 0.9665   |
| Accuracy   | 0.8793| 0.9505   |

The model demonstrates strong resistance to both Gaussian noise and JPEG compression, maintaining high detection performance even under challenging conditions.

## Usage
1. Prepare your dataset and place it in the `data` directory.
2. Train the model:
    ```bash
    python train.py --config config.yaml
    ```
3. Evaluate the model:
    ```bash
    python evaluate.py --config config.yaml
    ```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License.

## Output
![image](https://github.com/DarkDevil1306/DCU-Net/assets/88668115/556b04f5-03a8-43c9-b3e6-da32912eaaf8)
![image](https://github.com/DarkDevil1306/DCU-Net/assets/88668115/7dd87093-dbd1-4b3a-91ff-d35eeaafd0e0)
![image](https://github.com/DarkDevil1306/DCU-Net/assets/88668115/bb3cb59a-bc7e-4e66-a30d-d0236a0836ea)
![image](https://github.com/DarkDevil1306/DCU-Net/assets/88668115/ec6ac9fb-a41e-427d-9f3a-54fba6c35048)
![image](https://github.com/DarkDevil1306/DCU-Net/assets/88668115/eba8c9b3-fddf-4455-8582-11ed86652850)
---
